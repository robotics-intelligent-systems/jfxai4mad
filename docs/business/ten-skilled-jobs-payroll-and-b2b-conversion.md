# Ten Skilled Jobs: Payroll Funding and B2B Conversion Scenario

English translation and consolidation of the additional Spanish source note. **Status:** hypothetical planning scenario; salary costs, network size, conversion rates and market assertions are unverified source assumptions. Arithmetic corrections below do not validate commercial feasibility.

## 1. Annual financial requirement

The source proposes sustaining ten skilled jobs in software engineering, MLOps, B2B sales or infrastructure support in Argentina or California. It estimates payroll first, then designs a sales funnel from 30,000 LinkedIn contacts.

| Indicator | Argentina: ten jobs | California: ten jobs |
| --- | ---: | ---: |
| Average annual employee cost, gross pay plus employer charges | USD 30,000 | USD 180,000 |
| Annual payroll | USD 300,000 | USD 1,800,000 |
| Average SME cloud/AI SaaS subscription | USD 300/month; USD 3,600/year | USD 300/month; USD 3,600/year |
| Active annual subscriptions needed for payroll-only revenue equivalence | 84 | 500 |

The ceiling of payroll divided by USD 3,600 is 84 or 500. These counts assume full-year subscriptions and revenue entirely available for payroll. Hosting, support, acquisition, taxes, payment costs, churn and other overhead are excluded; ARR is not cash collected or payroll funding.

## 2. From 30,000 contacts to paying customers

For Brazil and India, the source positions the offering around high integrity and low cost. Its description of the following rates as standard B2B outbound/LinkedIn rates has no supporting dataset.

| Funnel stage | Assumed stage conversion | Source count | Exact modeled count |
| --- | ---: | ---: | ---: |
| LinkedIn universe | 100% | 30,000 | 30,000 |
| Connection acceptance or initial response | 15% | 4,500 | 4,500 |
| Qualified leads, described as MQL/SQL | 10% of responses | 450 | 450 |
| Proofs of concept or demos | 25% of SQLs | 112 | 112.5 |
| Closed paying customers | 20–30% of demos | 22–34 | 22.5–33.75 |

Fractional counts are expected values; the source's 22–34 range is an approximate scenario. Overall modeled conversion is 0.075–0.1125%. Connection acceptance and a response are different events, as are MQL and SQL; an operational funnel needs separate definitions and observed cohorts.

## 3. Market allocation

The source argues that approximately 30 customers yield USD 108,000 ARR, leaving a gap against either payroll scenario. It allocates contacts to two markets:

| Market | Share | Contacts | Proposed segment | Source customers | ARR at USD 300/month |
| --- | ---: | ---: | --- | ---: | ---: |
| India | 60% | 18,000 | CTOs, DevOps leads and startup founders in Bangalore, Hyderabad and Pune | About 20 | USD 72,000 |
| Brazil | 40% | 12,000 | Heads of IT and fintech firms in São Paulo, Rio de Janeiro and Florianópolis | About 12 | USD 43,200 |
| Total | 100% | 30,000 | B2B cloud/AI prospects | About 32 | USD 115,200 |

**India — volume strategy.** The source describes India as having the largest ecosystem of technology SMEs and AI startups seeking inexpensive AWS/GCP alternatives. This comparative market claim is unverified.

**Brazil — higher average revenue per user (ARPU).** The source proposes lower time-zone/cultural friction with the Americas and greater willingness to pay USD 400–600/month. These remain hypotheses. Its USD 43,200 Brazilian ARR uses USD 300/month, not the higher proposed price. At USD 400–600, twelve full-year customers would instead yield USD 57,600–86,400, and combined ARR would be USD 129,600–158,400.

The 20/12 customer split implies approximately 0.1111% and 0.1% conversion. It is a separate source scenario, not an observed result or a necessary consequence of the aggregate funnel.

## 4. Payroll coverage and funding gap

Using the source's base-price USD 115,200 ARR:

| Scenario | Payroll | Gross revenue/payroll ratio | Payroll-equivalent jobs | Annual gap before operating costs |
| --- | ---: | ---: | ---: | ---: |
| Argentina | USD 300,000 | 38.4% | 3.84 | USD 184,800 |
| California | USD 1,800,000 | 6.4% | 0.64 | USD 1,684,800 |

