# Cost Curve & Pricing Strategy

## Cost Model

# Margin Calculator, Module 3

## Inputs
- Avg requests/user/month: 360000
- Blended cost/request: $0.00005
- Revenue/user/month: $284
- Non-AI COGS/user/month: $2.3

## Current Margin
- AI COGS/user: $18.00
- Total COGS/user: $20.30
- Gross margin: 92.9% ($263.70/user)

## Stress Test
| Scenario | AI COGS | Margin |
|----------|---------|--------|
| 3x Cost  | $54.00 | 80.2% ($227.70) |
| 2x Usage | $36.00 | 86.5% ($245.70) |

## Cost Curve
| Feature | Complexity | Model Tier | Cost/Req | Volume % | Weighted | Justification of Model |
|---------|------------|------------|----------|----------|----------|------------------------|
| Domain SME | Low | Small | .00005 | 40% | .0002 | Small domain corpus |
| Site guide | Low | Small | .00005 | 30% | .00 15 | Small site scope |
| Case resolution | Mid | Mid | .01 | 30% | .003 | MCP integration to other agent |



## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model: limited corpus and well-defined workflows**
**Mid model: Only needed for case resolution**
**Routing rule: Escalate to Mid model only for case resolution tasks**
**Expected cascade ratio:70/30**

## Pricing Model

Pricing Strategy Block, Module 3

Pricing Strategy
- Strategy posture: Penetrate
- Pricing model: Seat / Access
- Unit of work metered: Enrollments completed
- Base fee ($/month): 20
- Price per unit: $0
- Estimated units/user/month: 360000
- Implied revenue/user/month: $20.00

**Decision Note**
Why this pricing structure fits the buyer and the value delivered: ·We are using AI to increase conversions while lowering call center engagement.  Therefore we are following a combination of increased conversions and lowered support costs.

## Before/After for Board

**Before (traditional SaaS):**
Revenue: $85/seat x 36000 seats = $3M
COGS: $1.7M
Gross Margin: 176%

**After (AI-enabled):**
Revenue: $85/seat x 40000 seats = $3.4M
COGS: $1.3M
Gross Margin: 261%

**Net margin shift:**
Delta Margin %: 176% -> 261%
Narrative: AI slightly increases conversion while drastically reducing call center costs while using mainly low-tier models.
