# DI-ShoppingWise

DI-ShoppingWise is a Grounded DI public demonstration archive for rule-governed product-claim review, transparent recommendations, and provenance-oriented shopping workflows.

**Published by:** Grounded DI LLC · **Creator / operator:** Mark S. Weinstein · **Public repository established:** July 30, 2025

## Overview

The repository preserves five substantive artifacts: a makeup shopping list, a consumer-claim clarity audit, a shampoo assessment, a family-and-pet sofa comparison, and a nail-concealer recommendation memo. Together they show how ShoppingWise DI² records user constraints, product claims, source types, safety or integrity gates, recommendation rationale, and a final disposition.

The public tree is an evidence and demonstration archive. It contains no runnable ShoppingWise service, product-data connector, dependency manifest, test suite, CI workflow, or current source links. “Deterministic” is used narrowly here to describe fixed or rule-governed processing under stated inputs; it is not a guarantee that a product is safe, compliant, authentic, or suitable for every consumer.

## Why It Matters

Consumer recommendations combine facts that change over time with claims that need scrutiny. The strongest ShoppingWise record makes those layers visible: a claim is compared with transparency or source information, an integrity rule can trigger an override, and the output retains a reason, score, certainty field, and review boundary. That is more useful for diligence than an unexplained “best product” label.

## Key Records

| Artifact | What the repository records | Status / boundary |
|---|---|---|
| `ShoppingWise_Clarity_Audit` | A DI² claim-audit demonstration covering three sample products and the claims “Hypoallergenic,” “Non-toxic,” and “Volume-limited.” It records Scroll 91 overrides, a safety index, entropy values, certainty, and hallucination-risk fields. | Creator-authored demonstration. The public tree contains no product test data, regulatory corpus, benchmark, or independent confirmation of the stated scores or claims. |
| `Safe_Makeup_Shopping_List.md` | July 30, 2025 curated picks across seven makeup categories, with shade, ingredient, safety, and quality rationales. Links and prices are redacted. | Recommendation record, not a current catalog, safety certification, or independent product review. |
| `Shampoo_DI2_Demo` | Fancy- and Regular-mode assessment of Garnier Whole Blends Oat & Rice shampoo, including ingredient observations, fragrance cautions, and a recorded certainty/hallucination-risk status. | Source type is identified as secondary in the artifact; product facts, user reports, and EWG references are not independently rechecked here. |
| `Mid-Century_Sofa_DI2_5-Pro` | September 14, 2025 comparison of three mid-century-style sofas under a stated `$6,000` budget for a child-and-dog household. The record marks the constraint check `PASSED`. | Prices, warranty terms, fabrics, and source links are time-sensitive or redacted. The record is not a current purchasing guarantee. |
| `ShoppingWise_Manucurist_Nail_Concealer_Pick.pdf` | A five-product comparison that ranks Manucurist Active Smooth first with a recorded `9.5/10` concealer score and Active Blur second at `9/10`. | A recommendation memo based on the stated visual goal; scores are editorial judgments, not laboratory measurements. |

## What the Record Demonstrates

### Product-claim clarity path

The clarity audit documents a proposed path from a consumer claim to an integrity disposition:

`claim → transparency / source check → Phantom Claim filter → Scroll 91 override → score and rationale → human review`

The record states that Scroll 91 fired on all three sample products, that `∆H ≤ 0.03` passed its entropy-lock condition, and that the audit captured a safety index of `71/100`, certainty `92`, and low hallucination risk for the CleanSkin sample. Those are values displayed by the artifact; no executable benchmark or independent product testing is included.

### Constraint-based recommendations

The shopping records turn user preferences into explicit constraints: product category and shade for makeup; ingredient and fragrance considerations for shampoo; style, budget, construction, warranty, and family/pet practicality for sofas; and finish, coverage, and ease of use for nail products. The recommendation memos preserve the reason for each selection instead of presenting a bare ranking.

### Review modes and state labels

The artifacts use labels such as Fancy Mode, Regular Mode, `PASSED`, `Claim Passed`, ScrollLock, certainty, and hallucination risk. These are record-level dispositions and presentation modes. The repository does not include a runtime that implements separate Scan, Deep Audit, DriftWatch, KidShield, or BrandCheck modes.

## Recorded Checks

