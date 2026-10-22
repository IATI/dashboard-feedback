# IATI Data Quality Framework — consultation

This repository collects feedback on the **draft IATI Data Quality Framework**,
which is being used to assess the quality of the data organisations publish to
IATI.

**Comments are open until 17 November 2026.**

## How to comment

Each part of the framework has its own issue, so that comments stay attached to
the thing they are about:

- one issue for each of the **11 components** of the four dimensions —
  availability, timeliness, coverage and comprehensiveness
- one issue for each of the **33 indicators** that make up those components

[Browse the issues](../../issues) and comment on the ones you have a view on.
You do not need to comment on all of them, and you are welcome to comment on
only your own area of interest.

Each issue describes what is being measured, the specific tests behind it, and
any caveats that are still unresolved. Useful things to tell us:

- whether what is being measured is reasonable to expect of publishers
- whether the tests are a fair way of measuring it
- whether the thresholds for **Good**, **Very good** and **Excellent** are set at
  the right level
- whether an indicator should apply to every organisation, or whether there are
  organisation types it should not apply to

Comments are public. You will need a free
[GitHub account](https://github.com/signup).

## Before you comment

The dashboard explains how an assessment is reached, lists every indicator and
its thresholds, and flags what is still provisional:

- **[How the assessment works](https://preview-dashboard.iatistandard.org/about)**
- [Reimagining Data Quality: A User Centric Approach — Proposal for Consultation](https://connect.iatistandard.org/post/reimagining-data-quality-consultation-new-metrics-and-dashbaord-13842373)

Organisations publishing to IATI can also sign in to the dashboard to see their
own preliminary assessment.

## If you cannot use GitHub

If you would rather not use GitHub, want to share feedback privately, or have a
question rather than a comment, email **support@iatistandard.org**.

## What happens next

Feedback will be reviewed and used to finalise the framework — the indicators,
the thresholds and the weightings — before the dashboard is published. A
snapshot of the final assessments will feed into IATI's State of the Data
report, and publishers will be consulted on that before it is published.

## For maintainers

The issues in this repository are generated rather than written by hand, so that
they say the same thing as the dashboard. The generator lives in the dashboard
frontend repository, at `scripts/consultation/`:

```sh
python3 scripts/consultation/generate_issues.py   # build the issue texts
python3 scripts/consultation/post_issues.py       # dry run — shows what would be posted
python3 scripts/consultation/post_issues.py --post
```

It skips any issue whose title already exists, so it is safe to re-run. It does
not update issues that have already been posted: if wording changes after an
issue exists, edit that issue here.
