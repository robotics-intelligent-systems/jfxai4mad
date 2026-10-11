# Ergonomic recliners and support wedges: source review

Reviewed: 2026-10-11. Status: research and proposed requirements; no furniture prototype, clinical validation or procurement decision.

## Provenance and scope

Migration entry 68 processes `docs/El uso de mobiliario de.txt`, Git blob `23dfc4023332ee4239a18d47ff83ed169c07befb`, retained at [source revision](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/ec3016b913f6fa4099eb7e2c218ab286b19536d6/docs/El%20uso%20de%20mobiliario%20de.txt).
The source has no author, date, measurements or citations. Coverage includes the introduction, three recliner features, both wedge-use groups, cleaning considerations and all three summary rows. Its prose supplies research input; it does not establish engineering requirements.

The candidate connection to [OpenTwin modular habitats](../../mbse/opentwin-modular-habitat.md) is furnishing and accessibility research. Adult couple comfort and pregnancy/feeding support are separate intended-use scenarios. No benefit for conception or fertility is established.

## Normalized source content

The draft proposes rest furniture and ergonomic supports for adult comfort and later family-care and breastfeeding scenarios.

### Recliner features proposed in the source

- Adjustable recline and a marketed “zero gravity” position: intended to redistribute body weight and reduce lumbar/pelvic pressure.
- High-density foam and memory foam: intended to adapt to pressure points and support elevated or resting postures.
- Prominent lumbar and pelvic support: intended to maintain spinal alignment and improve comfort; the draft also claims pelvic-floor relaxation.

### Wedge cushions and pillows

For adult couple comfort, the draft proposes pelvic elevation through an inclined wedge to reduce leg and lower-back strain. It claims solid viscoelastic foam remains stable under body weight, unlike air- or fibre-filled cushions.

For pregnancy, it proposes lumbar/back support and claims a wedge relieves vena-cava pressure during side rest or recline. For breastfeeding, it proposes combining the wedge and recliner to support infant positioning and reduce shoulder, neck and arm fatigue. Removable washable knit covers, described as hotel-style, are proposed for softness, breathability and routine family cleaning.

| Source element | Proposed function | Claimed ergonomic benefit |
| --- | --- | --- |
| Reclining chair | Whole-body rest and relaxation posture | Weight distribution and reduced lumbar pressure |
| Viscoelastic wedge | Pelvic support / angular elevation | Spinal alignment, posture stability and adult couple comfort |
| Washable knit cover | Breathability and cleaning | Soft contact surface for sensitive skin and feeding scenarios |

These benefits remain source claims unless qualified below.

## Selected evidence checks

| Claim / decision | Review outcome |
| --- | --- |
| Pillows may support pregnancy comfort | NHS describes side sleeping and pillows supporting the bump or between the knees. This does not validate a particular wedge, recliner angle or vascular-pressure claim. [Pregnancy sleep guidance](https://www.nhs.uk/pregnancy/common-symptoms/tiredness/) |
| Support during breastfeeding | NHS describes supported chair and semi-reclined positions. This supports considering adjustable support; it does not establish a universal ideal infant height or product-specific reduction in fatigue. [Breastfeeding positions](https://www.nhs.uk/best-start-in-life/baby/feeding-your-baby/breastfeeding/how-to-breastfeed/breastfeeding-positions/) |
| Infant use of soft wedges / recliners | Feeding support must remain distinct from infant sleep equipment. NHS advises a clear, firm, flat sleep surface and identifies risk from sleeping with an infant on a sofa/chair. [Safer sleep](https://www.nhs.uk/best-start-in-life/baby/baby-basics/newborn-and-baby-sleeping-advice-for-parents/safe-sleep-advice-for-babies/) |
| “Foam does not deform” | Unsupported absolute statement. Compliance under load is a material property to measure; stability, permanent set and recovery are different outcomes. No material test or manufacturer specification supplied. |
| “Zero gravity,” pelvic-floor relaxation, pressure reduction | No product definition, pressure map, clinical study or comparator supplied. Treat as hypotheses rather than demonstrated effects. |
| Sensitive-skin suitability, hygiene and breathability | No textile composition, laundering cycle, airflow or skin-contact evidence supplied. Washability alone does not establish these benefits. |

Sources accessed 2026-10-11. These selected checks do not constitute clinical advice or furniture certification.

## Proposed requirements and verification work package

All thresholds, sample sizes and applicable standards are TBD until a qualified reviewer approves the intended use and jurisdiction.

| ID | Proposed requirement | Verification and acceptance evidence |
| --- | --- | --- |
| MAD-ERG-001 | Separate adult rest, adult couple comfort and supervised feeding configurations; exclude infant sleeping use. | Review scenario/configuration matrix and labels against the declared scope; unresolved clinical claims block baseline approval. |
| MAD-ERG-002 | Specify seat, backrest, armrest and wedge dimensions, angle range, tolerances and units. | Compare drawings and measured prototype geometry to approved values; record anthropometric accommodation limits. |
| MAD-ERG-003 | Define recline locking, stability, load capacity, ingress/egress and pinch/entrapment controls for each configuration. | Qualified engineering review and reproducible static/cyclic/tip tests with approved loads, cycles and limits. No tests executed. |
| MAD-ERG-004 | Record foam type, density, load-deflection response, recovery and cover/material compatibility. | Supplier evidence plus load/compression and durability tests at declared conditions; quantify permanent set separately from elastic deflection. |
| MAD-ERG-005 | Specify removable-cover cleaning, dimensional change, drying and service replacement. | Approved wash-cycle protocol and measured post-cleaning fit; skin-contact or hygiene claims require separate evidence. |
| MAD-ERG-006 | Evaluate usability and comfort using a reviewed protocol and voluntary participants. | Define comparator, posture, duration, outcomes and stopping conditions before evaluation; no sensitive data collection or clinical study initiated. |

```mermaid
flowchart LR
    S[Historical TXT claims] --> E[Evidence and intended-use review]
    E --> R[Approved requirements and unresolved TBDs]
    R --> C[Dimensioned configuration and material data]
    C --> V[Engineering and usability verification]
    V --> H[Human acceptance review]
```

## Next AI-assisted task: MAD-ERG-001

Draft one adult-rest configuration and its dimension/material/verification matrix. AI may organize source evidence and draft the protocol; maintainers approve thresholds and qualified reviewers assess safety and any clinical claims. Deliver the configuration drawing, requirement-to-evidence links, test procedures and explicit unexecuted cases. Feeding-specific configurations require their own review. No physical prototype, measurements or implementation are claimed.

Related: [project scope](../../product/project-scope.md), [research index](../README.md), [documentation index](../../README.md).
