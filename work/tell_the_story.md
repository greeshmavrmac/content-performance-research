<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tell the Story | FlyRank ML Internship</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: #111827;
            color: #e5e7eb;
            line-height: 1.8;
        }

        header {
            background: #1f2937;
            padding: 50px 20px;
            text-align: center;
            border-bottom: 3px solid #2563eb;
        }

        header h1 {
            margin: 0;
            font-size: 2.2rem;
            color: white;
        }

        header p {
            color: #9ca3af;
            margin-top: 10px;
        }

        .container {
            max-width: 1000px;
            margin: auto;
            padding: 30px 20px 60px;
        }

        section {
            background: #1f2937;
            margin-bottom: 25px;
            padding: 30px;
            border-radius: 10px;
            border: 1px solid #374151;
        }

        h2 {
            color: #60a5fa;
            border-bottom: 1px solid #4b5563;
            padding-bottom: 10px;
        }

        h3 {
            color: #d1d5db;
            margin-top: 25px;
        }

        .highlight {
            background: #172554;
            border-left: 5px solid #3b82f6;
            padding: 20px;
            margin: 20px 0;
        }

        .result {
            background: #052e16;
            border-left: 5px solid #22c55e;
            padding: 20px;
            margin: 20px 0;
        }

        .warning {
            background: #3f2a0a;
            border-left: 5px solid #f59e0b;
            padding: 20px;
            margin: 20px 0;
        }

        ul, ol {
            padding-left: 25px;
        }

        .stats {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .stat-box {
            flex: 1;
            min-width: 200px;
            background: #111827;
            border: 1px solid #374151;
            padding: 20px;
            border-radius: 8px;
        }

        .stat-box strong {
            display: block;
            color: #60a5fa;
            font-size: 1.6rem;
        }

        footer {
            text-align: center;
            padding: 30px;
            background: #1f2937;
            color: #9ca3af;
        }

        a {
            color: #60a5fa;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 1.7rem;
            }

            section {
                padding: 20px;
            }
        }
    </style>
</head>

<body>

<header>
    <h1>Tell the Story</h1>
    <p>FlyRank ML Internship — Content Performance Case Study</p>
</header>

