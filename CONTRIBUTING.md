# Contributing

This is a vendor neutral list of Copilot rank tracking tools, sorted by whether each one is built for a Microsoft tenant or for a single login watching the public chat. Corrections and additions are welcome.

## Edit the data, not the table

1. Edit [tools.yaml](tools.yaml). Fields: `name`, `url` (optional), `copilot_coverage`, `enterprise_fit`, `price_from`, `best_for`.
2. Run `python render_table.py --write` to regenerate the block between the `<!-- TABLE:START -->` and `<!-- TABLE:END -->` markers.
3. Open a PR and link a source for any pricing, coverage, or enterprise feature claim.

## What gets merged

- `copilot_coverage` stated honestly. If Copilot sits behind a beta flag or a higher tier, say so.
- `enterprise_fit` backed by something checkable: SSO, an admin console, seat based reporting, a documented API. Not a marketing adjective.
- Real pricing, with the currency and tier named. Trials stated as trials, not as free plans.

## What gets rejected

- Affiliate links. Vendor domain only.
- Duplicate rows. Update the existing entry.
- Adjectives in `best_for`. Name the buyer and the job.

## Setup

```bash
pip install pyyaml
python render_table.py          # preview
python render_table.py --write  # write into README.md
```
