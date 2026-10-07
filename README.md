# Apartments Prices Analysis (Excel)

Real estate data analysis project using Excel to clean, analyze, and visualize **5,526 apartment listings** (prices in EGP) and uncover what drives property prices.


<img width="607" height="631" alt="Screenshot 2026-09-26 205045" src="https://github.com/user-attachments/assets/8fd88212-da73-48a8-8ac8-b00a90aafff2" />


## Business Questions

1. What does the real-estate market look like?
2. What factors are associated with property prices?
3. What factors drive price per square meter?
4. How does property age affect value?
5. How do seller type and payment method relate to pricing?

## Dataset

- **5,526 listings**, 13 original columns
- Key fields: `price`, `area_sqm`, `Rooms`, `Bathroom`, `floor_level`, `year_built`, `seller_type`, `view`, `payment_method`, `finishing_type`

## Data Cleaning & Preparation

- `price_per_sqm` was stored as **text with units** (e.g. `18,025 EGP/M²`), so it could not be used in calculations. I created a clean **numeric Price per m²** column.
- Created **Area Group** bins: `<80`, `80:120`, `120:180`, `180:250`, `>250` m².
- Created **Property Development Stage** from `year_built`:

| Stage | Year Built |
|---|---|
| Older Properties | 1980 - 1999 |
| Established Properties | 2000 - 2019 |
| Recent Properties | 2020 - 2026 |
| Near Completion | 2027 - 2028 |
| Under Construction | 2029 - 2030 |

- Built PivotTables and an interactive dashboard on top of the cleaned table.

## Key Insights

**Market overview**
- Average price: **5.9M EGP** | Median: **4.9M EGP** | Average area: **145 m²** | Average price/m²: **43.1K EGP**
- The average sits above the median, so a group of high-priced properties pulls the average up.

**What drives price**
- **Size:** properties above 250 m² average **10.0M EGP**, compared with **3.5M EGP** for those under 80 m² (about 3x).
- **Rooms:** 5-room apartments average **11.9M EGP** vs **3.8M EGP** for 1-room (about 3x).
- **View:** Nile View is the most expensive at **13.2M EGP** on average, vs **3.7M EGP** for Back view (about 3.5x).

**What drives price per m²**
- **View:** Nile View reaches **93.2K EGP/m²**, while Side Street is the lowest at **27.3K EGP/m²** (about 3.4x).
- **Finishing:** Extra Super Lux (47.5K) and Super Lux (46.8K) lead, while Lux (32.3K) comes in lowest, even below Without Finish (33.8K).
- **Development stage:** Under Construction units have the highest price/m² (**61.0K**), followed by Near Completion (48.3K). Older properties are the cheapest per m² (26.4K).

**Payment method**
- 46% of listings are Cash, 32% Installments, and 22% accept both.

## Tools

Microsoft Excel: Power Query, PivotTables, formulas (MEDIAN, GETPIVOTDATA), charts and dashboard design.

## Files

| File | Description |
|---|---|
| `Apartments_Prices_Dataset_Edited.xlsx` | Raw data, cleaned data, pivot report, and dashboard |
| `dashboard.png` | Dashboard screenshot |

## Author

**Ziad Amr** - www.linkedin.com/in/ziadamrr

