# 📊 Superstore Sales BI Analysis

A comprehensive data-driven revenue optimization strategy for retail operations, combining Python analytics with interactive Power BI dashboards to identify product-level discount opportunities and seasonal demand patterns.

## 🎯 Project Overview

This project addresses sales inefficiencies caused by reactive, "one-size-fits-all" discount strategies. By leveraging transaction-level data analysis and a 5-quadrant product classification system, we provide actionable insights for:

- **WHERE**: Identifying high-priority regions and states
- **WHICH**: Classifying products into strategic categories (Star, Luxury, Traffic Builder, New/Niche, Dead Zombie)
- **WHEN**: Timing discounts based on seasonality index patterns

## 📁 Repository Structure

```
Superstore-Sales-BI-Analysis/
│
├── Superstore Sales Analysis.ipynb    # Main Jupyter notebook with full analysis
├── create_executive_report.py         # Script to generate Word report
├── train.csv                          # Raw sales data
├── train_clean.csv                    # Cleaned dataset
├── BI Dashboard.pbix                  # Power BI dashboard file
├── Executive_Summary_Report_FINAL.docx # Executive summary document
├── *_seasonality.png                  # Seasonality heatmaps (NY, CA, TX, FL)
└── README.md                          # Project documentation
```

## 🔍 Business Problem

Despite revenue growth, Superstore suffers from sales inefficiencies due to blanket discount strategies applied without considering:
- Product-level performance metrics
- Regional demand variations
- Seasonal demand patterns

**Result**: Unnecessary discounts on high-demand items and missed opportunities on slow-moving inventory.

## 🛠️ Methodology

### 5-Quadrant Product Classification System

Products are classified based on **Value** (total sales) and **Volume** (order frequency) relative to their sub-category peers:

1. **⭐ Star Products (Protect)**: High value + High volume → Never discount, protect margins
2. **💎 Luxury Products (Target)**: High value + Low volume → Exclusive offers, no public discounts
3. **🔄 Traffic Builders (Bundle)**: Low value + High volume → Aggressive bundling strategies
4. **🆕 New/Niche (Watch List)**: New products (<180 days) → Monitor and bundle with stars for exposure
5. **☠️ Dead Zombies (Liquidate)**: Old + Underperforming → Aggressive clearance

### Seasonality Analysis

Seasonality Index is calculated for each sub-category by month:
- **Peak Season** (Index >1.2): Harvest period, focus on premium sales
- **Normal Period** (Index 0.8-1.2): Standard operations
- **Valley Period** (Index <0.8): Discount deployment window

## 📊 Key Findings

### National Performance
- **Portfolio Mix**: 623 Star products, 986 Dead Zombies across 4 priority states
- **Regional Leader**: West region (CA-focused) drives highest revenue
- **Seasonal Peaks**: Q4 dominates (holiday shopping), September-December surge

### State-Level Insights

| State | Stars | Luxury | Traffic | Zombies | New/Niche |
|-------|-------|--------|---------|---------|-----------|
| **New York** | 154 | 253 | 72 | 244 | 81 |
| **California** | 308 | 289 | 128 | 361 | 97 |
| **Texas** | 133 | 249 | 40 | 265 | 70 |
| **Florida** | 28 | 143 | 11 | 116 | 35 |

## 💻 Technologies Used

- **Python 3.13**
  - `pandas` & `numpy`: Data manipulation
  - `matplotlib` & `seaborn`: Visualization
  - `statsmodels`: Time series decomposition
  - `python-docx`: Report generation
  
- **Power BI**: Interactive dashboard development
- **Jupyter Notebook**: Analysis documentation
- **Microsoft Word**: Executive reporting

## 🚀 Getting Started

### Prerequisites

```bash
python 3.13+
jupyter notebook
Power BI Desktop (for dashboard viewing)
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/moyez48/Superstore-Sales-BI-Analysis.git
cd Superstore-Sales-BI-Analysis
```