| Check | Result | Evidence |
|---|---|---|
| Claim-audit sample | Scroll 91 override reported for three products; Scroll 106 `Verified`; Scroll 122 `Locked` | `ShoppingWise_Clarity_Audit` |
| Entropy-lock field | `∆H = 0.02` for the CleanSkin sample; condition shown as `∆H ≤ 0.03 → PASS`; artifact states all scans were stable | `ShoppingWise_Clarity_Audit` (the referenced benchmark file is not in this repository) |
| Shampoo assessment | `Claim Passed`; certainty `85`; hallucination risk `Low`; source type `Secondary` | `Shampoo_DI2_Demo` |
| Sofa comparison | `PASSED`; three options meet the stated style, budget, and durability constraints; certainty `95`; hallucination risk `Low` | `Mid-Century_Sofa_DI2_5-Pro` |
| Nail memo | Active Smooth `9.5/10`; Active Blur `9/10`; Plump `7.5/10`; Active Glow `7/10`; Active Shine `3/10` | `ShoppingWise_Manucurist_Nail_Concealer_Pick.pdf` |
| Repository review during this update | Six tracked files inspected, including the PDF; no executable runtime, product-data feed, tests, dependencies, or CI found | Current `main` tree and Git history |

The checks above are artifact-recorded outputs. They do not establish current product availability, regulatory compliance, medical safety, or independent accuracy.

## Technical Significance

ShoppingWise’s useful design pattern is the combination of a recommendation rationale with a claim-level override path and a preserved review state. For a commercial evaluator, that creates a clear place to add live sources, jurisdiction-specific rules, human approval, and an audit receipt without hiding why an item was selected or rejected.

## Scope and Limitations

- Prices, product formulations, warranties, retailer policies, reviews, and regulatory references can change; the repository does not refresh them.
- Source URLs and supporting file identifiers are redacted or absent in several artifacts, so current verification requires a separate research pass.
- “Safe,” “non-toxic,” “hypoallergenic,” “genuine,” and similar terms are claims recorded in the demos, not certifications issued by ShoppingWise or a regulator.
- The demonstrations do not establish that a product is suitable for a particular allergy, medical condition, child, pet, or household.
- No production implementation, API, browser extension, sensor, or test harness is included.

## How to Review

```bash
git clone https://github.com/Grounded-DI/DI-ShoppingWise.git
cd DI-ShoppingWise
```

Start with `ShoppingWise_Clarity_Audit` to see the claim and override structure. Then review the shampoo and sofa records for constraint-based recommendations, the makeup list for category coverage, and the PDF memo for a compact ranked output. For any live evaluation, independently verify product pages, prices, ingredients, certifications, and applicable consumer-protection rules at the time of use.

## Evaluation and Integration Context

The public archive can support a scoped proof of concept for transparent product research: normalize a user brief, preserve source snapshots, evaluate claims against an approved rule set, route uncertain or high-risk claims to a human, and export a reasoned recommendation with receipts. A responsible pilot would add current source retrieval, provenance capture, conflict handling, accessibility and bias review, and a clear correction path.

Potential integration scenarios include editorial shopping research, internal product-content QA, and consumer-protection review. Nothing in this repository establishes a deployed service, customer adoption, compliance certification, or product-safety guarantee. Commercial licensing and integration inquiries: **[CONTACT PLACEHOLDER]**.

## Authorship, Provenance, and Intellectual Property

Git history identifies Grounded DI LLC and Mark S. Weinstein as the repository authorship identity beginning July 30, 2025. The artifacts retain dates, DI²/ShoppingWise labels, ScrollLock values, signal language, recommendation scores, and stated source types as public provenance records. These records support technical chronology and traceability; they do not independently establish legal ownership or patent priority.

The repository description and one artifact use “Patent-Pending” language. No filing record is included in this repository, so this README makes no representation about the scope or status of any particular patent application. Verify any filing statement against an identified public record before external use.

No open-source license is present. Public availability does not grant reuse rights to the reports, formulas, branding, or nonpublic implementation materials. Review any future license, notice, citation file, and release terms separately with counsel.

## Status

**Status:** Active public product-research and claim-audit demonstration archive. It preserves concrete recommendation and override records for review; it is not a current product database, safety certification, regulatory compliance system, or independently validated consumer classifier.

## Discovery

#ShoppingWise #ConsumerResearch #ProductClaimAudit #AIValidation #HumanInTheLoop #Provenance #AuditTrail #GroundedDI
