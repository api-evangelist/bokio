---
name: Record and reconcile a Bokio journal entry
description: Post a double-entry journal entry, attach a receipt upload, and reverse it if needed.
api: openapi/bokio-company-api-openapi.yml
operations: [post-journalentry, add-upload, get-journalentries-journalId, reverse-journalentry, post-journal-entry-comment]
---

# Record and reconcile a Bokio journal entry

Book accounting transactions into a company's ledger via the Bokio Company API.

## Auth
- `Authorization: Bearer <access_token>`.
- Scopes: `journal-entries:write` / `journal-entries:read`, `uploads:write`.

## Steps
1. **Create the journal entry** — `post-journalentry`
   `POST companies/{companyId}/journal-entries`. Debits and credits must
   balance. Persist the returned `journalEntryId`. A `400` with
   `code=validation-error` carries per-field detail in `errors[]`.
2. **Attach a receipt** — `add-upload`
   `POST companies/{companyId}/uploads` as `multipart/form-data` with the file
   plus `journalEntryId` to link the document to the entry (image or PDF, one
   file per request).
3. **Verify** — `get-journalentries-journalId`
   `GET companies/{companyId}/journal-entries/{journalEntryId}`.
4. **Add a note (optional)** — `post-journal-entry-comment`
   `POST .../journal-entries/{journalEntryId}/comments` (plain text only).
5. **Reverse if wrong** — `reverse-journalentry`
   `POST companies/{companyId}/journal-entries/{journalEntryId}/reverse`.
   Only entries created through the API can be reversed; already-reversed
   entries and invoice-linked entries cannot.

## Rules
- Serialize writes to the same journal-entry path (429 on concurrent writes).
- Comments can only be updated/deleted by the integration that created them.
