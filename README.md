# SMSRoute Open Datasets

Open, dated snapshots of SMS pricing and sender-ID registration rules, published as
machine-readable JSON. Free to reuse under the MIT license (see `LICENSE`).

## What's here

| File | Description |
|---|---|
| `data/prices-2026-07-26.json` | Published per-destination SMS rates (with competitor comparison columns, as published) |
| `data/sender-id-rules.json` | Alphanumeric sender-ID / registration regime summaries for 40 countries |

## Update cadence

Snapshots are dated and refreshed roughly weekly. Each file carries an `as_of` /
`dataset_version` field — check that before assuming freshness. This repo is a periodic
export, not a live feed.

## Canonical / live sources

- Live JSON (same data, always current): https://smsroute-cc.github.io/api/v1/
- OpenAPI description of the live endpoints: https://smsroute-cc.github.io/api/v1/openapi.yaml
- Human-readable published price page: https://smsroute.cc/prices

## Provenance

- `prices-2026-07-26.json`: our own published outbound SMS rates, parsed from
  https://www.smsroute.cc/prices on 2026-07-25. Competitor columns (Twilio, Vonage,
  MessageBird) are as publicly published on that same page at capture time — not
  independently re-verified against each provider's own pricing pages, and may lag
  their live rates.
- `sender-id-rules.json`: public, well-documented sender-ID and alphanumeric-registration
  regimes compiled from carrier/regulator practice (CTIA, TRAI DLT, KISA, İYS, ACMA,
  etc. — see the `basis` field per row). Regulatory summaries, not legal advice.

## Machine-readable pointers

Both files are also served live (not just as periodic exports here) at:
- https://smsroute-cc.github.io/api/v1/prices.json
- https://smsroute-cc.github.io/tools/sender-id-rules.json

A `Dataset` JSON-LD description (schema.org) is embedded at
https://smsroute-cc.github.io/api/v1/index.html for discovery by search engines and
AI assistants.

## License

MIT — see [LICENSE](LICENSE). Please attribute "SMSRoute" and link back to
https://smsroute.cc when reusing.

## Related: Sender-ID Regulations Dataset
Verified alphanumeric sender-ID rules, registration regimes and charset classes for 40 countries (JSON/CSV, CC-BY-4.0): [sms-sender-id-regulations](https://github.com/SMSRoute-cc/sms-sender-id-regulations)
