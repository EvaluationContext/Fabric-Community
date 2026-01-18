## Main Question

- How does Atlanta compare to 11 peer cities across key livability dimensions?

## Design Concept: "City Comparison Cards" (Top Trumps Inspiration)

The core visual hook will be a "Head-to-Head" comparison tool, useful for planners to benchmark Atlanta against specific peers.

### 1. The Comparison View (Interactive Page)
- **Layout**: Two large "Profile Cards" side-by-side.
  - **Left Card**: Fixed to **Atlanta** (Anchor City).
  - **Right Card**: Dynamic (User selects peer city).
- **Card Content**:
  - **Hero Image**: Representative skyline/photo.
  - **Metric Cluster** (The 5 Dimensions):
    1. Housing Affordability
    2. Transit Score
    3. Green Space %
    4. Emissions Index
    5. Livability Composite
  - **Visualizations per Metric**:
    - **Icon**: Dynamic state (e.g., Leaf transition from brown to green for Green Space).
    - **Value**: Big generic number (BAN).
    - **Trend Indicator**: Arrow + Color difference (contextual: "Up" is bad for Emissions, good for Transit).
    - **Delta**: Gap analysis vs Atlanta (e.g., "+5% vs ATL").
- **Badges/Insights**:
  - Auto-generated text: "Atlanta has better transit but significantly lower green space."
  - Badges: "Green Leader", "Transit Hub", "Affordability Alert".

Ashgrove, Briarport, Cloudbreak, Crestwater, Eastwick, Golden Shoals, Ironbar, Northhaven, Prairiebend, Southmere, Willowford, Winterstead
  
### Data-Driven City Monikers (For Profile Cards)
*Based on 2024 data analysis (Fictional Cities):*

1.  **Briarport**: *"The Wallet Winner"* (Best Housing Affordability: 24.58)
2.  **Ironbar**: *"The Ultimate Utopia"* (Rank #1 in Livability: 68.5, Green Space: 53.7% & Transit: 89.2)
3.  **Southmere**: *"The Concrete Desert"* (Lowest Green Space: 27.9% & Tied Last in Livability)
4.  **Willowford**: *"The Heavy Breather"* (Highest Emissions: 66.4 & Tied Last in Livability)
5.  **Winterstead**: *"The Premium Passage"* (Great Transit: 83.9 but Most Expensive Housing: 52.9)
6.  **Cloudbreak**: *"The Clean Standard"* (Best Emissions: 35.0 & Rank #2 Livability)
7.  **Northhaven**: *"The Costly Commute"* (High Transit: 77.2 but 2nd Most Expensive: 48.5)
8.  **Eastwick**: *"The Urban Efficient"* (Rank #3 in Livability & #4 in Transit)
9.  **Crestwater**: *"The Green Runner-Up"* (2nd Low Emissions: 35.1 & 2nd Best Green Space)
10. **Prairiebend**: *"The Affordable Alternative"* (2nd Best Affordability: 31.7)
11. **Golden Shoals**: *"The Carbon Struggle"* (2nd Highest Emissions: 57.1)
12. **Ashgrove**: *"The Median Metropolis"* (Consistent middle-tier performance)

### 2. The Analytical View (Context & Distribution)
*Targeting the "Policy Analyst" audience who need to see the full spread, not just 1:1.*

- **Rankings (Bar Charts)**: Small multiples showing all 12 cities for each of the 5 metrics. 
  - Highlight Atlanta in a specific color.
- **Correlations (Scatter Plot)**: 
  - *Housing Affordability* vs *Transit Score*.
  - *Green Space* vs *Emissions*.
  - Show where Atlanta sits in the quadrant (e.g., "High Cost, Low Transit" vs "Balanced").
- **Rank Consistency (Bump Chart)**:
  - Visualize how Atlanta's rank shifts across the 5 different dimensions compared to peers.
  - Highlights if Atlanta is consistently top-tier or specialized (good in some, bad in others).

## Report Structure (Max 5 Pages)

1.  **Executive Summary**: High-level KPI strip + The "Comparison Cards" interactive view.
2.  **Deep Dive Analysis**: Comprehensive rankings, distributions, and correlations across all dimensions (Housing, Transit, Green Space, Emissions).
3.  **About / Methods**: Definitions of metrics and badge criteria.

## Accessibility & Guidelines Checklist
*Contest Requirement: ≥4.5:1 contrast, Alt Text, Tab Order*

- [ ] **Color Palette**: Ensure "Trend" colors (Good/Bad) are color-blind safe (e.g., use Orange/Blue or double encode with Icons).
- [ ] **Tab Order**: Ensure logical navigation through the comparison cards.
- [ ] **Alt Text**: Dynamic alt text measures for the card values (e.g., "Atlanta Housing Score is 95, 5 points higher than selection").
- [ ] **Icons**: Ensure icons are not the *only* way to understand the status (include text labels).

## Data Strategy

- **Tables**: `City Metrics` and `City Lookup`.
- **Calculated Measures Needed**:
  - `[Selected City Metric]`
  - `[Atlanta Metric]` (Hardcoded or filtered calculator)
  - `[Delta %]`
  - `[Trend Direction]` (Logic switch for Emissions where Lower = Better)
  - `[Badge Logic]` (Rank = 1 then "Gold", etc.)

## Supplemental Data Candidates (Contextual Analysis)
*To better answer "Investment Prioritization" questions:*

1.  **Population Density**: 
    - *Why*: Critical context for **Transit Score** and **Green Space**. High density usually justifies high transit investment but makes green space harder to acquire.
2.  **GDP per Capita**: 
    - *Why*: The denominator for specific comparisons. A high Housing cost is less specific if GDP is also double the peers.
3.  **Safety / Crime Index**:
    - *Why*: Often the #1 prioritize for "Livability Stakeholders" and is missing from the core 5.
4.  **Net Migration**:
    - *Why*: The ultimate "vote with your feet" metric. If Livability is high but migration is negative, there is a mismatch.
5.  **Average Commute Time**:
    - *Why*: Validates the "Transit Score". Does a high score actually result in lower commute times?

