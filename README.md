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

- **Higher-Performance Content**: 34,372 items (68.74%)
- **Lower-Performance Content**: 15,628 items (31.26%)

The higher-performing archetype showed stronger impressions, clicks, pageviews, organic sessions, scroll events, and search position.

## Project Structure

```
content-performance-research/
│
├── README.md                          # This file
│
├── website/                           # Website and publication files
│   └── index.html                    # Research paper website
│
├── images/                            # Research visualizations
│   ├── figure1.png                   # Content archetype distribution
│   ├── figure2.png                   # Performance comparison
│   ├── figure3.png                   # Normalized performance comparison
│   ├── figure4.png                   # PCA visualization
│   └── figure5.png                   # Silhouette-score comparison
│
├── notebooks/                         # Jupyter notebooks organized by week
│   ├── week01/
│   │   └── 01_research_question.ipynb
│   │
│   ├── week02/
│   │   ├── 02_ml_task_framing.ipynb
│   │   └── 02_readable_model.ipynb
│   │
│   ├── week03/
│   │   └── 03_data_contract.ipynb
│   │
│   ├── week04/
│   │   └── 04_baseline_score.ipynb
│   │
│   └── discovery/
│       └── 01_first_look_and_discovery.ipynb
│
├── submissions/                       # Project submissions
│   └── paper_url.txt                 # Deployed paper URL
│
└── work/                              # Work summaries and narratives
    ├── employer_summary.md
    ├── social_summary.md
    └── tell_the_story.md
```

## Project Website

https://greeshmavrmac.github.io/content-performance-research/

The website displays the complete research findings with interactive visualizations and detailed methodology.

## Technologies Used

Python, DuckDB, Pandas, NumPy, Scikit-learn, HTML, and CSS.

## Data Credit

This project uses the FlyRank ML Internship Warehouse dataset. The analysis uses aggregated and pseudonymized content-performance data.

## Repository Organization

This repository has been organized for clarity and maintainability:

- **notebooks/**: All Jupyter notebooks organized by week of work
- **website/**: GitHub Pages HTML with all figures properly linked
- **images/**: All PNG visualizations in a dedicated folder
- **work/**: Summary documents and narratives
- **submissions/**: Project submission files

All cross-references and paths have been updated to reflect the new structure. The GitHub Pages site serves from `website/index.html` with images correctly referenced from `../images/`.
