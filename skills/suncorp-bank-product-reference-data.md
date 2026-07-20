---
name: Look up Suncorp Bank products (CDR PRD)
description: Retrieve and compare Suncorp Bank's currently offered banking products using the public, unauthenticated Consumer Data Right Product Reference Data API.
api: openapi/suncorp-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
auth: none
base_url: https://id-ob.suncorpbank.com.au/cds-au/v1
---

# Look up Suncorp Bank products (CDR PRD)

This skill uses Suncorp Bank's public Consumer Data Right (CDR) Product Reference
Data API. It is **read-only and unauthenticated** — no API key, token, or consent
is required. All responses follow the Australian Consumer Data Standards.

## Prerequisites

- Base URL: `https://id-ob.suncorpbank.com.au/cds-au/v1`
- Every request MUST send the `x-v` header (API version). Use `x-v: 5` for the
  product list and `x-v: 7` for product detail. If you send an unsupported
  version you get `406` with CDS code `urn:au-cds:error:cds-all:Header/UnsupportedVersion`.

## Steps

1. **List products** — call `listBankingProducts`:
   `GET /banking/products` with header `x-v: 5`.
   - Optional filters: `effective` (CURRENT|FUTURE|ALL, default CURRENT),
     `product-category` (e.g. `TRANS_AND_SAVINGS_ACCOUNTS`, `RESIDENTIAL_MORTGAGES`,
     `CRED_AND_CHRG_CARDS`), `updated-since` (ISO date-time), `brand`.
   - Paginate with `page` and `page-size` (default 25). Read `meta.totalRecords`
     and `meta.totalPages` to know when to stop.
   - Each item carries a `productId`; results are ordered by `lastUpdated` descending.

2. **Get product detail** — for a chosen `productId`, call `getBankingProductDetail`:
   `GET /banking/products/{productId}` with header `x-v: 7`.
   - The detail payload embeds `features[]`, `constraints[]`, `eligibility[]`,
     `fees[]`, `depositRates[]`, and `lendingRates[]`. Each array element has a
     `type` enum and an `additionalValue`/`additionalInfo`/`additionalInfoUri`.
   - A `404` (`Resource/NotFound` or `Resource/Invalid`) means the productId is
     no longer offered or malformed.

3. **Compare / present** — use `productCategory` to group, and the rate/fee arrays
   to compare. Do not attempt to link a product to a customer account: the CDR
   model intentionally provides no product→account id.

## Rules & conventions

- Send `x-v` on every call; treat `406` as "retry with a supported version".
- Errors use the CDS envelope `{ "errors": [ { "code", "title", "detail" } ] }`
  (see `errors/suncorp-bank-problem-types.yml`) — NOT RFC 9457.
- The data reflects openly offered products only; terms may change without notice,
  and following the ANZ acquisition some products may be varied to ANZ equivalents.
- For accessing a consumer's own accounts/transactions you need CDR accreditation
  (OAuth2/OIDC/FAPI, see `authentication/suncorp-bank-authentication.yml`); that is
  out of scope for this public skill.
