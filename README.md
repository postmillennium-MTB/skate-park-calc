# Skatepark and Pump Track ROI Calculator — Methodology & Configuration Reference

**Version:** Current (reviewed 2026-10-21; see *Verification status* below)  
**Live:** https://www.postmillenniumrenaissance.com/pump-track/  
**Purpose:** Municipal investment advocacy for public skateparks, pump tracks, and combined wheel parks  
**Audience:** City councils, parks and recreation departments, municipal planners, community advocates

---

## Overview

The Skatepark and Pump Track ROI Calculator estimates the annual economic value of a publicly funded wheeled sport facility. It produces two distinct economic value estimates — one anchored to peer-reviewed academic research, one derived from proxy data with documented limitations — that together give a planning-level estimate of community value. P1 has one anchor and an assumed scaling; P2 rests on a proxy and unsourced inputs. Neither is a floor.

**What the output represents:** Both pillars estimate *community economic value*, not municipal tax receipts, not direct facility revenue, and not return on investment in a commercial sense. The "value recovery" metric shows how long it takes for cumulative community economic benefit to equal the facility's construction cost. These figures are appropriate for public-good infrastructure framing before a council — they are not cash flow projections.

**Positioning:** Inputs were set below the published anchors, but the scaling and visitor inputs are judgment, so the tool does not claim a floor. The on-page checks flag any assumption set above its anchor, and note when direct spend is a large share of the lowest MTB benchmark. Present results with the assumptions shown, and say which were edited.

**P1 and P2 are different kinds of value.** P1 is consumer surplus (welfare). P2 is visitor spending (transactions). The combined figure is shown for scale, not as a financial return, and the tool shows each pillar's payback alone and its share of the total. Value is gross, undiscounted and before maintenance and operating cost.

---

## Pillar 1 — Direct User Economic Surplus

### What it measures

The economic value that facility users derive from visiting, measured as their willingness to pay above and beyond their actual travel costs. This is distinct from visitor spending (Pillar 2) — it is a measure of *benefit received*, not *dollars circulated*.

### Formula

```
P1 = Construction Cost × Annual Surplus Rate
```

### Derivation

P1 is anchored to the only peer-reviewed Travel Cost Model (TCM) study of a public skatepark facility:

> Kemp, J. (2025). Estimating the user benefits associated with large public skateparks.
> *Journal of Economic Analysis*, 4(1), 66–82.
> https://www.anserpress.org/journal/jea/4/1/90

**Kemp (2025) baseline — Lauridsen Skatepark, Des Moines, Iowa:**
- Facility size: 88,000 sq ft (largest public skatepark in the United States at time of study)
- Estimated construction cost: approximately $6.2 million. **Not from Kemp**: the abstract reports no cost. Press coverage gives a $6.1M expected budget and a $6.3M funding goal (2019); no final audited cost was found. The 7.9% is therefore this tool's ratio of a study figure to a news figure.
- Annual consumer surplus (adults): $488,000
- Per-adult-user-day benefit: $61 (implies roughly 8,000 adult user-days per year)
- Implied annual surplus rate: $488,000 ÷ $6,200,000 = **7.9% per year**
- Dollar year and sample size: not stated in the abstract
- Adults only: youth users are not counted

Kemp's surplus is driven by visits and travel distance, not by what the facility cost. Tying a rate to construction cost is this tool's own device, and the README and the page say so. The Travel Cost Model establishes user benefit by analyzing the relationship between a visitor's travel distance and frequency of visits. Users who travel further incur higher costs but still choose to visit, revealing their willingness to pay. The $61 figure is a TCM-derived consumer surplus — not an admission fee, but a revealed-preference measure of value received per adult user-day.

### Scaling logic

The Lauridsen is an exceptional facility: the largest of its kind in the country, generating national destination draw. Smaller or less destination-oriented facilities produce proportionally lower surplus per construction dollar because:

1. Most of their users travel short distances, generating near-zero TCM-measured travel-cost surplus
2. Less unique or specialized facilities attract fewer willing-to-travel visitors

Annual surplus rates applied in the calculator range from 3.0% to 7.2%, all set below the Lauridsen's 7.9% baseline. **The rates are the author's judgment: nothing derives why 4.8% and not 5.5%.** The destination skatepark rate of 7.2% is set slightly below the Lauridsen to reflect that even large regional destination skateparks are unlikely to match that facility's exceptional national profile. The calculator flags any edited rate above 7.9%.

