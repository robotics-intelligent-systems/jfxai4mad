# GitHub Open-Source B2B Market Sizing and ROI

**Status:** planning framework; no market count, lead volume or conversion rate has been validated for JFXAI4MAD.

This note consolidates two supplemental Spanish drafts about GitHub’s potential as a source of technical collaborators and B2B opportunities. It replaces platform-wide user counts and unsupported funnel percentages with a dated platform indicator, an organization-level market model and a measurable pilot.

## What the available platform data can and cannot show

GitHub’s 2025 Octoverse report says more than 180 million developers use GitHub. That is a platform-scale context figure, not a count of active monthly users, organizations with a relevant need, buyers, or people willing to be contacted. It cannot serve as JFXAI4MAD’s TAM, SAM, SOM or sales forecast. The report’s project and repository totals likewise do not identify purchasing organizations.

The source drafts’ estimates of 225 million accounts, four million organizations, 45–50 million monthly active developers, or 900,000–2.5 million people in an aeronautics/STEM niche do not include traceable definitions, dates or denominators. They are not used here. The inherited 0.1–1% and 2–5% market-fit assumptions are also unsupported and should not be multiplied into a platform total.

## Separate buyers from the open-source community

A maintainer’s or contributor’s public work can indicate technical relevance, a possible integration need, or an opportunity for reciprocal collaboration. It does not establish buying intent, authority to procure, permission for outreach, or consent to be added to a marketing list. Count buying organizations and open-source collaborators in separate cohorts and report any partnership outcomes separately from paid-customer conversions.

Use organization-level evidence to qualify a potential buyer:

- a documented technical or operational need that matches a deliverable in the portfolio;
- an active project, integration, issue or deployment context that supports the fit;
- a plausible organizational buyer and a procurement path, verified during conversation;
- ability to serve and contract in the organization’s jurisdiction; and
- an explicit response or opt-in before any ongoing follow-up.

For an initial study, California, Israel and Argentina can be tracked as separate market strata because they are current project priorities. Confirm service eligibility, applicable procurement and privacy rules, and actual organization-level fit before treating a location as addressable. Do not infer a person’s location from an avatar or other profile clues.

## TAM, SAM and SOM method

| Measure | Unit and calculation | Evidence needed |
| --- | --- | --- |
| TAM | Organizations with the defined need × plausible annual contract value (ACV) | A reproducible organization list, stated inclusion rules and a defensible ACV range |
| SAM | The TAM subset reachable with the current product, delivery capacity and eligible jurisdictions | Region, industry, language, procurement and product-fit filters, each dated |
| SOM | The SAM portion plausibly served in a stated period | Pilot results, qualified pipeline, sales capacity, delivery capacity and budget |

Do not substitute individual GitHub accounts for organizations in these calculations. If the organization count or ACV is unknown, report the range as “not yet estimated” rather than applying a percentage to GitHub’s global user total.

## Plus, GitHub data and capacity assumptions

ChatGPT Plus is an analysis tool, not a GitHub contact database and not a guaranteed monthly throughput quota. OpenAI describes plan access and usage limits as subject to change; the in-product counter shows available Deep Research tasks. The Plus subscription page lists USD 20 per month as of the review date below, and API usage is billed separately. A subscription price is one cost input; it does not establish how many profiles can be found, processed or contacted.

For reproducible discovery, use GitHub’s search/API capabilities to identify public organizations and repositories relevant to defined technical themes, then manually verify the organization-level evidence. GitHub applies rate limits, and search endpoints have separate, more restrictive limits than general REST requests; use current response headers and documentation when planning collection. Do not scrape personal contact data or automate bulk outreach. A public contribution is not authorization for marketing.

The inherited claims that Plus can process 10,000–50,000 profiles per month, qualify 15%, produce a 50% response rate, or convert 5–10% are not documented by the plan description or by a measured cohort. They are excluded as capacity and conversion forecasts.

## Pilot and measurement

A first batch of 100 organizations is a proposed manual research cohort, not a number Plus is expected to find. Select organizations against published inclusion rules; deduplicate by organization; and record the URL, evidence of fit, geography, review date, official business contact channel and outcome. Contact only through a relevant public organizational channel with a concise, truthful, value-first message. Respect refusals and stop follow-up when asked.

