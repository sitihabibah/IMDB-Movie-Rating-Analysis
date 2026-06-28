# IMDb Movie Insights & Analysis Dashboard 🎬🍿

An interactive data analytics and visualization project exploring historical cinematic patterns from a curated top-100 IMDb movie dataset. The project bridges raw data engineering with interactive storytelling, moving from a multi-stage data preparation pipeline in Excel to dynamic analytical charts built using **Tableau**.

---

## 📌 Project Objectives
The core purpose of this project is to unearth structural trends across major motion pictures over time by addressing key cinematic questions:
* Which globally acclaimed films command the highest engagement through user reviews and votes?
* Where are the primary operational hubs for top-performing movie productions?
* How are movie qualities distributed according to viewer ratings (IMDb score)?
* What does the historical distribution line tell us about the frequency of film releases past the mid-20th century?

---

## 🛠️ Data Pipeline & Preparation
The raw data originally obtained from [Kaggle](https://www.kaggle.com/datasets/davidfuenteherraiz/messy-imdb-dataset) contained inconsistencies typical of real-world datasets. Extensive preprocessing was executed within the source file `messy_IMDB_dataset.xlsx` to render the dataset analysis-ready:

1. **Deduplication & Completeness:** Screened historical entries to delete duplicate records and handled missing data gaps across attributes.
2. **Text Standardization:** Standardized genres, country names, rating schemas, and stripped leading/trailing spaces across text objects.
3. **Feature Engineering & Extraction:** Parsed and cleaned mixed text values to reliably extract the clean **Release Year**, duration numerical formats, and standardized score scalars.

### Final Dataset Features (11 Variables across 100 Movies):
* `IMBD title ID`: Unique identifier for each movie item.
* `Original Title`: Official release name of the motion picture.
* `Release year`: Clean 4-digit calendar year of theatrical debut.
* `Genre`: Categorical taxonomy classifying the film style.
* `Duration`: Total running time of the film.
* `Country`: Country of production origin.
* `Content Rating`: Maturity audience rating classification (e.g., R, PG-13).
* `Director`: Full name of the primary creative visionary behind the film.
* `Income`: Worldwide commercial box-office gross revenue.
* `Votes`: The total count of registered audience review scores.
* `Score`: Calculated raw numerical rating score out of 10.

---

## 📊 Tableau Dashboard Architecture & Modules
The presentation tier, captured in `imdb_dashboard_preview.png`, features an executive sleek dark mode layout embedded with quick-glance cross-filtering KPI blocks.

### 1. Highlight Cards / Dynamic Overview Panel
* Serves as a dynamic lookup panel reflecting chosen granular values such as *Director* (e.g., Frank Darabont), *Country* (e.g., United States), *Original Title*, *Content Rating*, *Duration*, *Score*, *Votes*, and *Release Year*.

### 2. Popular Movie by Votes (Packed Bubble Chart)
* Visualizes audience engagement volume. 
* Highlighting absolute historical favorites like *The Shawshank Redemption* (2.3M votes), *The Dark Knight* (2.2M votes), *Inception* (2.0M votes), and *Pulp Fiction* (1.8M votes), color-scaled by overall rating weight.

### 3. Top Movie Producing Countries (Geographic Map View)
* Maps structural density across global production studios.
* Graphically scales based on country frequencies, immediately pinpointing the **United States** as the dominant market share holder with 64 films, flanked by major global hubs like the United Kingdom, India, and South Korea.

### 4. Most Movies Released After 1990 (Trend Line Chart)
* Evaluates runtime release frequency tracking from historical periods up until 2022.
* Reveals sharp volume spikes in the mid-1990s through the early 2000s, reflecting an expansion period for globally indexed blockbusters.

### 5. Histogram Score (Distribution Bar Chart)
* Bins numerical audience ratings to view standard distribution profiles.
* Pinpoints that the vast majority of the top 100 films aggregate between a **8.1** to **8.6** score bracket, signaling an elite selection cluster.

---

## 💼 Business Recommendations

**1. Content Acquisition Strategy**
Streaming platforms and distributors should prioritize acquiring titles within the 8.1–8.6 IMDb score range — this bracket represents the densest concentration of critically validated, high-engagement films and offers the strongest ROI for licensing investments.

**2. Geographic Production Focus**
With the US accounting for 64% of top-100 films, international studios seeking global distribution appeal should consider US co-production partnerships or align narrative themes with proven Western storytelling frameworks that consistently resonate with global audiences.

**3. Audience Engagement as a Quality Signal**
The strong alignment between vote counts and high scores suggests that audience engagement (votes) is a reliable early signal of long-term critical reception — useful for greenlight decisions on sequel investments or franchise expansions.

**4. Post-1990 Content Dominance**
The sharp volume spike in globally acclaimed films after 1990 reflectsa structural shift in cinematic production quality and global distribution infrastructure. For archival or catalog investments, post-1990 titles represent a significantly higher density of elite-rated content.

---

## 📂 Repository Structure
* **`messy_IMDB_dataset.xlsx`**: The primary data container holding the original raw and cleansed data worksheets mapping the 11 analytical attributes.
* **`imdb_dashboard_preview.png`**: A snapshot export of the finalized Tableau dashboard interface showing layout configurations, themes, and chart elements.

---

## 🚀 How to Experience the Project
1. Download `IMDB Movie Explorer.twbx`
2. Open with **Tableau Desktop** or **Tableau Public** (free) — the dashboard will load instantly with all data embedded.
3. Use the filter panel to explore by Director, Country, Genre, or Content Rating interactively.

---
*Developed as part of a Professional Data Analytics Portfolio.*
