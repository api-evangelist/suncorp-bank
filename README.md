# Suncorp Bank (suncorp-bank)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
