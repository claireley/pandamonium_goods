# Project overview
...

# Installation

1. **Clone the repository**:

```bash
git clone https://github.com/YourUsername/repository_name.git
```

2. **Install UV**

If you're a MacOS/Linux user type:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

If you're a Windows user open an Anaconda Powershell Prompt and type :

```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

3. **Create an environment**

```bash
uv venv 
```

3. **Activate the environment**

If you're a MacOS/Linux user type (if you're using a bash shell):

```bash
source ./venv/bin/activate
```

If you're a MacOS/Linux user type (if you're using a csh/tcsh shell):

```bash
source ./venv/bin/activate.csh
```

If you're a Windows user type:

```bash
.\venv\Scripts\activate
```

4. **Install dependencies**:

```bash
uv pip install -r requirements.txt
```

# Questions 
...

# Dataset 
...

## Main dataset issues

- ...
- ...
- ...

## Solutions for the dataset issues
...

# Conclussions
...

# Next steps
...



# PandaMonium: Penetrating the Amazon Ecosystem
### 🐼 A Data-Driven E-Commerce Launch Strategy for PandaMonium Goods

---

## 🎯 Executive Summary & Analytical Framework

This research initiates an investigative, data-driven framework to solve structural growth and positioning challenges for PandaMonium Goods. To scale our brand profitably without engaging in capital-intensive price wars against entrenched corporate giants, this meta-analysis evaluates a foundational e-commerce matrix containing **1,465 validated Amazon product listings**. 

The core analytical engine processes this listing data to systematically evaluate three core strategic business questions:
* **Strategic Pricing Freedom (H1):** Does high product pricing naturally signal premium quality to customers and boost overall ratings? Can high price variance (Standard Deviation) be utilized as a strategic green light indicating market segmentation rather than commoditization? How does a high Coefficient of Variation ($CV > 0.75$) grant the freedom to establish a premium brand presence away from race-to-the-bottom price wars?
* **The Discount Cliff (H2):** Do substantial promotional discount rates act as massive emotional anchors that drive customer ratings up, or do they sabotage the product lifecycle? At what specific threshold does a consumer perception penalty trigger, causing buyers to sub-consciously evaluate build quality against the *original full price benchmark* rather than what they paid?
* **Market Gaps (H3):** Can we systematically locate un-commoditized, severe demand-supply imbalances where low competitor product counts are coupled with high review volumes and poor consumer satisfaction scores? How can these friction points be mapped to highlight accessible openings for high-margin, premium accessory entries?

---

## 🏗️ Repository Architecture
```text
├── README.md                          <- Project overview and business roadmap
├── data/
│   └── amazon.csv                     <- Raw source dataset from Kaggle
├── notebooks/
│   └── eda_claire.ipynb               <- Exploratory data analysis & custom plotting pipeline
└── figures/
    ├── fig1_price_vs_rating.png       <- Price segmentation bar charts
    ├── fig2_discount_trap.png         <- Dual-axis discount volume/sentiment cliff
    └── fig3_niche_quality_price.png   <- Opportunity scoring & niche candidate analysis

```

---

## 🛠️ Data Pipeline & Integrity Remediation

The data processing pipeline engineered within the notebook (`eda_claire.ipynb`) utilizes a custom brand asset theme (**PandaMonium Brand Palette**: Forest Dark `#064e3b`, Slate Gray, and Coral accents). During the initialization phase of the project, three core data engineering and structural alignment anomalies were identified:

1. **Currency and Numeric Formatting Faults:** Raw retail data fields were locked as text strings, heavily polluted with native currency symbols (such as `₹`) and structural commas, preventing immediate statistical computation or aggregation.
2. **Hierarchical Category Nesting:** The marketplace classification system stored product categories as deeply nested, delimited strings (e.g., separating parent nodes from child nodes with `|` characters), masking the granular Level-3 subcategories required to locate hyper-specific market gaps.
3. **Extreme Pricing Dispersion:** Raw prices spanned several orders of magnitude across wildly diverse product types (ranging from a budget ₹50 unit to a premium ₹100,000 item), creating severe baseline skew that threatened to distort parent-category mean calculations.

### Technical Executions & System Normalization

To correct these structural anomalies and secure the data pipeline against skewing risks, the processing engine deployed the following precise programmatic workflows:

