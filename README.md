# ATTOM (attom-data)

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

ATTOM Data Solutions is a national property, real estate, and location data provider that curates a multi-sourced warehouse of data on 158+ million U.S. properties. The ATTOM API (also delivered as ATTOM Cloud) exposes that data over REST as a family of logical resources - property characteristics, tax assessments, automated valuations (AVM), sales and deed history, mortgage records, area and boundary geographies, schools, community and neighborhood data, points of interest, transportation noise, all-event snapshots, and home equity - queried by address, APN/FIPS, ATTOM ID, radius, or geoIdV4 and authenticated with an API key sent in the `apikey` header.

All endpoints are served from the gateway host `https://api.gateway.attomdata.com`. Classic Property API resources use the pattern `/propertyapi/v1.0.0/{resource}/{package}`; version 4 endpoints use `/v4/{resource}`; area geographies use `/areaapi/v2.0.0/`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/attom-data/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/attom-data/refs/heads/main/apis.yml)

## Tags

- Property Data
- Real Estate
- Location Data
- Valuation
- AVM
- Assessment
- Mortgage
- Neighborhood

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### ATTOM Property API

Core property characteristics for a single property or a list of properties, queried by address, APN/FIPS, ATTOM ID, or radius. Includes the basic profile, detail, expanded profile, id, address, snapshot, and detail-with-owner packages returning building, lot, location, and ownership attributes.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Assessment API

County tax assessment data - assessed and market values, tax amounts, exemptions, and the assessment history for a property, via the assessment detail, assessment snapshot, and assessment history packages.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM AVM & Valuation API

Automated Valuation Model estimates for a property, including the ATTOM AVM detail, AVM snapshot, AVM history, and rental AVM packages, returning an estimated value with a confidence score and high/low value range.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Sales & Deed API

Recorded sale and deed transactions plus multi-year sales history and sales trends - sale detail, sale snapshot, sales history (basic/expanded), and aggregated sales-trend counts and average/median prices by area and interval.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Mortgage API

Property records enriched with mortgage and lender information via the detail-with-mortgage and detail-with-mortgage-and-owner packages, returning loan amounts, lenders, loan types, and recording dates alongside owner details.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Area & Boundary API

Geography services that resolve and describe ATTOM area codes - geoId/geoIdV4 lookups by name and geography type, area hierarchy lookups, location lookups, and boundary geometry returned in GeoJSON for counties, places, neighborhoods, school districts, and ZIP code tabulation areas.

- **Human URL:** [https://cloud-help.attomdata.com/article/612-attom-api-v4](https://cloud-help.attomdata.com/article/612-attom-api-v4)
- **Base URL:** `https://api.gateway.attomdata.com/areaapi/v2.0.0`

### ATTOM School API

School and school-district data - search schools near a location or attendance zone, retrieve an individual school profile with ratings and enrollment, get district details, and attach school attendance zones to a property via the detail-with-schools package.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Community & Neighborhood API

Neighborhood and community context for a place or geoIdV4 - climate, crime, demographics, natural hazards, education, commute, and quality-of-life indicators returned by the v4 community endpoint.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/v4`

### ATTOM POI API

Points-of-interest search returning nearby businesses and amenities - grocery, dining, schools, parks, healthcare, and more - within a radius or area, plus a POI category lookup for the supported business categories.

- **Human URL:** [https://cloud-help.attomdata.com/article/641-upgrading-to-poi-endpoint-v4](https://cloud-help.attomdata.com/article/641-upgrading-to-poi-endpoint-v4)
- **Base URL:** `https://api.gateway.attomdata.com/v4`

### ATTOM Transportation Noise API

Modeled transportation-noise scores for a location, estimating noise exposure from road, rail, and air traffic at a set of coordinates or for a property.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com`

### ATTOM AllEvents & Snapshot API

A consolidated view of every event on a property - assessment, AVM, sale, deed, and mortgage - in a single call via the allevents detail and snapshot packages, ideal for building a full property timeline.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

### ATTOM Home Equity API

Estimated home equity for a property, combining the AVM value with outstanding mortgage balances to return an estimated equity position and loan-to-value indication via the valuation home-equity package.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

## Authentication

All requests require an ATTOM API key passed in the `apikey` HTTP header, plus an `Accept: application/json` (or `application/xml`) header. Keys are issued via the 30-day free trial at cloud.attomdata.com or through a paid subscription.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/attom-data-solutions)
- [Website](https://www.attomdata.com)
- [Documentation](https://api.developer.attomdata.com/docs)
- [Plans](plans/attom-data-plans-pricing.yml)
- [Rate Limits](rate-limits/attom-data-rate-limits.yml)
- [Fin Ops](finops/attom-data-finops.yml)

## Artifacts

- [OpenAPI](openapi/attom-data-openapi.yml)
- [Postman Collection](collections/attom-data.postman_collection.json)
- [Open Collection](collections/attom-data.opencollection.json)

## Review

A review of whether ATTOM exposes a documented public WebSocket API concluded **no** - ATTOM's entire public API surface is synchronous request/response REST over HTTPS. See [review.yml](review.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
