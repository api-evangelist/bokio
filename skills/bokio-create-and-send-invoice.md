---
name: Create and publish a Bokio invoice
description: Create a customer, draft an invoice with line items, then publish it via the Bokio Company API.
api: openapi/bokio-company-api-openapi.yml
operations: [post-customer, post-invoice, post-invoice-lineItem, post-invoices-invoiceId-publish, download-invoice]
---

# Create and publish a Bokio invoice

Use the Bokio Company API (`https://api.bokio.se/v1`) to invoice a customer. All
operations are scoped to a company: `companies/{companyId}/...`.

## Auth
- Send `Authorization: Bearer <access_token>`.
- Required scopes: `customers:write`, `invoices:write` (and `invoices:read` to
  download). See `scopes/bokio-scopes.yml`.

## Steps
1. **Create the customer** — `post-customer`
   `POST companies/{companyId}/customers`. Persist the returned `customerId`.
2. **Create a draft invoice** — `post-invoice`
   `POST companies/{companyId}/invoices` referencing the customer. New invoices
   start in `draft` status. Persist `invoiceId`.
3. **Add line items** — `post-invoice-lineItem`
   `POST companies/{companyId}/invoices/{invoiceId}/line-items` (invoice must be
   in `draft`). `taxRate` must be one of 0%, 6%, 12%, 25% or you get
   `code=validation-error`.
4. **Publish** — `post-invoices-invoiceId-publish`
   `POST companies/{companyId}/invoices/{invoiceId}/publish`. Publishing does
   NOT email the customer automatically.
5. **(Optional) Download the PDF** — `download-invoice`
   `GET companies/{companyId}/invoices/{invoiceId}/download` (published only).

## Rules
- Only `draft` invoices can be updated, have line items added, or be deleted.
- Serialize writes to the same invoice — parallel writes to one resource are
  rejected with `429` (concurrency limit). See `conventions/bokio-conventions.yml`.
- Errors use `{ "error": { code, innerCode, message, bokioErrorId } }`; quote
  `bokioErrorId` to Bokio support. See `errors/bokio-problem-types.yml`.
