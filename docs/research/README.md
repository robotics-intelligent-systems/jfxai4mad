# Research Index

This directory is the landing page for research-oriented documentation. The 33 previously migrated English Markdown notes remain at `docs/` root in this refactor so historical links and the migration register stay stable. New research documents should be created under thematic subdirectories rather than added to the root.

## Current thematic groups

- [Tourism and mobility](../README.md#tourism-and-mobility)
- [Destination weddings, education and professional development](../README.md#destination-weddings-education-and-professional-development)
- [Platforms and market analysis](../README.md#platforms-and-market-analysis)
- [Adult relationships, consent and wellbeing](../README.md#adult-relationships-consent-and-wellbeing)
- [Adult sex-work, demography and legal context](../README.md#adult-sex-work-demography-and-legal-context)
- [Child protection](../README.md#child-protection)

## Recommended future structure

```text
docs/research/
├── tourism/
├── platforms/
├── adult-relationships/
├── legal-socioeconomic/
└── child-protection/
```

When a future migration moves an existing research note into these subdirectories, update both `docs/README.md` and `docs/ANNEX-DOCS-CONSOLIDATED.md` in the same PR so no repository-local links are left stale.