**P1 is driven by construction cost, not daily user count or operating days.** Those two inputs affect Pillar 2 only, and the page tags them "P2 input".

### Limitation

The Kemp (2025) Lauridsen study is the *only* peer-reviewed TCM analysis of a public skatepark. Applying its framework to pump tracks and wheel parks requires analogy by facility type — no direct TCM study of pump tracks exists. The page now states this beside P1 (badge: **A · Anchored, rates assumed**). The old "High confidence" badge overstated it: only the single Kemp figure is anchored, and the scaling to nine presets is assumed.

---

## Pillar 2 — Visitor & Tourism Spending

### What it measures

The economic activity generated in the local economy by out-of-town visitors whose trip is primarily or partly motivated by the facility. This is expressed in direct community dollars — the actual spending on gas, food, lodging, and retail by non-local visitors, amplified by a standard economic multiplier.

### Formula

```
P2 = Average Daily Users × Visitor Fraction × Operating Days × Direct Spend per Visitor-Day × Economic Multiplier (1.72×)
```

### Source data

No peer-reviewed visitor spending study exists for public skateparks or pump tracks. P2 uses mountain bike tourism proxy data as the nearest available benchmark:

- Whistler Bikepark visitor studies: $94–$133 per visitor per day
- Northwest Arkansas cycling tourism study: $159.4 million annual economic impact from bicycle tourism; $416 average spending per destination trip (Trust for Public Land, 2025)
- Economic multiplier: $1.72 per $1 of direct outdoor recreation visitor spending (Outdoor Industry Association, 2022)

These are a different kind of facility: lift-served bike parks and trail networks, with lodging, where a visit is a trip. A wheeled-sport facility is a different product. The tool scales spend down from the benchmark by judgment, as described below, and the page tags the result **P · Proxy, inputs assumed**.

### Visitor fraction rationale

Visitor fractions range from 1.5% (small neighborhood pump track) to 4.0% (destination skatepark). These are assumptions with no source; the page tags them **J · Judgment**. For comparison, major MTB trail networks routinely report 30–60% of users as out-of-town visitors. Wheeled sport facilities are generally not the sole driver of travel in the way that a Whistler or Moab destination is; the fractions here reflect a more realistic subset of daily users making purpose-driven trips from outside the local area.

### Spend by facility type — judgment, not a derived income adjustment

A documented income differential exists between mountain bike and skateboarding participant populations:

**Mountain biking (higher income):**
Over 50% of mountain bike participants in the United States come from households earning $75,000 or more per year. The high cost of entry — capable trail bikes range from $2,000 to $8,000+ — creates a natural income filter.

> Sources:
> - SHRED TRAIL / OIA Outdoor Participation Survey data:
>   https://shredtrail.com/mountain-biking-statistics/
> - Singletracks.com reader demographics study (households earning $100K+ over-represented vs. U.S. population)
> - American Trails, "Mountain Bicycling in Wisconsin: Surveyed and Analyzed" (54%+ of respondents earning above $50K, higher than local demographic baseline):
>   https://www.americantrails.org/resources/mountain-bicycling-in-wisconsin-surveyed-and-analyzed

**Skateboarding (near national median):**
Skateboarding participant household income is near or slightly below the national median (~$54,000), distributed broadly across income brackets rather than concentrated at the upper end. Skateboarding ranks in the bottom 10 of all tracked recreational activities by participant median household income.

> Sources:
> - National Sporting Goods Association (NSGA) sports participation by household income survey, summarized in:
>   Sports Destinations Management (2013). "Connecting Sports Participation with Household Income."
>   https://www.sportsdestinations.com/management/economics/nsga-study-8221
> - Tony Hawk Foundation / ERIC (2020). *Beyond the Board: Findings from the Field.*
>   Survey of 5,717 respondents; financial issues cited as top concern by 74% of skaters under 26.
>   https://files.eric.ed.gov/fulltext/ED609263.pdf

**Application in the calculator:**
The income argument above is the reason for setting skatepark spend below pump-track spend. It is not a derivation, and it is weak for pump tracks, which serve many children and families, so adult MTB household income is a poor basis for their higher values. In the presets, **scale moves the spend value much more than type does** (neighborhood pump track $22 vs neighborhood skatepark $20). Combined wheel park figures sit between the two.

