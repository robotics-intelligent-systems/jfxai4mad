# Research Index

This directory is the landing page for research-oriented documentation. The 33 previously migrated English Markdown notes remain at `docs/` root in this refactor so historical links and the migration register stay stable. New research documents should be created under thematic subdirectories rather than added to the root.

## Consolidated origin-market research

[Inbound tourism origin-market research](tourism/inbound-origin-market-research.md)
combines three additional drafts into one English note covering 14 destinations.
It retains the draft origin/driver pairs as hypotheses and includes a Mermaid
validation workflow. No current tourism ranking or visa/route claim is verified
by the documentation migration.

## Sport fishing and hunting tourism

[Sport fishing and hunting tourism](tourism/sport-fishing-and-hunting-tourism.md) consolidates three additional Spanish drafts. It retains four fishing and three hunting destination groups, distinguishes unverified spending and conservation claims, and replaces the plaintext comparison with a table and Mermaid research workflow.

## Marriage-conversion research

[Match Group and peer marriage-conversion research](platforms/match-group-and-peer-marriage-conversion.md) translates the additional comparison of Tinder, Badoo, OkCupid and Mutual. It corrects corporate scope, preserves qualitative labels as unsupported source opinions, and adds cohort definitions and a Mermaid evidence workflow.

## Current thematic groups

- [Tourism and mobility](../README.md#tourism-and-mobility)
- [Destination weddings, education and professional development](../README.md#destination-weddings-education-and-professional-development)
- [Platforms and market analysis](../README.md#platforms-and-market-analysis)
- [Adult relationships, consent and wellbeing](../README.md#adult-relationships-consent-and-wellbeing)
- [Adult sex-work, demography and legal context](../README.md#adult-sex-work-demography-and-legal-context)
- [Child protection](../README.md#child-protection)

## Current and recommended structure

```text
docs/research/
├── tourism/
│   ├── inbound-origin-market-research.md
│   └── sport-fishing-and-hunting-tourism.md
├── platforms/
│   └── match-group-and-peer-marriage-conversion.md
├── adult-relationships/
├── legal-socioeconomic/
└── child-protection/
```

`tourism/` and `platforms/` contain migrated research; the other thematic directories remain recommendations.

When a future migration moves an existing research note into these subdirectories, update both `docs/README.md` and `docs/ANNEX-DOCS-CONSOLIDATED.md` in the same PR so no repository-local links are left stale.
