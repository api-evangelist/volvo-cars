# Volvo Cars (volvo-cars)
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