The MTB proxy range from source studies is $94–$133 per visitor per day (direct spending, before any multiplier). Spend values in the calculator range from $20 (neighborhood skatepark) to $85 (destination pump track). **The earlier text called these "substantial discounts at all tiers". That does not hold at the top:** $85 is 90% of the lowest benchmark, and after the 1.72× multiplier a destination pump track is $146 per visitor-day. The page now shows direct spend as a share of the lowest benchmark and the after-multiplier figure, and the destination presets are open to revision.

### Operating days

Default is 300 days per year (applies to P2 only). The slider allows adjustment from 180 to 365 days in 5-day increments to reflect local climate:

| Days | Climate context |
|---|---|
| 340–365 | Mild (GA, TX, CA, FL) |
| 300–339 | Temperate (CO, PA, OR, NC) |
| 260–299 | Northern (MN, WI, NY, WA) |
| 180–259 | Cold / harsh winters (ND, MT, AK) |

---

## Configuration Parameters — All 9 Presets

The table below lists every parameter for each facility type and scale combination. Users may override all six numbers: **construction cost**, **average daily users**, and the four assumptions (**sR**, **vP**, **vS** and the **multiplier**). Edited fields are outlined, the summary says which assumptions differ from the presets, and a copied link carries them. Switching type or scale keeps edited values; "Reset to presets" clears them.

| Facility Type | Scale | Default Cost | Default Users/day | Surplus Rate (sR) | Visitor Fraction (vP) | Visitor Spend/day (vS) |
|---|---|---:|---:|---:|---:|---:|
| Pump track | Neighborhood | $75,000 | 25 | 3.0% | 1.5% | $22 |
| Pump track | Regional | $200,000 | 60 | 4.8% | 2.5% | $58 |
| Pump track | Destination | $450,000 | 120 | 6.0% | 3.2% | $85 |
| Skatepark | Neighborhood | $275,000 | 40 | 3.5% | 1.8% | $20 |
| Skatepark | Regional | $550,000 | 80 | 5.5% | 3.0% | $48 |
| Skatepark | Destination | $1,200,000 | 150 | 7.2% | 4.0% | $72 |
| Combined wheel park | Neighborhood | $350,000 | 55 | 3.2% | 1.8% | $22 |
| Combined wheel park | Regional | $750,000 | 105 | 5.2% | 3.0% | $52 |
| Combined wheel park | Destination | $1,800,000 | 250 | 6.8% | 3.8% | $82 |

**Column definitions:**

- **sR (Surplus Rate)** [tag J · Judgment]: Annual surplus rate applied to construction cost for P1. Derived from Kemp (2025) Lauridsen baseline of 7.9%/yr, scaled down by facility size and destination-draw characteristics.
- **vP (Visitor Fraction)** [tag J · Judgment]: Percentage of daily users estimated to be out-of-town visitors for P2 calculation. Conservative relative to MTB destination benchmarks.
- **vS (Direct spend/visitor-day)** [tag P · Proxy]: Estimated average daily spending by an out-of-town visitor (gas, food, lodging, retail), before the multiplier. Scaled from MTB proxy data by judgment.
- **Multiplier** [tag C · Cited]: 1.72×, OIA (2022), national outdoor recreation. May overstate a small local facility.

### Scale definitions

**Neighborhood:** Primarily serves local residents within a short travel radius. Users arrive on foot, by bike, or by short car trip. Very low visitor fraction; near-zero travel-cost surplus in TCM terms. Benchmark construction costs reflect modest asphalt pump tracks ($50K–$120K) or small concrete skateparks ($150K–$400K).

**Regional:** Serves a multi-town or multi-county area. Meaningful destination draw from surrounding communities; a mix of local daily users and regional day-trip visitors. Benchmark costs reflect mid-size asphalt pump tracks ($150K–$300K) or 10,000–15,000 sq ft concrete skateparks ($450K–$750K).

**Destination:** Purpose-driven travel from a broad geographic region. Competition-grade or landmark facilities that function as a primary reason for travel. Visitor spend approaches the MTB proxy benchmark range. Benchmark costs: $350K–$600K for competition-grade pump tracks; $900K–$1.5M for large destination skateparks.

---

## Default Value Recovery — Reference Table

The following payback estimates assume both pillars are active and operating days are set to 300. Payback will increase (longer) when operating days are reduced.