<div class="container">

    <section>
        <h2>1. The FlyRank Problem</h2>

        <p>
            FlyRank has large amounts of content-performance data. Each content
            item can generate search impressions, clicks, pageviews, sessions,
            traffic from different sources, and user engagement signals.
        </p>

        <p>
            The problem is that looking at these metrics one content item at a
            time makes it difficult to identify broader performance patterns.
            With thousands of content items, a practical question is whether
            machine learning can identify meaningful groups automatically.
        </p>

        <div class="highlight">
            <strong>Research Question:</strong><br>
            Can unsupervised machine learning identify distinct content
            performance archetypes from search visibility, traffic, and user
            engagement signals?
        </div>
    </section>


    <section>
        <h2>2. What Data Did I Use?</h2>

        <p>
            I used the FlyRank ML Internship Warehouse dataset, focusing on
            aggregated content-performance observations.
        </p>

        <div class="stats">
            <div class="stat-box">
                <strong>50,000</strong>
                Aggregated Content Items
            </div>

            <div class="stat-box">
                <strong>14</strong>
                Numerical Performance Features
            </div>

            <div class="stat-box">
                <strong>2–6</strong>
                Cluster Counts Evaluated
            </div>
        </div>

        <h3>Examples of Features Used</h3>

        <ul>
            <li>Total impressions</li>
            <li>Total clicks</li>
            <li>Average search position</li>
            <li>Total pageviews</li>
            <li>Total sessions</li>
            <li>Total users</li>
            <li>Organic sessions</li>
            <li>Direct sessions</li>
            <li>Referral sessions</li>
            <li>Social sessions</li>
            <li>AI sessions</li>
            <li>Total engagement time</li>
            <li>Engaged sessions</li>
            <li>Total scroll events</li>
        </ul>
    </section>


    <section>
        <h2>3. How Did I Solve the Problem?</h2>

        <ol>
            <li>Aggregated daily observations into content-level records.</li>
            <li>Created a sample of 50,000 content items.</li>
            <li>Selected 14 numerical performance features.</li>
            <li>Handled missing values.</li>
            <li>Standardized the features using StandardScaler.</li>
            <li>Applied K-Means clustering.</li>
            <li>Tested cluster counts from K = 2 to K = 6.</li>
            <li>Used silhouette scores to evaluate cluster separation.</li>
            <li>Used PCA to visualize the final clusters.</li>
        </ol>

        <div class="result">
            <strong>Method Choice:</strong><br>
            K-Means was used because the goal was to group content items based
            on similarities in their combined performance characteristics.
        </div>
    </section>


    <section>
        <h2>4. The Key Result</h2>

        <p>
            The silhouette-score evaluation showed that two clusters provided
            the strongest result among the tested cluster counts.
        </p>

        <div class="result">
            <strong>Selected Model: K = 2</strong><br>
            The two-cluster solution produced the strongest cluster-selection
            result and was used for the final analysis.
        </div>

        <h3>Two Content Performance Archetypes</h3>

        <div class="stats">
            <div class="stat-box">
                <strong>34,372</strong>
                Higher-Performance Content<br>
                68.74% of the sample
            </div>

            <div class="stat-box">
                <strong>15,628</strong>
                Lower-Performance Content<br>
                31.26% of the sample
            </div>
        </div>
    </section>


    <section>
        <h2>5. What Is the Difference Between the Groups?</h2>

        <p>
            The Higher-Performance Content group showed substantially stronger
            observed performance across search visibility, website traffic,
            and engagement metrics.
        </p>

        <ul>
            <li><strong>Impressions:</strong> 17,307.27 vs 2,751.18</li>
            <li><strong>Clicks:</strong> 64.77 vs 2.92</li>
            <li><strong>Pageviews:</strong> 65.90 vs 11.53</li>
            <li><strong>Organic Sessions:</strong> 32.76 vs 1.23</li>
            <li><strong>Scroll Events:</strong> 6.29 vs 1.10</li>
        </ul>

        <div class="highlight">
            <strong>Search Position:</strong><br>
            Higher-Performance Content had an average position of 10.39,
            compared with 41.13 for Lower-Performance Content.
            Because lower search-position values indicate stronger rankings,
            the higher-performing group demonstrated better observed search
            visibility.
        </div>
    </section>


    <section>
        <h2>6. Why Does This Matter for FlyRank?</h2>

        <p>
            The useful outcome is not simply that the algorithm created two
            groups. The practical value is that a large collection of content
            records can now be viewed as broader performance archetypes.
        </p>

        <h3>Possible Use 1: Find Content That Needs Investigation</h3>
        <p>
            Lower-performing content can be prioritized for investigation into
            weak search visibility, low traffic, or weak user engagement.
        </p>

        <h3>Possible Use 2: Learn From Stronger Content</h3>
        <p>
            Higher-performing content can be used as a comparison group when
            investigating the characteristics of content with stronger observed
            performance.
        </p>

        <h3>Possible Use 3: Prioritize Analysis at Scale</h3>
        <p>
            Instead of manually examining thousands of individual records,
            clustering provides a structured starting point for deeper analysis.
        </p>
    </section>


    <section>
        <h2>7. My Recommendation</h2>

        <ol>
            <li>Prioritize content with weak search visibility.</li>
            <li>Investigate content with low impressions and clicks.</li>
            <li>Review content with weak organic traffic.</li>
            <li>Examine low-engagement content for relevance and readability.</li>
            <li>Use higher-performing content as a comparison group.</li>
            <li>Repeat the analysis on newer data because performance can change over time.</li>
        </ol>
    </section>


    <section>
        <h2>8. What I Built</h2>

        <p>
            I built an end-to-end unsupervised machine learning analysis of
            content performance.
        </p>

        <ul>
            <li>Data aggregation</li>
            <li>Feature selection</li>
            <li>Missing-value handling</li>
            <li>Feature standardization</li>
            <li>K-Means clustering</li>
            <li>Silhouette-score evaluation</li>
            <li>PCA visualization</li>
            <li>Performance comparison</li>
            <li>Business-oriented interpretation</li>
        </ul>
    </section>


    <section>
        <h2>9. Important Limitation</h2>

        <div class="warning">
            <strong>This analysis identifies patterns, not causes.</strong><br><br>

            The clusters show observed associations between the selected
            performance metrics. The results do not prove that any specific
            metric causes content to become successful or unsuccessful.
        </div>
    </section>


    <section>
        <h2>10. Final Story</h2>

        <p>
            I started with a large collection of content-performance data and
            a simple question: can machine learning identify broader patterns
            without manually defining what successful content should look like?
        </p>

        <p>
            After aggregating 50,000 content items and analyzing 14 numerical
            features covering search, traffic, and engagement, K-Means clustering
            identified two broad content-performance archetypes.
        </p>

        <div class="result">
            <strong>Final Result:</strong>
            <ul>
                <li>Higher-Performance Content: 34,372 items (68.74%)</li>
                <li>Lower-Performance Content: 15,628 items (31.26%)</li>
            </ul>
        </div>

        <p>
            The project demonstrates how unsupervised machine learning can turn
            a large collection of raw performance records into interpretable
            patterns that can support further content analysis and prioritization.
        </p>
    </section>

</div>

<footer>
    <p>FlyRank ML Internship — Tell the Story Case Study</p>
    <p>
        <a href="index.html">View the Full Research Paper</a>
    </p>
</footer>

</body>
</html>