* **Regex-Driven Price Cleansing:** Built an automated scrubbing process that systematically stripped out currency symbols and commas, casting the remaining values into clean, operational mathematical floats (`float64`).
* **Categorical String Parsing:** Developed a string tokenization split-sequence to isolate specific Level-3 e-commerce product nodes, separating high-level generic buckets from local, exploitable accessory categories.
* **Volatility Metrics & Price Dispersion:** Instead of relying on vulnerable parent-category averages, the system engineered the **Price Coefficient of Variation (CV)** per specific sub-category to measure baseline price dispersion independently of scale:

$$CV = \frac{\sigma}{\mu}$$



This mathematical step successfully isolated categories with genuine pricing elasticity from rigid, low-margin commodity traps.

---

## 📊 Empirical Data Discoveries & Strategic Alignment

The complete analytical suite disproved common retail assumptions and delivered clear data metrics to safeguard future brand assets:

### The Realities of Premium Pricing (Refutation of H1)

Expensive products do not act as a direct gateway to positive reviews. While premium items often feature higher manufacturing value, they simultaneously trigger hyper-critical customer expectations. The true sweet spot for margin stability exists within value-based tiers where consumer expectations remain balanced.

### The Dynamics of the Discount Trap (Validation of H2)

Aggressive promotional discounts exceeding a **40% to 60% threshold** trigger an immediate drop in customer perception. When markdown rates are pushed to the extreme, the product's quality signal is subverted, causing lifecycle customer satisfaction ratings to plunge toward a 3.6 baseline.

### Exploiting Supply Imbalances (Validation of H3)

The automated opportunity scoring pipeline ($f(\text{Low Rating}) + f(\text{High Pricing CV})$) successfully bypassed corporate review walls to identify highly exploitable demand imbalances. Two premium, un-commoditized market gaps stood out as immediate revenue opportunities:

| Product Target | Ecosystem Anchor | The Strategic Opportunity | Target Launch Position |
| --- | --- | --- | --- |
| **Audio Condensers** | 4.5M+ Review Audio Space | Captures a highly frustrated premium creator niche suffering under a low **3.92 category average**. | **Premium Bracket (+15-20% above anchor)** |
| **Premium Dust Covers** | 2.3M+ TV & Appliance Space | A low-capital asset protection play riding the coattails of legacy hardware traffic on expensive appliances (Smart TVs, Mixers), allowing the brand to monetize high-variance hardware spaces without any engineering, factory tooling, or R&D risk. | **Asset Insurance Play (5-10% of total machine value)** |

---

## 🚀 Operational Deployment Roadmap

To transition these analytical conclusions into immediate operational execution and ensure repeatable e-commerce success, the product development and launch divisions will implement the following structured workflow (The Panda Path):

```
[Phase 1: Identify Moat] ➔ [Phase 2: Funnel Filter] ➔ [Phase 3: Premium Targeting] ➔ [Phase 4: Promotional Guardrails]

```

* **Phase 1 — Operational Auditing & Pricing Dispersion:** Measure price dispersion ($\sigma$) to verify high pricing freedom and segmentation in the target L3 subcategory. Audit quarterly level-3 subcategory performance, filtering specifically for nodes demonstrating a high Coefficient of Variation before allocating manufacturing assets.
* **Phase 2 — The Funnel Filter & Competitor Log Review:** Map out the target category and locate the high-volume "Goliaths" sitting at the narrow, right-hand end of the Regression Funnel. Review their negative review logs to isolate the exact manufacturing and functional flaws consumers are willing to spend more money to fix.
* **Phase 3 — Premium Targeting & Value Anchoring:** Position the PandaMonium asset at a 15–20% premium directly above market anchors, utilizing the added margin to explicitly resolve and fix the anchor's primary 1-star complaints. For dust covers, apply an asset-insurance model pricing the cover at **5% to 10% of the total machine value** to leverage existing premium anchoring.
* **Phase 4 — Promotional Guardrails & Asset Shielding:** Enforce hardcoded markdown limits in the brand's promotional calendar, capping all introductory and holiday discounts to a **strict maximum of 40%** to completely shield the product line from the rating erosion of the Discount Cliff.

---

### 📝 Project Contact

* **Team:** PandaMonium Goods Launch Strategy Division
* **Email:** [pandamonium.strategy@analysis.edu]()
* **Dataset Reference:** [Kaggle Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset/data)

