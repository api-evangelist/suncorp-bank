# Suncorp Bank (suncorp-bank)

Suncorp Bank is an Australian retail and business bank headquartered in Brisbane, Queensland, offering transaction and savings accounts, home and personal lending, credit cards, and business banking. Formerly the banking arm of Suncorp Group, it was acquired by Australia and New Zealand Banking Group (ANZ) on 31 July 2024 and now operates as a division of ANZ while retaining the Suncorp Bank brand under a multi-year transition. As an authorised deposit-taking institution (ADI) it is a data holder under Australia's Consumer Data Right (CDR / Open Banking) and exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Consumer Data Standards, powered by the Frollo PRD portal.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/suncorp-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/suncorp-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Product Reference Data
- Consumer Data Right

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Suncorp Bank CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data API exposing Suncorp Bank's currently offered banking products (transaction, deposit, mortgage, personal lending, credit card and business lending) per the Australian Consumer Data Standards. GET /banking/products and /banking/products/{productId} return REST/JSON with an x-v version header (live at x-v 5, 26 products at time of review). No credentials required. Powered by the Frollo PRD portal.

- **Human URL:** [https://www.suncorpbank.com.au/help-support/open-banking.html](https://www.suncorpbank.com.au/help-support/open-banking.html)
- **Base URL:** `https://id-ob.suncorpbank.com.au/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Public

#### Properties

- [Documentation](https://www.suncorpbank.com.au/help-support/open-banking.html)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#consumer-data-standards-banking-apis)
- [OpenAPI](openapi/suncorp-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.suncorpbank.com.au/)
- [Developer Portal](https://www.suncorpbank.com.au/help-support/open-banking.html)
- [Documentation](https://consumerdatastandardsaustralia.github.io/standards/)
- [GitHub Organization](https://github.com/suncorp)
- [LinkedIn](https://www.linkedin.com/company/suncorp/)
- [Privacy Policy](https://www.suncorpbank.com.au/about-us/legal/privacy.html)
- [Terms of Service](https://www.suncorpbank.com.au/about-us/legal.html)
- [Support](https://www.suncorpbank.com.au/help-support/open-banking.html)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