| Facility Type | Scale | Approx. Value Recovery |
|---|---|---|
| Pump track | Neighborhood | ~11.5 years |
| Pump track | Regional | ~3.7 years |
| Pump track | Destination | ~2.3 years |
| Skatepark | Neighborhood | ~16.1 years |
| Skatepark | Regional | ~6.1 years |
| Skatepark | Destination | ~3.9 years |
| Combined wheel park | Neighborhood | ~15.6 years |
| Combined wheel park | Regional | ~6.1 years |
| Combined wheel park | Destination | ~3.4 years |

The faster payback for pump tracks vs. skateparks at equivalent scale comes from the spend assumptions and the smaller construction cost, not from a measured difference in visitor behavior. These were checked against the code on 2026-10-21 and match. Nine-preset payback ranges from 13.9 to 33.3 years on P1 alone, and spending is 43–86% of the combined value, so the headline depends on the least-sourced pillar.

---

## Worked Example

**Scenario:** A mid-size city proposes a $550,000 regional skatepark. Expected daily users: 80. Climate is temperate (300 operating days).

**P1 — Direct User Economic Surplus:**
- Formula: $550,000 × 5.5% = **$30,250/year**
- Interpretation: The community receives $30,250 annually in user economic surplus, equivalent to 5.5% of the capital invested, anchored to the Kemp (2025) Lauridsen baseline.

**P2 — Visitor & Tourism Spending:**
- Visitor-days: 80 users × 3.0% visitor fraction × 300 days = 720 visitor-days/year
- Gross spend: 720 × $48/day = $34,560
- With multiplier: $34,560 × 1.72 = **$59,443/year**
- Interpretation: Out-of-town visitors generate approximately $59,000 in annual local economic activity. Based on mountain bike tourism proxy data, adjusted downward for skateboarding demographics.

**Combined:**
- Total annual value: $30,250 + $59,443 = **$89,693/year**
- Value recovery: $550,000 ÷ $89,693 = **6.1 years** (gross, undiscounted, before maintenance)
- Annual value ÷ cost: 16%

---

## What the page shows

- A per-field tag on every assumption (J · Judgment, P · Proxy, C · Cited), and a P1/P2 badge with a letter and a word (never color alone).
- Checks under the assumptions: a rate above the Kemp-based 7.9%; direct spend at or above, or at half or more of, the lowest MTB benchmark ($94).
- Each pillar's payback alone and its share of the combined value.
- Payback on a 20-year timeline, replacing the earlier "value recovery progress" bar, which showed the *remaining* share of 20 years after payback and read as progress.
- **Copy link** always writes the canonical `https://www.postmillenniumrenaissance.com/pump-track/#…` address and carries the pillar toggles and any edited assumptions. Format: `#type-scale-days-pillars-cost-users-sR-vP-vS-mult`, where `pillars` is `11`, `10`, `01` or `00` and `p` means "follow the preset". Links in the old format (`#type-scale-cost-users-days`) still open.
- Print includes the assumptions, the pillars included, the date, and a planning-estimate notice.

## Verification status (2026-10-21)

| Item | Status |
|---|---|
| Kemp (2025): ~$488K/yr, $61/adult user-day | Read on the publisher's abstract page |
| Kemp: $6.2M cost | **Not in the abstract.** Press: $6.1M expected / $6.3M funding goal (2019); links from search results, not opened |
| Kemp: size, sample, dollar year | Not stated in the abstract |
| Whistler $94–$133 per visitor-day | Not verified; cited via NW Arkansas studies |
| NW Arkansas, TPL 2025, $416 per trip | Not verified |
| OIA (2022) 1.72× multiplier | Not verified |
| NSGA and Tony Hawk Foundation income data | Not verified |
| Wishaw pump track 55% crime reduction | Not used by the tool; primary report not verified |

## Complete Source List

**Press coverage of Kemp (2025):**

https://www.spaskateparks.com/resources/skatepark-user-economic-benefits/
https://www.wpr.org/news/wisconsin-skateboarding-economist-researches-value-skate-parks
https://www.npr.org/sections/planet-money/2025/01/14/g-s1-42171/this-skateboarding-economist-suggests-we-need-more-skateparks-and-less-capitalism

**Lauridsen Skatepark cost, press reports (2019):**

https://www.businessrecord.com/skatepark-lands-500k-state-grant-closes-in-on-doubled-6-1-million-budget
https://www.crestonnews.com/2019/10/14/des-moines-skatepark-reaches-6-3m-funding-goal/arlnixf


