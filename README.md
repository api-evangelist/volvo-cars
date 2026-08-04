# Volvo Cars (volvo-cars)

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

Volvo Cars is a Swedish premium automotive OEM (headquartered in Gothenburg, owned by Geely) that operates the Volvo Cars Developer Portal as the public face of its connected-vehicle platform. The portal exposes the Connected Vehicle API, Energy API, Energy Device API, and Location API for third-party developers to build applications around real Volvo cars equipped with Volvo On Call or Google Built-In. APIs use OAuth 2.0 against Volvo ID with explicit owner consent, a VCC-API-Key client identifier, and a free tier capped at 10,000 calls per day per app. The portal also covers Android Automotive in-car app development with an official XC40 Recharge emulator, 3D assets and simulator resources, and an active open-source program at github.com/volvo-cars.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/volvo-cars/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Automotive, Connected Vehicle, Electric Vehicles, Telematics, Android Automotive, OEM, Mobility

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Volvo Cars Connected Vehicle API
Receive vehicle data and send commands to the vehicle. Vehicle data covers status, diagnostics, statistics, and metadata — odometer, fuel amount, tyre pressures, brake status, engine status, window status, warnings, environment values. Commands include lock/unlock, climate start/stop, flash lights, sound horn, and engine start/stop, with a `list-commands` endpoint to discover what a given vehicle supports. Available on Volvo On Call vehicles (MY 2010-2024) and Google Built-In vehicles (MY 2020+).

