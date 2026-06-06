# Superstore-Sales-Tableau-Dashboard
# Superstore Sales & Profit Performance Dashboard (Tableau)

An interactive Tableau dashboard designed to help Regional Sales Directors monitor overall business health, analyze product category profitability, and identify underperforming states using dynamic geographic filtering.


---

## 🎯 Project Overview & Requirements

*   **Target Stakeholder:** Regional Sales Director
*   **Business Goal:** Track quarterly sales targets, identify underperforming product categories, and analyze geographic profit margins to make data-driven sales decisions.
*   **Core KPI Metrics:**
    *   **Total Sales:** High-level revenue tracker.
    *   **Total Profit:** Overall earnings tracker.
    *   **Profit Margin:** Ratio of profit to sales (`SUM(Profit) / SUM(Sales)`).

---

## 📈 Visual Hierarchy & Design Choices

The dashboard is structured in a **2x2 grid** following a standard reading Z-pattern to optimize visual scanning:

1.  **Top Row (High-Level Overview):**
    *   **KPI Cards:** Quick, 2-second overview of critical metrics (Sales, Profit, Margin).
    *   **Segment Sales (Pie Chart):** Breaks down revenue split by customer segment (Consumer, Corporate, Home Office).
2.  **Bottom Row (Geographic & Product Details):**
    *   **Profit Map (Geographic Map):** Highlights profitable (blue/green) and unprofitable (orange/red) states using a diverging color palette.
    *   **Category Sales (Horizontal Bar Chart):** Compares sales performance by product category. Sorted descending to make high-performing categories instantly recognizable.
3.  **Interactivity:**
    *   **Map Action Filter:** Clicking any state on the map automatically filters all other worksheets (KPIs, bar chart, pie chart) for that state.

---

## 🔍 Key Data Insights Discovered

Using the interactive filters on the dashboard, the following business insights were uncovered:
*   **Regional Profit Issues:** While total sales are strong, several states in the southern region (such as Texas) are operating at a significant net profit loss.
*   **Product Line Drag:** Drilling down into underperforming states reveals that the **Furniture** category—specifically **Tables** and **Bookcases**—is driving the majority of the losses.
*   **Segment Stability:** The **Consumer** segment consistently represents the largest share of sales across almost all states.

---

## 🛠️ How to Recreate This Project

1.  **Connect to Data:** Open Tableau and load the `Sample-Superstore.xlsx` file.
2.  **Build Worksheets:**
    *   **Profit Map:** Double-click `State`, change mark to `Map`, and drag `Profit` to `Color` (Red-Blue diverging).
    *   **Category Sales:** Drag `Category` to `Rows`, `Sales` to `Columns` (set as Horizontal Bar).
    *   **Trend Chart:** Drag `Order Date` (set to Month/Year) to `Columns`, `Sales` and `Profit` to `Rows`, and combine using `Dual Axis`.
    *   **Segment Sales:** Create a Pie Chart using `Segment` (Color) and `Sales` (Angle).
3.  **Assemble Dashboard:** Create a new dashboard (1200 x 800) and arrange worksheets in a 2x2 grid.
4.  **Add Actions:** Enable "Use as Filter" on the Map worksheet container.

---

## 📁 Repository Structure

```text
├── Sample-Superstore.xlsx      # Raw Excel dataset
├── Superstore_Dashboard.twbx   # Tableau packaged workbook
└── README.md                   # Project Case Study