The source summarizes these as approximately 38% and three to four jobs in Argentina, versus approximately 6% and fewer than one job in California. It proposes product-led growth (PLG) or a second funnel for Argentina, and enterprise sales or capital for California.

These are gross revenue comparisons. Funding coverage requires cash timing and contribution margin after delivery costs; no margin or working-capital model is supplied.

## 5. Reorganized action proposal

1. **Algorithmic trading and open banking:** the source proposes using surplus financing from the [value-architecture model](value-architecture-and-financing.md) to bridge Argentina's first-year payroll gap, moving from roughly 38% to full coverage. No surplus, committed capital or returns are evidenced.
2. **Turn outbound into product-led growth:** invite the 30,000 contacts to the open-source/GitHub community as well as to direct sales. The source proposes a freemium converter to raise overall conversion from 0.1% to 0.3%, targeting 84 customers. Arithmetic clarification: 0.3% of 30,000 is 90 customers and USD 324,000 ARR; 84 customers require 0.28% and yield USD 302,400 ARR. Conversion uplift is unverified.
3. **Hiring sequence:** the source proposes initially placing all ten jobs in Argentina or remote Latin America, then progressively moving leadership/sales roles to California as India/Brazil sales approach 500 customers. Five hundred customers at the base price yield USD 1.8 million ARR, still before operating costs. Hiring and relocation remain proposals requiring funded runway and updated employment-cost estimates.

## Consolidation and proposed measurements

The later [regional-hub revision](regional-hiring-hubs-and-market-distribution.md) proposes twenty jobs in Argentina and Türkiye and six target countries. Its USD 600,000 payroll and USD 108,000–133,200 ARR are a separate scenario; this note preserves the earlier ten-job comparison.

The [contact-acquisition timeline](linkedin-contact-acquisition-and-lead-velocity.md) adds the time needed to build the 30,000-contact universe. Include that acquisition period and the sales cycle in payroll runway; invitations are not net accepted contacts.

Use the [business model and KPI framework](business-model-and-kpis.md) for contribution margin, the [implementation and investment roadmap](../roadmap/implementation-and-investment.md) for delivery/funding gates, and the [lean presales plan](../strategy/lean-presales-demonstrator-plan.md) for demonstrations.

| Proposed measure | Definition |
| --- | --- |
| Stage conversion | Unique accounts advancing / eligible accounts at the prior stage, per dated cohort |
| Contact-to-paid conversion | Unique paying accounts / eligible initial prospect accounts |
| Realized annual contract value | Contracted annual amount, with discounts and cancellation terms |
| ARR and collections | Report recurring run-rate separately from actual cash receipts |
| Payroll funding coverage | Cash available after delivery costs / fully loaded payroll, over the same period |
| Runway | Unrestricted available cash / expected net monthly cash outflow |

Deduplicate contacts and company accounts, distinguish accessible contacts from permission to contact, and validate price, retention, acquisition cost and margin through a bounded pilot before using this model for commitments. No outreach, trading, financing, recruitment or product implementation is performed by this documentation migration.

## Source migration record

| Field | Record |
| --- | --- |
| Original filename | `docs/Para crear y sostener.txt` |
| English destination | `docs/business/ten-skilled-jobs-payroll-and-b2b-conversion.md` |
| Baseline commit | `cee7212d561648ab5a4dd010754eae3025c0d6c9` |
| Original Git blob | `dee57e1ca7572fbf09060028a1485ea456545559` |
| Immutable original | [Spanish source](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/cee7212d561648ab5a4dd010754eae3025c0d6c9/docs/Para%20crear%20y%20sostener.txt) |
| Processing date | 2026-10-12 |
| Coverage | Opening premise; all five numbered sections; financial table; funnel; market allocation, cities and segments; coverage diagram; three action proposals |
| Editorial treatment | Full thematic translation; reconstructed tables; source assumptions distinguished from arithmetic corrections |

The working TXT is replaced by English Markdown; the original remains recoverable in Git history. This is a supplemental migration without renumbering the earlier 68 entries.

[Documentation index](../README.md) · [Consolidated annex](../ANNEX-DOCS-CONSOLIDATED.md#33-ten-skilled-jobs-payroll-and-b2b-conversion)
