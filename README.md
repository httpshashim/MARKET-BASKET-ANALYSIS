# Market Basket Analysis Internship Project

## Overview
This project applies Market Basket Analysis (MBA) to the Online Retail II dataset, using R and the Apriori algorithm to discover meaningful associations between products. It aims to extract actionable insights for retail optimization, product recommendations, and marketing strategies, with a focus on practical application to ecommerce markets such as the UAE.

## Dataset
- Source: Online Retail II (UCI Machine Learning Repository)  
- Size: 1,067,371 transactions  
- Features: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, Price, CustomerID, Country  
- Time Period: Dec 2009 - Dec 2011

## Objectives
- Data cleaning and preprocessing to ensure quality  
- Transformation of raw transactions into market baskets  
- Mining frequent itemsets and association rules using Apriori  
- Visualizing and interpreting strong product associations  
- Building a recommendation system based on shopping baskets  
- Exporting results for business reporting and further analysis

## Methodology

### 1. Data Preprocessing
- Removed transactions with missing CustomerID or Description  
- Filtered out cancelled orders and negative quantity/price records  
- Removed outlier transactions beyond the 99th percentile quantity

### 2. Market Basket Creation
- Grouped products by InvoiceNo to represent baskets  
- Converted lists into `arules` transactions for analysis

### 3. Association Rule Mining
- Applied Apriori algorithm with minimum support=1% and confidence=50%  
- Filtered rules by lift > 1.2 to retain strong associations

### 4. Analysis & Visualization
- Examined frequent item distributions  
- Analyzed key rules by support, confidence, and lift  
- Created scatter plots, grouped matrix plots, network graphs  

### 5. Product Recommendations
- Designed a function to suggest complementary products based on basket contents  
- Validated recommendations for sample baskets

## Results
- Final dataset comprised ~800,000 valid transactions  
- Discovered thousands of valuable association rules  
- Identified frequent purchases and useful product bundles  
- Generated recommendations aligned with real purchase behavior  
- Visualizations revealed intuitive insights for business use

## Business Impact
- Enables targeted cross-selling and upselling strategies  
- Optimizes product placement in retail or online platforms  
- Supports personalized marketing campaigns  
- Informs inventory and supply chain decisions  
- Applicable to UAE and global ecommerce environments

## How to Run
1. Load dataset from Kaggle or download CSV  
2. Install required R packages (`arules`, `arulesViz`, `dplyr`, `readxl`, etc.)  
3. Execute sequentially:
   - Data preprocessing  
   - Basket formation  
   - Association rule mining  
   - Visualization and analysis  
   - Recommendation generation  
4. Export results using provided scripts for reporting

## Requirements
- R 4.x or higher  
- R packages: arules, arulesViz, dplyr, readxl, ggplot2, Matrix  

## Files Included
- `market_basket_analysis.Rmd`: Complete R notebook with all steps and commentary  
- `association_rules.csv`: Exported association rules with metrics  
- `top_frequent_items.csv`: Item frequency breakdown  
- Visualizations generated in notebook  

## Future Work
- Incorporate temporal and seasonality analysis  
- Expand to customer segmentation and predictive analytics  
- Improve recommendation engine for real-time use  
- Explore alternative algorithms like FP-Growth for efficiency

## Author
[Your Name]  
Aspiring Data Analyst | Internship Project  
[LinkedIn Profile URL] | [Contact Email]

## License
This project is licensed under the MIT License.

---

*Thank you for reviewing this project! Feel free to reach out for collaboration or feedback.*