Track each stage with its own denominator:

| Stage | Example measure |
| --- | --- |
| Research | Unique organizations reviewed / organizations selected |
| Outreach | Delivered organization-level messages / organizations approved for outreach |
| Response | Replies and positive replies / delivered messages, reported separately |
| Discovery | Meetings held / positive replies |
| Qualification | Organizations with verified need, buyer and path to procure / meetings held |
| Commercial result | Signed paid pilots and collected revenue / qualified organizations |
| Partnership result | Opt-in integrations, joint work or accepted contributions, reported separately from sales |

Do not label a reply “hot,” a contribution “lead,” a proposal “customer,” or an unpaid collaboration as revenue. Report counts, dates, stage definitions and sample sizes; establish rates from this pilot before forecasting a larger funnel. Do not rank, filter or enrich people based on gender, age, appearance, relationship status or inferred intimate preferences. These attributes do not measure technical or commercial fit.

## ROI calculation

Use realized incremental gross profit attributable to the pilot, not profile counts or proposed contract value alone:

**ROI (%) = (attributable incremental gross profit − total pilot/acquisition cost) ÷ total pilot/acquisition cost × 100**

Include research and outreach labor, subscription and API charges, data or event costs, and other direct acquisition expenses. Track signed contracts, recognized revenue, collected cash and unpaid collaboration separately. If the total cost is zero or unknown, ROI is not yet calculable.

Illustration only: one paid customer produces USD 2,000 of incremental gross profit and the full pilot costs USD 500; ROI is 300%. This is arithmetic, not an estimate of the chance of finding or converting a customer. A three-month Plus subscription at the listed USD 20 monthly price would be USD 60 before tax; add it to the pilot cost, but also count the human time and all other expenses.

## Sources and review date

Reviewed 17 October 2026. Platform totals, plan features, prices and API limits can change; recheck the official pages before budgeting or operational use.

- GitHub, [Octoverse 2025](https://github.blog/news-insights/octoverse/octoverse-a-new-developer-joins-github-every-second-as-ai-leads-typescript-to-1/) — dated developer-scale context.
- GitHub Docs, [REST API rate limits](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api) — current API and search-limit guidance.
- OpenAI Help Center, [What is ChatGPT Plus?](https://help.openai.com/en/articles/6950777-what-is-chatgpt-free-plan) — plan scope, variable usage limits and separate API billing.
- OpenAI Help Center, [Deep research in ChatGPT](https://help.openai.com/en/articles/10500283-deep-research-in-chatgpt) — plan-dependent usage and in-product counter.

## Source migration record

Both Spanish TXT files were added in the same baseline commit. Their immutable GitHub links, Git blob IDs and SHA-256 digests are recorded below; the working copies are removed after this English replacement and its indexes are complete.

| Original source | Baseline commit | Git blob | SHA-256 |
| --- | --- | --- | --- |
| [Para sdk2035 y la organización.txt](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/97ae9548077106ac1af278876aaf2330f2d83fe7/docs/Para%20sdk2035%20y%20la%20organizaci%C3%B3n.txt) | 97ae9548077106ac1af278876aaf2330f2d83fe7 | 2f4a5a030b8e219f707013f883025182ff8be0a8 | d9b5ec7357593975639c9dc40cafd8d904e4420c18ed336f98ddc6a12938d274 |
| [Para estimar el potencial.txt](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/97ae9548077106ac1af278876aaf2330f2d83fe7/docs/Para%20estimar%20el%20potencial.txt) | 97ae9548077106ac1af278876aaf2330f2d83fe7 | 0a044eb7464a2297be6fee746a0924a41b6fc611 | 233173e20cada759c9b3fab5d9c818fbe268c00f60290ddb05a80f35d9fb89f0 |

## Related documents

- [Business model and performance indicators](business-model-and-kpis.md)
- [LinkedIn contact acquisition and lead velocity](linkedin-contact-acquisition-and-lead-velocity.md)
- [Requirements and consent model](../product/requirements-and-consent.md)

No contact list was collected, no individual was profiled, and no outreach or conversion test was performed as part of this documentation migration.
