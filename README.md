
# Identifying Content Performance Archetypes Using Unsupervised Machine Learning

## FlyRank ML Internship Capstone Research

This project uses unsupervised machine learning to identify meaningful patterns in content performance using search visibility, website traffic, and user engagement signals.

## Research Question

Can unsupervised machine learning identify distinct content performance archetypes from search visibility, traffic, and user engagement signals?

## Dataset

FlyRank ML Internship Warehouse dataset.

The analysis used the `fact_content_daily_performance` dataset and a sample of 50,000 aggregated content items.

## Methodology

- Data aggregation by `content_hash_id`
- Selection of 14 numerical performance features
- Missing-value handling
- Feature standardization using StandardScaler
- K-Means clustering
- Silhouette-score evaluation for K = 2 to K = 6
- PCA visualization of the final clusters

## Final Results

Two content performance archetypes were identified:

- Higher-Performance Content: 34,372 items (68.74%)
- Lower-Performance Content: 15,628 items (31.26%)

The higher-performing archetype showed stronger impressions, clicks, pageviews, organic sessions, scroll events, and search position.

## Project Website

https://greeshmavrmac.github.io/content-performance-research/

## Project Files

- `index.html` — Research paper website
- `figure1.png` — Content archetype distribution
- `figure2.png` — Performance comparison
- `figure3.png` — Normalized performance comparison
- `figure4.png` — PCA visualization
- `figure5.png` — Silhouette-score comparison
- `submissions/paper_url.txt` — Deployed paper URL

## Technologies Used

Python, DuckDB, Pandas, NumPy, Scikit-learn, HTML, and CSS.

## Data Credit

This project uses the FlyRank ML Internship Warehouse dataset. The analysis uses aggregated and pseudonymized content-performance data.
