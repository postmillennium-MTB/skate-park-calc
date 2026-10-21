# Skatepark and Pump Track ROI Calculator — Methodology & Configuration Reference

**Version:** Current (reviewed 2026-10-21; see *Verification status* below)  
**Live:** https://www.postmillenniumrenaissance.com/pump-track/  
**Purpose:** Municipal investment advocacy for public skateparks, pump tracks, and combined wheel parks  
**Audience:** City councils, parks and recreation departments, municipal planners, community advocates

---

## Overview

The Skatepark and Pump Track ROI Calculator estimates the annual economic value of a publicly funded wheeled sport facility. It produces two distinct economic value estimates — one anchored to peer-reviewed academic research, one derived from proxy data with documented limitations — that together give a planning-level estimate of community value. P1 has one anchor and an assumed scaling; P2 rests on a proxy and unsourced inputs. Neither is a floor.

**What the output represents:** Both pillars estimate *community economic value*, not municipal tax receipts, not direct facility revenue, and not return on investment in a commercial sense. The "value recovery" metric shows how long it takes for cumulative community economic benefit to equal the facility's construction cost. These figures are appropriate for public-good infrastructure framing before a council — they are not cash flow projections.

**Positioning:** Inputs were set below the published anchors, but the scaling and visitor inputs are judgment, so the tool does not claim a floor. The on-page checks flag any assumption set above its anchor, and note when direct spend is a large share of the lowest per-day MTB figure in the Ledger. Present results with the assumptions shown, and say which were edited.

**P1 and P2 are different kinds of value, so they are shown as two separate results.** P1 is consumer surplus (welfare: what users gain). P2 is visitor spending (economic impact: what visitors spend locally). Each has its own value and its own payback. A combined total is available behind a checkbox that is off by default, because adding a welfare measure to a spending measure mixes two accounting frames. In a benefit-cost analysis spending is a transfer, and a visitor's trip cost is already deducted inside the travel-cost surplus, so the dollars are not literally counted twice, but the sum answers no single question. The multiplier is a further problem: an output multiplier counts suppliers' sales too, which inflates P2 against any welfare figure. Values are gross, undiscounted and before maintenance and operating cost.

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

> Kemp, T. (2025). Shred Central: Estimating the user benefits associated with large public skateparks.
> *Journal of Economic Analysis*, 4(1):90. doi:10.58567/jea04010004
> https://www.anserpress.org/journal/jea/4/1/90
>
> (AMA-style citation: 90 is the publisher's article number; the page gives no page range. An earlier version of this README printed "66–82" and "Kemp, J." and the title without "Shred Central:"; all three were wrong. Checked against the publisher's page 2026-10-21.)

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

### What "what users gain" means

P1 is **consumer surplus**: the dollar value riders place on having the facility, over and above what it costs them to get there and use it. Nobody receives this money. It is value, not cash.

**The mechanism.** Say a skater would gladly pay $80 for a session and spends $19 in gas and time to get there. The $61 gap is their surplus, and $61 is Kemp's per-adult-user-day figure. Kemp measured it with a travel-cost model: people who live farther away pay more to come, and they come less often. That distance-versus-visits pattern traces out a demand curve for a facility that charges nothing, and the area under the curve, above what people actually paid, is the surplus. Because the park is free, the value people get is large relative to the revenue it brings in, which is why economists use surplus to price public recreation: it is the standard way to put a dollar figure on a free public good.

**How P1 differs from P2**

- P2 is money that changes hands in the local economy.
- P1 is value experienced by the rider. A rider who lives next door and spends nothing adds nothing to P2, but still gains from the facility.
- In a benefit-cost analysis, P1 is the benefit. Visitor spending would normally be a transfer, which is why the page shows the two separately.

**What P1 leaves out:** youth users (Kemp counts adults only); health, safety and property effects; and value to people who never ride (neighbors, parents).

