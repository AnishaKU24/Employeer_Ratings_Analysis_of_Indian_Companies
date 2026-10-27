# Employeer_Ratings_Analysis_of_Indian_Companies


Industry distribution, headquarters concentration, and employer-rating patterns in the Companies in India dataset

An exploratory data analysis (EDA) in Python of the Kaggle dataset Companies in India. The project cleans the raw file, explores how companies are spread across industries and headquarters cities, and looks at how ratings, review counts, and other employer-profile metrics relate to each other.

Dataset at a glance
Item	Detail
File	Companies_in_India.csv
Raw size	10,000 rows x 11 columns (including an unnamed index column)
After cleaning	9,402 companies, 12 columns (index dropped, hq_city and other_locations added)
Granularity	One row per company

Columns

Column	Meaning
name	Company name
rating	Average employee rating (1.0 to 5.0)
company_type	Industry / sector label (84 distinct values after cleaning)
hq	Headquarters city plus number of other locations, e.g. Bengaluru +445 other locations
number_of_reviews, salaries, interviews, jobs, benefits, photos	Counts of employer-profile items, stored as text such as 1.2L, 74.3k

Important: This is an employer-profile dataset (ratings, reviews, salary and interview counts). It does not contain registration dates, company status, listing status, or authorized / paid-up capital. Analyses that depend on those fields are out of scope for this data.

Data cleaning
Issue found	Action
Unnamed index column	Dropped
273 shifted rows: the headquarters value sat in company_type and hq was empty	Moved the value back to hq; company_type set to missing
-- used as a missing-value placeholder	Converted to NaN
Counts stored as text with suffixes (k = thousand, L = lakh = 100,000)	Parsed into numbers
HQ text mixed with +N other locations	Split into hq_city and other_locations
City spelling variants (Bangalore / Bengaluru, Gurgaon, Delhi)	Standardized to Bengaluru, Gurugram, New Delhi
598 exact duplicate rows	Removed (10,000 to 9,402)

Remaining missing values after cleaning: photos 5,202, jobs 3,352, company_type 252, a handful in rating, salaries, interviews, and benefits.

The cleaned file is saved at data/cleaned/companies_cleaned.csv.

Key findings

All numbers below come from the cleaned data (9,402 companies).

1. Industry distribution
84 distinct industry labels. The top 10 industries account for 46.4% of companies.
IT Services & Consulting is the largest group (1,222 companies, about 13%), followed by Engineering & Construction (456), Auto Components (408), Industrial Machinery (372), and Pharma (369).

Industries

2. Geographic concentration
Companies are headquartered in 257 distinct cities, but they are highly concentrated: the top 5 cities hold 55.3% and the top 10 hold 80.9%.
Largest hubs: Mumbai (1,445), Bengaluru (1,438), New Delhi (808), Chennai (754), Pune (750), Hyderabad (738), Gurugram (681).

Cities

3. Ratings
Ratings are tightly clustered: mean 3.73, median 3.8. 30.7% of companies rate 4.0 or higher and only 4.3% (407) rate below 3.0.
Among industries with at least 50 companies, the highest averages are Government (4.00), Non-Profit (3.92), Oil & Gas (3.89), Building Material (3.89), and Real Estate (3.89).
The lowest are Accounting & Auditing (3.45), Analytics & KPO (3.45), BPO (3.48), and Management Consulting (3.48).
IT Services & Consulting, the largest industry, averages 3.57, below the overall 3.73.

Ratings Top rated industries

4. City comparison

Average rating differs only slightly between major hubs: New Delhi and Ahmedabad lead at 3.78, and Bengaluru is lowest at 3.67. The spread is small, so city alone is a weak differentiator.

5. Relationships between metrics (Spearman correlation)
number_of_reviews is strongly related to salaries (0.83), interviews (0.79), and benefits (0.74). Larger, better-known employers simply collect more of everything.
number_of_reviews and other_locations correlate moderately (0.57): companies with more locations tend to have more reviews.
Rating is only weakly related to any other metric (about 0.06 with review count, 0.16 with number of locations). Popularity and size do not predict how well a company is rated.

Rating vs reviews

6. Review volume is highly skewed
TCS has the most reviews (120,000), followed by Accenture (74,300), Wipro (65,700), Cognizant (62,100), and Capgemini (54,000).
The top 10% of companies (1,100+ reviews) hold about 61% of all reviews.
Limitations
Not a registry. The data reflects companies with employer profiles on a review platform, not every company registered in India. Findings describe this dataset, not the whole Indian corporate sector.
Selection bias. Every company has at least 111 reviews, so small and new firms are absent. Large IT, services, and consumer-facing employers are likely over-represented.
Ratings are self-reported by employees and can be skewed by who chooses to review.
Industry labels are missing for 252 companies, and jobs and photos are missing for a large share of rows.
Headquarters cities come from a single field; companies with many offices are assigned one city.
24 company names appear more than once with different details after de-duplication; these were kept as separate records.
No registration dates exist, so no time-series or registration-trend analysis was possible.

indian-company-landscape-analysis/
├── data/
│   ├── raw/Companies_in_India.csv
│   └── cleaned/companies_cleaned.csv
├── notebooks/
│   └── company_analysis.ipynb
├── images/
│   ├── industries.png
│   ├── cities.png
│   ├── ratings.png
│   ├── top_rated_industries.png
│   └── rating_vs_reviews.png
├── analysis.py              # same analysis as a script
└── README.md


