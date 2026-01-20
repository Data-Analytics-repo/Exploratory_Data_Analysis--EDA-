# MY EDA PROJECT - Exploratory Data Analysis

## Project Overview
This project performs a comprehensive Exploratory Data Analysis (EDA) on an automotive dataset containing information about various car models, their specifications, and pricing. The analysis leverages Python libraries for data manipulation, cleaning, and visualization to uncover patterns and insights in the data.

## Dataset Description
The dataset includes **11,916 records** of vehicles with the following features:

### Original Features:
- **Make**: Manufacturer of the vehicle
- **Model**: Vehicle model name
- **Year**: Year of manufacture
- **Engine Fuel Type**: Type of fuel used
- **Engine HP**: Horsepower of the engine
- **Engine Cylinders**: Number of cylinders
- **Transmission Type**: Type of transmission (MANUAL/AUTOMATIC)
- **Driven_Wheels**: Type of drive mode (rear wheel, front wheel, all-wheel)
- **Number of Doors**: Number of doors
- **Market Category**: Category in the market
- **Vehicle Size**: Size classification
- **Vehicle Style**: Style type (Coupe, Convertible, etc.)
- **highway MPG**: Fuel efficiency on highways
- **city mpg**: Fuel efficiency in cities
- **Popularity**: Popularity rating
- **MSRP**: Manufacturer's Suggested Retail Price

## Project Structure
```
MY_EDA_PROJECT/
├── data.csv                    # Raw automotive dataset
├── MY_EDA_Project.ipynb        # Main analysis notebook
└── README.md                   # Project documentation
```

## Data Cleaning & Preprocessing

### Steps Performed:
1. **Feature Selection**: Dropped unnecessary columns that didn't add significant value:
   - Market Category
   - Vehicle Style
   - Engine Fuel Type
   - Popularity
   - Number of Doors
   - Vehicle Size

2. **Column Renaming**: Standardized column names for better clarity:
   - `Make` → `Manufacturer`
   - `Engine HP` → `HP`
   - `Engine Cylinders` → `Cylinders`
   - `Transmission Type` → `Transmission`
   - `Driven_Wheels` → `Drive Mode`
   - `highway MPG` → `MPG-HIGH`
   - `city mpg` → `MPG-CITY`
   - `MSRP` → `PRICE`

3. **Duplicate Removal**: Identified and removed duplicate records to ensure data quality

4. **Missing Value Handling**: Dropped rows with null/missing values to maintain data integrity

### Final Dataset:
After preprocessing, the dataset was reduced to a clean, analysis-ready format with no missing values or duplicates.

## Analysis & Visualizations

### 1. Outlier Detection
- **Box plots** created for:
  - Price distribution (identifying high-value outliers)
  - Engine HP (horsepower outliers)
  - Engine Cylinders (cylinder count distribution)

### 2. Categorical Analysis
- **Bar charts** showing:
  - Top 40 manufacturers by vehicle count
  - Price distribution across different vehicle price points

### 3. Correlation Analysis
- **Heatmap** visualization showing correlations between numerical features
- Identifies relationships between:
  - HP and Price
  - Cylinders and Price
  - Year and Price
  - MPG metrics and other variables

### 4. Relationship Analysis
- **Scatter plots** examining:
  - HP vs Price correlation
  - Cylinders vs Price relationship

These visualizations reveal how vehicle specifications directly influence pricing in the automotive market.

## Key Findings

1. **Engine Power Impact**: Higher horsepower vehicles tend to have significantly higher prices
2. **Cylinder Count**: More cylinders correlate with increased vehicle price
3. **Manufacturer Distribution**: Certain manufacturers dominate the market with higher production volumes
4. **Price Variability**: Wide range of prices across the dataset, indicating diverse market segments

## Libraries Used
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization

## Requirements
To run this project, ensure you have Python 3.x installed with the following packages:

```bash
pip install pandas numpy matplotlib seaborn
```

## How to Use

1. **Setup Environment**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Run Analysis**:
   - Open `MY_EDA_Project.ipynb` in Jupyter Notebook or VS Code
   - Execute cells sequentially to perform the analysis
   - View visualizations and insights generated

3. **Customize Analysis**:
   - Modify filtering criteria to focus on specific manufacturers or years
   - Add additional visualizations as needed
   - Extend analysis to include predictive modeling

## Insights for Data-Driven Decisions

This EDA provides valuable insights for:
- **Market Analysis**: Understanding vehicle market segmentation and trends
- **Pricing Strategy**: Identifying key factors that influence vehicle pricing
- **Consumer Preferences**: Analyzing which features are most common in the market
- **Competitive Analysis**: Benchmarking manufacturers against market trends

## Author
**Data Analyst Project**

## Project Date
January 2026

## License
This project is open for educational and analytical purposes.

---

**Note**: Data path in the notebook may need to be updated when run on different systems. Ensure the `data.csv` file is in the same directory as the notebook for optimal execution.
