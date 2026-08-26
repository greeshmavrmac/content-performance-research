# Tell the Story: From Content Data to Action

## 1. Case Study: The Real FlyRank Content Problem

FlyRank works with large amounts of content-performance data. A practical problem is that not all content performs equally, and it is difficult to identify broader performance patterns by looking at individual metrics separately.

For example, one content item may have many impressions but few clicks, while another may generate stronger traffic and user engagement. Looking at thousands of content items one by one does not provide a clear overall picture.

This project used unsupervised machine learning to group content according to similarities in search visibility, website traffic, and user engagement.

The research question was:

> Can unsupervised machine learning identify distinct content performance archetypes from search visibility, traffic, and user engagement signals?

The analysis used 50,000 aggregated content items from the FlyRank ML Internship Warehouse dataset. Fourteen numerical features were used, including impressions, clicks, average search position, pageviews, sessions, users, engagement metrics, traffic sources, and scroll events.

After handling missing values and standardizing the features, K-Means clustering was evaluated using different numbers of clusters from K = 2 to K = 6.

The silhouette-score comparison showed that K = 2 produced the strongest result.

### What the Analysis Found

The final model identified two broad content-performance archetypes:

- **Higher-Performance Content:** 34,372 items (68.74%)
- **Lower-Performance Content:** 15,628 items (31.26%)

The higher-performance content group showed stronger average performance in impressions, clicks, pageviews, organic sessions, and scroll events.

The groups also differed substantially in average search position:

- Higher-Performance Content: 10.39
- Lower-Performance Content: 41.13

Because lower search-position values represent stronger rankings, the higher-performance group also demonstrated better observed search visibility.

### Why This Matters for FlyRank

The important result is not simply that two clusters were created.

The practical value is that content can be viewed as broader performance archetypes instead of thousands of isolated rows.

This can help answer practical questions such as:

1. **Which content may need attention?**  
   Lower-performing content can be investigated for weak search visibility, traffic, or engagement.

2. **What does stronger-performing content look like?**  
   Higher-performing content provides a comparison group for understanding successful observed performance patterns.

3. **How can content analysis be prioritized?**  
   Clustering can provide a starting point for grouping and investigating content at scale.

The analysis does not prove that any specific feature causes content success. It identifies observed patterns and associations in the selected data.

---

## 2. Five-Minute Demo Outline

### 0:00–0:45 — The Question

The problem was to understand whether a large collection of content items could be grouped into meaningful performance patterns using search visibility, website traffic, and user engagement data.

Instead of manually defining what successful content looks like, I used unsupervised machine learning to let the data identify broader groups.

### 0:45–1:45 — The Data

I used the FlyRank ML Internship Warehouse dataset and aggregated daily observations by content identifier.

This produced a sample of 50,000 content items.

I selected 14 numerical performance features representing search, traffic, acquisition, and engagement.

### 1:45–2:45 — The Method

I handled missing values, standardized the selected features using StandardScaler, and applied K-Means clustering.

I evaluated cluster counts from K = 2 through K = 6 using silhouette scores.

K = 2 produced the highest silhouette score and was selected for the final analysis.

### 2:45–4:00 — The Key Result

The analysis identified two content-performance archetypes.

The Higher-Performance Content group contained 34,372 items, or 68.74% of the sample.

The Lower-Performance Content group contained 15,628 items, or 31.26% of the sample.

The higher-performing group showed stronger observed performance across impressions, clicks, pageviews, organic sessions, and engagement signals.

### 4:00–5:00 — What I Would Do Next

I would use these archetypes as a starting point for deeper content investigation.

For lower-performing content, I would investigate search visibility, traffic acquisition, relevance, readability, and user engagement.

For higher-performing content, I would study the characteristics associated with stronger observed performance and compare similar content items.

The main limitation is that clustering identifies patterns and associations. It does not establish causation.

---

## 3. Shareable Cut: Social Post

I analyzed 50,000 aggregated content items using unsupervised machine learning to identify broader content-performance patterns.

Using 14 search, traffic, and engagement features, I tested K-Means clustering with cluster counts from 2 to 6.

The strongest silhouette score was produced by K = 2.

The final analysis identified:

- Higher-Performance Content: 34,372 items (68.74%)
- Lower-Performance Content: 15,628 items (31.26%)

The higher-performing group showed stronger observed performance across search visibility, traffic, and engagement metrics.

What I learned: unsupervised machine learning can help turn a large collection of content-performance records into interpretable groups that provide a starting point for deeper analysis and prioritization.

#MachineLearning #UnsupervisedLearning #KMeans #DataAnalysis #FlyRank

---

## 4. Shareable Cut: Employer-Facing Summary

**What I built:**  
An unsupervised machine learning analysis that grouped 50,000 content items into interpretable content-performance archetypes.

**What data I used:**  
Aggregated FlyRank content-performance data with 14 numerical features covering search visibility, website traffic, acquisition, and user engagement.

**What I found:**  
K-Means clustering identified two broad archetypes. The higher-performing group contained 68.74% of the analyzed content and showed stronger observed performance across impressions, clicks, pageviews, organic sessions, and engagement metrics.

**Why it matters:**  
The project demonstrates how machine learning can help transform a large collection of performance records into broader groups that can support investigation and prioritization.

**My key takeaway:**  
I learned how to move from raw data to preprocessing, feature standardization, unsupervised modeling, model evaluation, visualization, interpretation, and communicating results in a practical business context.

