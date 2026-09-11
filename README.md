# cloud-itonami-lei-635400iuizziujsamf76

> **Independent third-party archive/analysis. Not affiliated with, endorsed by, or sponsored by Fortum Oyj.**

This repository archives the publicly published Privacy Policy of **Fortum Oyj** (FI), with source-url and retrieval-date provenance, per
ADR-2607110300 (`cloud-itonami-lei-corporate-tos-catalog`, `com-junkawasaki/root`).
Read-only reference/archive repository — not a governed Advisor/Governor actor.

- LEI: `635400IUIZZIUJSAMF76` (GLEIF entity status ACTIVE, registration ISSUED)
- Source: https://www.fortum.com/legal/privacy
- Retrieved: 2026-07-25T05:18:14Z
- SHA-256 of archived text: `a44adc86faad4953bd8c8758bcc6b24f4b186c883eaef5a53294b5dff082b781`

Acquired by `scripts/lei-acquire.cljs` as part of the worldwide-broadening
continuation that followed the 2026-07-25 coverage audit, which found the
catalog's real reach was 27 countries with the United States at 55%.

## Verified register citations

`facts/catalog.edn` records what public registers say about this legal entity,
with one citation per claim. It is not prose about the company — every row names
a URL and a substring that must still be present in the response.

```bash
nbb tools/verify_citations.cljk facts/catalog.edn --min 15
```

Exit codes are three-valued on purpose, so a check that could not run never
looks like a check that passed:

| exit | meaning |
|---|---|
| 0 | every citation fetched, every claim substring still present |
| 1 | drift — a URL answered but no longer carries its claim, or returned non-2xx |
| 2 | could not answer — missing/unparseable catalog, zero entries, or below `--min` |

Measured 2026-08-20: 19/19 citations pass. The gate was confirmed to
discriminate — a broken URL and an altered claim substring each exit 1 naming
the offending row, and floor/empty/parse failures each exit 2.

Sources that were retrieved and **rejected** are kept in `:catalog/rejected`
with the reason, so a later pass does not re-add them believing they were
merely overlooked.