2. **Set up Python environment**
```bash
# Create virtual environment (optional but recommended)
python -m venv .venv
.venv\Scripts\activate  # On Windows
source .venv/bin/activate  # On Mac/Linux

# Install required packages
pip install pandas numpy matplotlib seaborn statsmodels scipy python-docx
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook "Superstore Sales Analysis.ipynb"
```

4. **Generate Executive Report**
```bash
python create_executive_report.py
```

## 📈 Viewing the Power BI Dashboard

### Option 1: Download Power BI Desktop (Recommended)

1. **Download Power BI Desktop** (Free)
   - Visit: https://powerbi.microsoft.com/desktop/
   - Click "Download free"
   - Install the application

2. **Open the Dashboard**
   - Download `BI Dashboard.pbix` from this repository
   - Double-click the file or open it from Power BI Desktop
   - Navigate through interactive pages:
     - Overview Dashboard
     - Product Portfolio Analysis
     - Regional Performance
     - Seasonality Patterns
     - Strategic Recommendations

3. **Refresh Data** (if needed)
   - Click "Refresh" in the Home ribbon
   - Ensure `train_clean.csv` is in the same directory

### Option 2: View Static Reports

If you cannot install Power BI Desktop:
- Review the **Executive_Summary_Report_FINAL.docx** for high-level insights
- Examine **seasonality heatmap images** (ny_seasonality.png, ca_seasonality.png, etc.)
- Run the Jupyter notebook for detailed analysis

## 📋 Analysis Workflow

1. **Data Preprocessing**: Clean raw data, handle missing values, create temporal features
2. **Exploratory Data Analysis**: Identify trends, patterns, and outliers
3. **Regional Deep-Dive**: Focus on top-performing states using "Kingmaker Rule"
4. **Product Classification**: Apply 5-quadrant matrix to all products
5. **Seasonality Mapping**: Calculate monthly seasonality index by sub-category
6. **Strategic Framework**: Combine product class × seasonality for actionable recommendations
7. **Visualization**: Create interactive Power BI dashboard and executive reports

## 🎯 Strategic Recommendations

### By Product Class & Seasonality

**Star Products**:
- Valley: Never discount, maintain brand positioning
- Normal/Peak: Bundle with New/Niche for cross-promotion

**Luxury Products**:
- Valley: Exclusive access programs, premium services
- Peak: B2B focus, corporate gifting programs

**Traffic Builders**:
- Valley: Aggressive discounts (20-30% off)
- Normal/Peak: Bulk bundling only, protect individual margins

**Dead Zombies**:
- All periods: Continuous clearance (40-60% off)

## 📊 Results & Impact

- **Data-Driven Segmentation**: 2,804 products classified into strategic categories
- **Regional Prioritization**: 4 states identified for focused optimization (NY, CA, TX, FL)
- **Seasonality Mapping**: 17 sub-categories analyzed across 12 months
- **Executive Documentation**: Professional consulting-style report for stakeholder communication

## 📝 Data Source

**Dataset**: Global Superstore Sales (2022-2025)
- Transaction-level sales data
- 49 US states, 4 regions
- 3 categories, 17 sub-categories
- 1,850+ unique products

**Note**: Row ID count is used as a proxy for volume/frequency due to missing Quantity column in the dataset.

## 🤝 Contributing

This is a portfolio project, but feedback and suggestions are welcome! Feel free to:
- Open issues for questions or suggestions
- Fork the repository for your own analysis
- Share insights or alternative approaches

## 📧 Contact

- GitHub: [@moyez48](https://github.com/moyez48)
- Repository: [Superstore-Sales-BI-Analysis](https://github.com/moyez48/Superstore-Sales-BI-Analysis)

## 📄 License

This project is open source and available for educational and portfolio purposes.

---

**⭐ If you found this analysis helpful, please consider starring the repository!**
