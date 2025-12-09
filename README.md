# Task_04_Descriptive_Stats


Analysis of political social media engagement during the 2024 U.S. presidential election.
This project computes descriptive statistics using three approaches: pure Python, Pandas, and Polars
on identical datasets to compare performance and methodology.

Dataset: https://drive.google.com/file/d/1Jq0fPb-tq76Ee_RtM58fT0_M3o-JDBwe/view

Repository Organization:
scripts/
├── pure_python_stats.py    # Statistics computed with standard library
├── pandas_stats.py          # Statistics computed with Pandas
├── polars_stats.py          # Statistics computed with Polars
.gitignore                   # Excludes data files from version control
README.md                    # Project documentation

Note: Dataset files are not included in the repository due to size constraints.
Place datasets in a `data/` directory before executing scripts.

Execution Instructions:
# Standard library approach
python scripts/pure_python_stats.py

# Pandas-based approach
python scripts/pandas_stats.py

# Polars-based approach
python scripts/polars_stats.py

Key Findings:

Dataset Overview:
- Contains approximately 250,000 Facebook advertisements and posts
- Features include: page_id, ad_id, spending estimates, impression counts, topic indicators

Analytical Operations:
- Aggregations performed on page_id
- Combined aggregations on page_id and ad_id
- Performance comparison across three computational approaches

Performance Observations:
- Polars demonstrated superior speed for aggregation operations
- Pure Python required substantially more code for equivalent functionality
- Polars demanded attention to schema definitions and type handling

Insights from Descriptive Analysis:

1. Distribution of Advertising Sources
   A concentrated pattern emerged where a limited set of pages generated the bulk of content.
   One page produced over 55,000 advertisements, suggesting coordinated campaign efforts.
   Ad identifiers showed minimal duplication, indicating unique tracking per advertisement.

2. Financial Spending Patterns
   Significant variation in average spending across different pages
   Combined page and ad-level groupings revealed diverse targeting strategies
   Mix of low-budget targeted ads and high-investment broad campaigns

3. Platform and Audience Characteristics
   USD dominated as the primary currency (>99% of records)
   Minor presence of international currencies (INR, GBP, EUR)
   Facebook and Instagram were the primary distribution platforms
   Geographic and demographic fields showed sparse or nested data structures

Comparative Tool Assessment:
- Pandas: Enhanced readability and exploratory workflows
- Polars: Superior computational efficiency on large datasets (~250k rows),
  requires syntax adaptation for certain operations
- Pure Python: Educational value for understanding algorithms, limited scalability