**Human URL:** [https://developer.volvocars.com/apis/connected-vehicle/v2/overview/](https://developer.volvocars.com/apis/connected-vehicle/v2/overview/)
**Base URL:** `https://api.volvocars.com/connected-vehicle/v2`

- [Documentation](https://developer.volvocars.com/apis/connected-vehicle/v2/overview/)
- [OpenAPI](https://developer.volvocars.com/apis/connected-vehicle/v2/specification/)
- [Endpoints](https://developer.volvocars.com/apis/connected-vehicle/v2/endpoints/)
- [Code Examples — Connected Vehicle Fetch Sample](https://github.com/volvo-cars/developer-portal-api-samples/tree/main/connected-vehicle-fetch-sample)

### Volvo Cars Energy API
Latest energy state for BEV and PHEV models: battery charge level, target battery charge level, charging connection status, charging system status, charging type, charging power, charger power status, charging current limit, estimated charging time, and electric range. Includes a capabilities endpoint that reports per-vehicle support. Supported models include EC40/C40, EX40/XC40 BEV, EX30, and the PHEV lineup (XC60/S90/V90 PHEV MY 2022+, XC90/S60/V60 PHEV MY 2023+, plus XC40 PHEV).

**Human URL:** [https://developer.volvocars.com/apis/energy/v2/overview/](https://developer.volvocars.com/apis/energy/v2/overview/)
**Base URL:** `https://api.volvocars.com/energy/v2`

- [Documentation](https://developer.volvocars.com/apis/energy/v2/overview/)
- [OpenAPI](https://developer.volvocars.com/apis/energy/v2/specification/)

### Volvo Cars Location API
Detailed information on a vehicle's current location, intended for interactive applications. Same OAuth flow, VCC-API-Key, and rate-limit profile as Connected Vehicle and Energy.

**Human URL:** [https://developer.volvocars.com/apis/location/v1/overview/](https://developer.volvocars.com/apis/location/v1/overview/)
**Base URL:** `https://api.volvocars.com/location/v1`

- [Documentation](https://developer.volvocars.com/apis/location/v1/overview/)
- [OpenAPI](https://developer.volvocars.com/apis/location/v1/specification/)
- [Endpoints](https://developer.volvocars.com/apis/location/v1/endpoints/)

### Volvo Cars Energy Device API
The device-side counterpart to the vehicle-side Energy API — manage wallboxes, charging sessions, and user ID tokens for end-to-end charging integrations.

**Human URL:** [https://developer.volvocars.com/apis/energy-device-api/v1/overview/](https://developer.volvocars.com/apis/energy-device-api/v1/overview/)

- [Documentation](https://developer.volvocars.com/apis/energy-device-api/v1/overview/)
- [Endpoints](https://developer.volvocars.com/apis/energy-device-api/v1/endpoints/)

## Authentication

- **OAuth 2.0 Authorization Code Flow** against Volvo ID. Explicit consent from the vehicle owner is required before an application can access their data. Test credentials are automatic; production credentials are granted after Volvo Cars manually reviews and publishes the app (typically 14-21 days).
- **VCC-API-Key** header — the application's primary client identifier, required on every request alongside the OAuth bearer token.

## Pricing

All APIs are free to use under the [APIs Terms and Conditions](https://developer.volvocars.com/terms-and-conditions/apis-terms-and-conditions/) (last updated 2026-01-27). Volvo Cars expressly reserves the right to introduce paid tiers in the future.

## Rate Limits

| Surface | Limit |
|---|---|
| Connected Vehicle API (read) | 100 req/min per Volvo ID + Client ID |
| Connected Vehicle API (commands) | 10 req/min per Volvo ID + Client ID |
| Energy API | 100 req/min per Volvo ID + Client ID |
| Location API | 100 req/min per Volvo ID + Client ID |
| Per-app daily cap (all APIs) | 10,000 calls / day (higher available on request) |

Exceeding a limit returns HTTP `429`.

## Regional Availability

- **Test:** demo Volvo IDs work globally.
- **Production:** Europe / Middle East / Africa and US / Canada / Latin America. Other regions are not yet supported.

## Developer Resources

- [Volvo Cars Developer Portal](https://developer.volvocars.com/)
- [APIs Overview](https://developer.volvocars.com/apis/)
- [Getting Started](https://developer.volvocars.com/apis/docs/getting-started/)
- [Authorisation](https://developer.volvocars.com/apis/docs/authorisation/)
- [Test Access Tokens](https://developer.volvocars.com/apis/docs/test-access-tokens/)
- [Observability](https://developer.volvocars.com/apis/docs/observability/)
- [In-Car Apps (Android Automotive)](https://developer.volvocars.com/in-car-apps/)
- [Volvo XC40 Recharge Android Automotive Emulator](https://developer.volvocars.com/in-car-apps/android-emulator-xc40/)
- [3D Assets and Simulator](https://developer.volvocars.com/3d/)
- [Open Source](https://developer.volvocars.com/open-source/)
- [News](https://developer.volvocars.com/news/)
- [Supported Locations](https://developer.volvocars.com/terms-and-conditions/apis-supported-locations/)
- [APIs Terms and Conditions](https://developer.volvocars.com/terms-and-conditions/apis-terms-and-conditions/)

## GitHub

[github.com/volvo-cars](https://github.com/volvo-cars) hosts the official Volvo Cars open-source program. Notable repos:

- [`developer-portal-api-samples`](https://github.com/volvo-cars/developer-portal-api-samples) — OAuth2 code flow and Connected Vehicle fetch samples (Node.js).
- [`automotive-media-sample`](https://github.com/volvo-cars/automotive-media-sample) — sample media application for Android Automotive.
- [`web-platform-examples`](https://github.com/volvo-cars/web-platform-examples) — jump-start examples for app development.
- [`sample-android-automotive-wearable-monitoring`](https://github.com/volvo-cars/sample-android-automotive-wearable-monitoring) — Android Automotive + wearables sample.
- [`coppercomm`](https://github.com/volvo-cars/coppercomm), [`remoteperf`](https://github.com/volvo-cars/remoteperf), [`pkcs11-utils`](https://github.com/volvo-cars/pkcs11-utils) — engineering tooling open-sourced by Volvo Cars teams.

## Support

- Developer Portal: developer.portal@volvocars.com
- Open Source Program Office: opensource@volvocars.com

## Maintainer

- **FN:** Kin Lane
- **Email:** info@apievangelist.com
- **X:** [@apievangelist](https://twitter.com/apievangelist)
- **URL:** [apievangelist.com](https://apievangelist.com)

specificationVersion: 0.16