**The gap between Kemp and this tool.** The tool does not estimate surplus per rider. It takes Kemp's $488K a year, divides by the park's $6.2M cost to get 7.9%, scales that down by judgment, and multiplies by the construction cost entered. So "what users gain" on the page is really "an annual user benefit tied to the cost, anchored to one study."

Dividing P1 by users × operating days shows how conservative that is:

| Facility | P1 per user-day |
|---|---|
| Neighborhood pump track | about $0.30 |
| Regional skatepark | about $1.26 |
| Destination skatepark | about $1.92 |
| Kemp's Lauridsen result | $61 |

(Preset values, 300 operating days. For example, the regional skatepark is $30,250 ÷ (80 users × 300 days) = $1.26.) The comparison is not apples to apples: Lauridsen draws destination travelers, and by the travel-cost method local users generate little surplus. But it shows that the page is not claiming Kemp-sized value per rider.

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

No peer-reviewed visitor spending study exists for public skateparks or pump tracks. **P2's spend values are compared against four mountain bike trail studies. They are a stand-in, not the source: the presets ($20–$85/visitor-day) are the author's judgment, scaled down from these, and the page says so.** The four are copied into the `BENCHMARKS` registry in `index.html` (from the PMR [Trail Visitor Spending Ledger](https://www.postmillenniumrenaissance.com/studies/), on purpose, so the tool does not depend on another page) and rendered on the page with citation, page, link, tier and a plain caveat. `PROXY_LOW` ($90) and `PROXY_HIGH` ($200) are derived from the list, not typed.

| Per-day, out-of-town | Study | Where | Tier |
|---|---|---|---|
| $90–$111 | Sage, J. L., & Nickerson, N. P. (2018). *Trail usage and value: a Helena, MT case study.* ITRR, University of Montana. https://scholarworks.umt.edu/itrr_pubs/365/ . Read via the TPL Green Paper (*Economic Benefits of Mountain Biking*, March 2025, https://www.tpl.org/wp-content/uploads/2025/03/Economic-Benefits-of-Mountain-Biking.pdf); the original was not reviewed. | TPL appendix p.29 (range $90.29–$110.59 confirmed in the Green Paper text, 2026-10-21) | M |
| $138.49 | Boozer, B. B., & Self, M. (2012). *An economic and impact analysis of the Coldwater Mountain Bike Trail.* Jacksonville State University, for the Calhoun County Community Development Corporation. https://headwaterseconomics.org/wp-content/uploads/Trail_Study_13-coldwater-mountain-bike-trail.pdf | pp.34–35 ($138.49 confirmed in the report text, 2026-10-21) | V |
| $143.27–$150 | Eades, D., & Arbogast, D. (2019). *Economic impacts of mountain biking and bike trail systems in West Virginia.* WVU Extension (title taken from the file name; later versions are retitled "…Bike Trail Events and Festivals…"). https://extension.wvu.edu/files/d/8d8adea5-a36b-4670-a729-4cc9143add34/economic-impacts-of-mountain-biking-and-bike-trail-systems-in-west-virginia-051619.pdf | Tables 9–10, pp.10–11 | M |
| $200 | Hadley, S., & Trechter, D. (2020). *Chequamegon Area Mountain Bike Association economic impact and user experience survey: summary, 2020* (Survey Research Center Report 2020/9). UW–River Falls. https://static1.squarespace.com/static/67a3d849527a3f4f3bc9c832/t/67f7182822b7236bc1b9bca3/1744246831440/Survey-Report-2020-Final.pdf | Table 1-3, p.16 ($200/day confirmed in the report text, 2026-10-21) | V |

Tiers (the Ledger's definitions): **V** the study's own direct rider survey; **M** a blended figure, or read through a secondary compilation. **The four are not independent**: West Virginia's $150 is the authors' rule of thumb built partly from Coldwater. The West Virginia link returned HTTP 403 to an automated fetch on 2026-10-21 and was not opened.

The Ledger's other per-day rows, with their sources, are at https://www.postmillenniumrenaissance.com/studies/ .

Three figures that earlier versions of this README (and the page) cited could **not** be traced on 2026-10-21 and are no longer used as benchmarks:

- "Whistler Bikepark visitor studies: $94–$133 per visitor per day." No such figure was found. The nearest traceable Whistler numbers are a 2015 Resort Municipality of Whistler summer-visitor figure of $148/day (all summer visitors, not bike park users; as quoted by REI) and a 2006 pilot study of the Bike Park (non-resident spending of $16.2M for June–September). Neither is a per-day bike park figure.
- "$416 per destination trip (Trust for Public Land, 2025)." **Corrected 2026-10-21 (an earlier version of this note said "not located"):** the TPL Green Paper *Economic Benefits of Mountain Biking* (March 2025) does say that for the destinations in its appendix, average per-visit spending by non-local mountain bikers is $416. It is *per visit*, not per trip, it averages the appendix destinations, and it is not a per-day figure, so it is not one of the four benchmarks.
- "Economic multiplier $1.72 per $1 (Outdoor Industry Association, 2022)." Not found in OIA's published reports. The tool still uses 1.72× as an editable default, tagged **C · Cited, unverified**, and shows direct spending before the multiplier next to the result. A regional example found while checking: a peer-reviewed Boundary Waters study reports a 1.59 output multiplier.

The $159.4 million Northwest Arkansas figure is real (University of Arkansas / Walton Family Foundation, 2023, covering all bicycling in two counties) but is an all-cyclist total, not a per-visitor spend, and is not used in the calculation.

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

The MTB per-day range in the Ledger is $90–$200 per visitor per day (direct spending, before any multiplier). Spend values in the calculator range from $20 (neighborhood skatepark) to $85 (destination pump track). **The earlier text called these "substantial discounts at all tiers". That does not hold at the top:** $85 is 94% of the lowest per-day figure ($90), and after the 1.72× multiplier a destination pump track is $146 per visitor-day. The page now shows direct spend as a share of the lowest per-day Ledger figure and the after-multiplier figure, and the destination presets are open to revision.

### Operating days

Default is 300 days per year (applies to P2 only). The slider allows adjustment from 180 to 365 days in 5-day increments to reflect local climate:

| Days | Climate context |
|---|---|
| 340–365 | Mild (GA, TX, CA, FL) |
| 300–339 | Temperate (CO, PA, OR, NC) |
| 260–299 | Northern (MN, WI, NY, WA) |
| 180–259 | Cold / harsh winters (ND, MT, AK, Canada) |

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
- **Multiplier** [tag J · Judgment]: 1.72×, **a starting point, not a measured value**, adjustable like every other input (1.0 shows direct spending only). Once attributed to OIA (2022); that could not be verified. Counts suppliers' sales too, so it may overstate a small local facility.

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

- A per-field tag on every assumption (J · Judgment, P · Proxy), a V/M tier on each benchmark study,, and a P1/P2 badge with a letter and a word (never color alone).
- **Two separate results (P1 user value, P2 visitor spending)**, each with its own payback, annual value ÷ cost, 20-year multiple and timeline. P2 also shows direct spending before the multiplier.
- An optional **combined total**, off by default (checkbox).
- Assumptions panel collapsed by default; it opens for print.
- Checks under the assumptions: a rate above the Kemp-based 7.9%; direct spend at or above, or at half or more of, the lowest per-day MTB figure in the Ledger ($90).
- Payback on a 20-year timeline, replacing the earlier "value recovery progress" bar, which showed the *remaining* share of 20 years after payback and read as progress.
- **Copy link** always writes the canonical `https://www.postmillenniumrenaissance.com/pump-track/#…` address and carries the pillar toggles and any edited assumptions. Format: `#type-scale-days-pillars-cost-users-sR-vP-vS-mult-combined`, where `pillars` is `11`, `10`, `01` or `00` (which pillars are shown), `p` means "follow the preset", and `combined` is `1` when the combined total is shown (absent means off). Links in the earlier formats (`#type-scale-cost-users-days`, and the same without `combined`) still open.
- Two buttons at the top, both with the Lucide `square-chevron-left` icon and `target="_top"`: Post Millennium Renaissance (home) and Trail Investment ROI Calculator (`/roi/`). The "Related tool" block at the bottom stays. Both are hidden in print.
- Print includes the assumptions, the pillars shown, the date, and a planning-estimate notice.

## Verification status (2026-10-21)

| Item | Status |
|---|---|
| Kemp (2025): ~$488K/yr, $61/adult user-day | Read on the publisher's abstract page |
| Kemp article link (anserpress.org), press link (spaskateparks.com), author profile (uwec.edu/profiles/kempta) | Confirmed working by Jon, 2026-10-21 |
| Kemp: $6.2M cost | **Not in the abstract.** Press: $6.1M expected / $6.3M funding goal (2019); links from search results, not opened |
| Kemp: size, sample, dollar year | Not stated in the abstract |
| Whistler $94–$133 per visitor-day | **Could not be traced; removed as a benchmark.** Replaced by the Ledger's per-day range ($90–$200) |
| Four benchmark studies (Helena, Coldwater, West Virginia, CAMBA) | Titles, authors and figures confirmed in the documents for Coldwater ($138.49), Helena via the TPL Green Paper ($90.29–$110.59) and CAMBA ($200); West Virginia not opened (HTTP 403). The Ledger itself notes not every figure was checked against its source |
| TPL 2025, $416 per non-local visit | Found in the Green Paper text (per visit, not per day). Not used as a benchmark. NW Arkansas $159.4M is a separate all-cyclist study |
| OIA (2022) 1.72× multiplier | **Not found in OIA's published reports**; kept as an editable default, tagged unverified |
| Kemp citation (title, author, 4(1):90, DOI) | Checked against the publisher's page; DOI resolves to the article |
| NSGA and Tony Hawk Foundation income data | Not verified |
| Wishaw pump track 55% crime reduction | Not used by the tool; primary report not verified |

## Complete Source List

**Author profile (Kemp, UW–Eau Claire):**

https://www.uwec.edu/profiles/kempta

**Press coverage of Kemp (2025):**

https://www.spaskateparks.com/resources/skatepark-user-economic-benefits/
https://www.wpr.org/news/wisconsin-skateboarding-economist-researches-value-skate-parks
https://www.npr.org/sections/planet-money/2025/01/14/g-s1-42171/this-skateboarding-economist-suggests-we-need-more-skateparks-and-less-capitalism

**Lauridsen Skatepark cost, press reports (2019):**

https://www.businessrecord.com/skatepark-lands-500k-state-grant-closes-in-on-doubled-6-1-million-budget
https://www.crestonnews.com/2019/10/14/des-moines-skatepark-reaches-6-3m-funding-goal/arlnixf


**Primary study — P1 anchor:**

Kemp, T. (2025). Shred Central: Estimating the user benefits associated with large public skateparks.
*Journal of Economic Analysis*, 4(1):90. doi:10.58567/jea04010004
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

Outdoor Industry Association. (2022). *Outdoor Participation Trends Report.* **Attribution of the 1.72× multiplier unverified; not found.**

Trust for Public Land. (2025). Mountain bike trail economic impact data. The $416 figure is real (per non-local visit, averaged over its appendix destinations) but is not per-day and is not used. Trail networks supporting up to 1,626 jobs
and $54.1 million in annual labor income across 13 locations.

Whistler Bikepark visitor studies. **The $94–$133 range could not be traced and is no longer used.** (See Source data.)

**P2 benchmark studies:** the four listed under *Source data*; more in the PMR Trail Visitor Spending Ledger, https://www.postmillenniumrenaissance.com/studies/

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
