# 📊 Netflix Content Analysis & Strategy Dashboard


An end-to-end Business Intelligence project analyzing **24,500+ Netflix Titles** to provides key insights on content distribution, rating performance, genre density, and strategic recommendations for catalog optimization. 

## 📌 Table of Contents
- [Executive Summary](#executive-summary)
- [Key Performance Indicators](#key-performance-indicators)
- [Dashboard Layout & Visualizations](#dashboard-layout-visualization)
- [Strategic Recommendations](#strategic-recommedations)
- [Data Modeling & DAX Measures](#data-Modeling-DAX-Measures)
- [Repository Structure](#repository-structure)
- [Data Challenges & Resolution](#data-challenges-resolution)
- [Authour & Acknowledgments](#author-acknowledgements)


## 📖 Executive Summary

Understanding content portfolio distribution and viewer ratings is essential for streaming platforms managing acquisition budgets and subscriber retention. This interactive Power BI dashboard provides a full overview of Netflix's catalog across **24,598 titles**, assesing content ratio(Movies vs Tv Shows),genre distribution,Imdb exposure tiers, and Just- Watching rating classifications.

**Key Objectives:**


1. **Catalog Portfolio Assessment:** Measure ratio parity between Movies(51.63%) and TV Shows(48.37%).
2. **Genre Gap Identification:** Uncover over-indexed vs under represented genre categories.
3. **Engagement Optimization:** Evaluate user sentiment distribution to unlock growth in under-exposed content tiers.


## 💡 Key Performance Indicators (KPIs)


| KPI Metric  |  Value   |Baseline/Target  | Status|
|:--- |:--- |:--- |:---|
|**Total Titles** | 24,598 |Target:25,000|🟡 On Track |   
|**Movies**| 12,700 (51.63%)| Target: 50.00%|🟢 Target Met|
|**TV Shows**| 11,898(48.37%)|Target: 50.00%| 🟢 Target Met|
|**Avg Runtime**|74.01 mins| Target: 75:00 mins|🟢 Target Met|



## 🖼️ Dashboard Visual & Breakdown
**Visual Modules Detailed:**
- **Content Distribution(Donut Chart):** Highlights catalog balance(*12,700* Movies vs *11,898* TV Shows).

- **Top Genres(Horizontal Bar Chart):** Ranks dominant genres (Romance at **1,438**, Science Fictionat **791**,Sport at **303**, War/Military at **152**, Western at **51**).

- **IMDb Rating Tiers(Column Chart):** Categories catalog exposure into Moderate Exposure **(15.5K)**, Low Sample **(5.6K)**, Mainstream Popular**(3.2K)**, and blockbuster.

- **Just_Watch Rating Tiers:** Measures audience reach (Well-Watched leads at **9.2k**,Viral Hits at ****6.0K**, Niche Catalogue at **5.2K**,Obscure at **4.2K**).

- **Vote Rating Split:** Segregates quality scores into Good(**22K** titles), Exceptional(**2K** titles), and Poor.


- **Interactive Slicers:** Header slicers enabling granular filtering by **Release Year**and **Type Filter**(Movies vs Tv Shows).

## 🎯 Strategic Business Recommendations

**1. Rebalance Content Portfolio (Genre Diversification)**
- Insight: Romance represents the vast majority of categorized lead (**1,438** titles), while high-yield segment like Science-friction(**791**) abd Sports(**303**) have significant room for expansion.
- Actionable Step: direct upcoming content acquisition and original production licensing toward mid-budget science friction series and sport documentaries to capture growing niche sub-demographics.

**2. Activate "Moderate Exposure" Back-Catalog**
- Insight: Over **15,500 titles** reside within the Moderate Exposure IMDb tier.
- Actionable Step: Implement dynamic home-screen recommendation carousels(e.g "Hidden Gems You Missed") to funnel active users toward moderate-exposure assets,extending content lifetimevalue(LTV).


**3. Optimize Format  Runtimes for Retention**
- Insight: The overall catalog average runtime sits at **74.01 Minutes**.
- Actionable Step: Focus new acquisition on 60-90 minute feature film formats and standard 45-minute episode TV formats to align with optimal daily viewing sessions.

**4 Re-engage Lower Rating Tiers**
- Insight : Over **9,400 titles** fall into Niche Catalogue or Obscure classification on Just-Watch.
- Actionable Step: Run targeted push notifications and specialised email campaigns for dedicated genre fans to surface obscure titles and decrease user churn.

  ## 🛠️ Data Modeling & DAX Measures

  The solution utilizes a clean Star Schema data model built in Power BI with custom DAX calculations.


   **Key DAX Formula Used:**

   **DAX**


   ```% Tv shows = DIVIDE([TV Shows],[Total Title]) ```

  ```Total Title = COUNTROWS(netflix_genre_titles)```

  ```Avg runtime = AVERAGE(netflix_genre_titles[runtime])```

  ## 📁 Repository Structure

  **Dashboard Preview**


  [Netflix Content Analysis Dashboard](https://github.com/user-attachments/assets/ec51a07e-2e1f-445c-9fdc-1a58703bd1dc)

  
  ## ⚠️ Data Challenges & Resolution
  | **Challenges** | **Resolution**|
  |:--- |:---|
  |**Blank/Missing Values** | Inputed missing numerical data using mean substitution.|
  |**Inconsistent Data Types** | Re-cast colums to explicit, approptiate data types in Power Query.|
  |**Dirty text field**| Clean string column headers and values using `TRIM()` and `Clean()`.|
  |**Delimiter Extraction**| Split combined text strings(e.g multiple production countries by commas) into) into distinct rows and columnsusing Power Query's **Split Column by Delimeter** feature.|
  
  ## 🤝 Author & Acknowledges
  - **Data Analyst:** Izobo Precious Oghenefega | [Profile](https://github.com/Preci0us01)(view here)
  - **Tools Used:** Microsoft Power BI Desktop, DAX, Power Query
  - **Data Sources:**  [Kaggle](https://www.kaggle.com/datasets/imtkaggleteam/netflix) (download here)
