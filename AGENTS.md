# Netflix EDA — Agent Instructions

## Project purpose

Maintain a reproducible, readable portfolio analysis of the supplied historical
Netflix catalog. The project owner is learning data analytics. Explain substantive
corrections, the reason for them, and the important implementation choices.

## Scope and structure

- Keep the main submission in `notebooks/Netflix_Submission.ipynb`.
- Keep `notebooks/Netflix_EDA.ipynb` as the secondary AI-assisted reference.
- Preserve both notebooks' contents and saved outputs during organizational or
  documentation changes. Do not rewrite or rerun them merely to categorize files.
- Keep the source in `data/netflix.csv`; never alter the original CSV. Preserve
  the identical root `netflix.csv` compatibility copy because the main submission
  reads that public URL. The secondary notebook reads the local `data/` copy.
- Export the six README charts into `images/` from the secondary notebook itself.
  Attribute those figures and enhanced methods to that notebook in the README.
- Keep setup instructions and verified direct dependencies current.
- Prefer straightforward Pandas code and the existing libraries. Add folders,
  abstractions, or dependencies only when there is a concrete need.

## Analysis rules

- Preserve substantive existing analysis. Explain any removal or correction.
- Use `show_id` as the title key; validate joins and relationship-table grain.
- Distinguish unique-title counts from title–attribute relationship counts.
- Label denominators, overlapping categories, missing metadata, incomplete
  periods, and exclusions wherever they affect interpretation.
- Treat the dataset as historical. Catalog presence is not evidence of current
  availability, popularity, profitability, or causal business impact.
- Use relative project paths, deterministic previews, and bounded outputs.
- Keep figures readable with descriptive titles, units, and explicit scope.
- Inspect extreme values before deciding whether to correct or exclude them.

## Validation

- Run the notebook from top to bottom after substantive code changes.
- Reconcile the README's claims with executed outputs.
- Verify the CSV hash remains unchanged when moving or repackaging it.
- Inspect exported charts and check README links before handoff.
- If execution or publishing is blocked, describe the blocker accurately; do not
  claim that unrun code passed or local changes are already live on GitHub.