**Primary study — P1 anchor:**

Kemp, J. (2025). Estimating the user benefits associated with large public skateparks.
*Journal of Economic Analysis*, 4(1), 66–82.
https://www.anserpress.org/journal/jea/4/1/90

**Supporting literature — wheeled sport economics:**

Glenney, B., Bjorke, I., & Buchetti, A. (2024). Skateboarding and the surplus value of city play.
*Frontiers in Sports and Active Living*, 6, Article 1454274.
https://doi.org/10.3389/fspor.2024.1454274

Todd, M., & Archer, M. (2025). A different gravitation: acceptance of authentic selves, becoming through
doing, and support through connection within a Highland skatepark. *Leisure Studies*, 1–17.
https://doi.org/10.1080/02614367.2025.2467749

Kilberth, V. (2025). Spaces for skateboarding in the city — new spatial concepts beyond skateparks.
*Frontiers in Sports and Active Living*, 6, Article 1457427.
https://doi.org/10.3389/fspor.2024.1457427

**Visitor spending & economic multiplier:**

Outdoor Industry Association. (2022). *Outdoor Participation Trends Report.*
Economic multiplier: $1.72 per $1 of direct visitor spending in local communities.

Trust for Public Land. (2025). Mountain bike trail economic impact data.
Average visitor spending: $416 per destination trip. Trail networks supporting up to 1,626 jobs
and $54.1 million in annual labor income across 13 locations.

Whistler Bikepark visitor studies. Cited range: $94–$133 per visitor per day.
(Referenced via Northwest Arkansas cycling tourism economic studies.)

**Cycling infrastructure health & social ROI** (background reading; not used by the calculator):

Macmillan, A., Connor, J., Witten, K., Kearns, R., Rees, D., & Woodward, A. (2014). The societal costs
and benefits of commuter bicycling: Simulating the effects of specific policies using system dynamics
modeling. *Environmental Health Perspectives*, 122(4), 335–344.
https://doi.org/10.1289/ehp.1307250

Sport New Zealand. Social Return on Investment study: $2.12 social return per $1 spent on
recreational physical activity.

**Demographic & income data:**

National Sporting Goods Association (NSGA). Sports participation by household income survey.
Summarized in: Sports Destinations Management (2013). Connecting Sports Participation with
Household Income.
https://www.sportsdestinations.com/management/economics/nsga-study-8221

Tony Hawk Foundation / ERIC. (2020). *Beyond the Board: Findings from the Field.*
Survey of 5,717 skateboarding respondents; income distribution and demographic data.
https://files.eric.ed.gov/fulltext/ED609263.pdf

SHRED TRAIL / Outdoor Industry Association. Mountain biking household income demographics.
~50% of participants from households earning $75,000+.
https://shredtrail.com/mountain-biking-statistics/

American Trails. Mountain Bicycling in Wisconsin: Surveyed and Analyzed.
54%+ of surveyed MTB participants reporting household income above $50,000;
higher income, educational attainment, and managerial occupations vs. local demographics.
https://www.americantrails.org/resources/mountain-bicycling-in-wisconsin-surveyed-and-analyzed

**Construction cost benchmarks:**

Public Skatepark Development Guide / Tony Hawk Foundation.
$50–$75 per square foot for outdoor concrete skateparks; neighborhood park (10,000 sf) ~$500,000.
https://publicskateparkguide.org

**Crime reduction & anti-social behavior data:**

Tony Hawk Foundation police survey (102 officers, 37 states): 91% reported no major issues at local
skateparks; 85% reported fewer complaint calls from businesses after skatepark opening.

North Lanarkshire Council (Scotland). Wishaw Pump Track post-construction assessment.
Reported 55% reduction in local anti-social behavior and crime rates following facility opening.
(Circulates in advocacy literature; primary council report not independently verified at time of writing. Not used by the calculator.)

---

## Disclaimer

All estimates are planning-level projections intended to support evidence-based municipal investment cases.
Results should be presented alongside original source studies. This tool does not constitute investment advice, a certified
economic analysis, engineering assessment, or legal or financial recommendation. The same notice is on the page and in printed output.

The calculator and this methodology document were produced for public advocacy purposes.
The underlying Kemp (2025) study is the only peer-reviewed economic analysis specific to skateparks;
all other estimates involve extrapolation, proxy data, or analogy by facility type.
Each pillar's badge and each assumption's tag are shown within the calculator interface.
