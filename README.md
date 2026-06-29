# 🎵 Spotify Top 50 World — Power BI Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![CSV](https://img.shields.io/badge/Dataset-CSV-1DB954?style=for-the-badge&logo=files&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Measures-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-1DB954?style=for-the-badge)

> An interactive Power BI dashboard analyzing Spotify's global Top 50 World chart data across **May 2023 – November 2024**, covering song popularity, artist dominance, release trends, and chart behavior through dynamic visualizations and KPIs.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Requirement](#-business-requirement)
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Dashboard Pages](#-dashboard-pages)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Tools & Technologies](#-tools--technologies)
- [Project Structure](#-project-structure)
- [How to Use](#-how-to-use)
- [Author](#-author)

---

## 🎯 Project Overview

Spotify's global Top 50 World chart generates hundreds of daily chart entries — but raw rankings alone tell you very little. This project transforms **27,800+ rows** of daily chart data into a structured, interactive Power BI dashboard that allows music analysts, playlist managers, and marketing teams to:

- Monitor song and artist performance at a glance
- Identify which release strategies drive chart dominance
- Track seasonal trends in chart activity and popularity
- Drill down from overview KPIs to individual song and artist records

The dashboard is built on Spotify's dark visual identity — black backgrounds, Spotify green (`#1DB954`) accents, and card-based layouts — making it feel native to the platform it analyzes.

---

## 📋 Business Requirement

Spotify stakeholders — music analysts, playlist managers, and marketing teams — need a **consolidated dashboard** to monitor song and artist performance across multiple dimensions.

### Overview Page
- Track KPIs: **Total Songs, Distinct Artists, Average Popularity, Avg Duration**
- Compare **Explicit vs Non-Explicit Songs** and their share of the chart
- Analyze **Songs by Album Type** (single, album, compilation)
- View **Distinct Songs and Avg Popularity by Year**
- Trend analysis of **Avg Popularity & Distinct Songs by Month**
- Highlight **Top Songs & Top Artists by Popularity**

### Artist Page
- Show **Top Artists by Total Popularity**
- Compare **Tracks per Album** and **Songs by Artist**
- Drill down to artist-level data: songs, release date, avg popularity, avg position, duration
- Identify artists with **consistent hits and #1 positions**

### Songs Page
- Rank **Top Songs by Popularity**
- Show **Tracks per Song** (album/single distribution)
- Compare **Songs by Song Count**
- Detailed table: song name, release date, distinct artists, avg popularity, position, duration per year

---

## ❓ Problem Statement

Spotify's raw "Top 50" dataset is limited to lists and rankings, making it difficult for stakeholders to **see patterns and act on insights quickly**.

| Problem | Solution Delivered |
|---|---|
| No clear KPI monitoring | Dashboard surfaces total songs, artists, avg popularity, and duration at a glance |
| Lack of explicit vs non-explicit analysis | Side-by-side comparison of explicit (11K) vs non-explicit (17K) chart entries |
| Difficulty tracking song/album distribution | Visuals break down chart share by album type and release year |
| Trend visibility missing | Monthly and yearly popularity and song-count trend lines |
| Artist vs song-level insights not connected | Drill-down pages link overview KPIs to individual artist and song records |
| Decision-making gaps | Marketing and curation teams can identify which artists to promote and when to release |

---

## 📁 Dataset

| Field | Details |
|---|---|
| **Source** | Spotify Top 50 World — daily global chart |
| **Period** | May 2023 – November 2024 |
| **Total Rows** | 27,800+ daily chart entries |
| **File** | `spotify-top-50-world.csv` |

### Columns

| Column | Type | Description |
|---|---|---|
| `date` | Date | Daily chart date |
| `position` | Integer | Chart rank (1–50) |
| `song` | Text | Track name |
| `artist` | Text | Artist name(s) |
| `popularity` | Integer | Spotify popularity score (0–100) |
| `duration_ms` | Integer | Track duration in milliseconds |
| `album_type` | Text | `album` / `single` / `compilation` |
| `total_tracks` | Integer | Number of tracks in the release |
| `release_date` | Date | Original release date |
| `is_explicit` | Boolean | `True` / `False` |
| `album_cover_url` | Text | Spotify album art URL |

---

## 📊 Dashboard Pages

### 🏠 Home
Entry screen with project branding, navigation buttons, and a brief description of the dashboard purpose.

### 🔍 Overview
High-level KPI cards and trend charts:
- **789** Distinct Songs · **342** Unique Artists · **3.28 min** Avg Duration · **90** Avg Popularity
- Songs by Album Type (donut) · Explicit vs Non-Explicit (donut)
- Songs by Year · Average Popularity by Album Type
- Avg Popularity by Month (line) · Distinct Songs by Month (bar)
- Top Songs by Popularity (bar) · Top Artists by Song Count (bar)

### 🎤 Artists
Artist-level performance analysis:
- Songs by Artist (distinct count)
- Total Popularity by Artist (sum of all chart appearances)
- Position #1 Hits per Artist
- Drill-through table: song name, release date, album type, avg popularity, avg duration

### 🎵 Songs
Song-level breakdown:
- Songs by Distinct Artist Count (collaboration depth)
- Total Popularity by Song
- Position #1 Hits by Song
- Detail table: song, release date, album type, avg popularity, avg duration

---

## 💡 Key Insights

1. **Taylor Swift dominates the catalog** — 85 distinct charting songs, 2.8× the next artist (Travis Scott at 30). Her total popularity score of **163,538** across 1,871 chart entries is unmatched.

2. **Chart longevity is rare but powerful** — 'I Wanna Be Yours' (Arctic Monkeys) stayed on the Top 50 for **548 days**. 'Cruel Summer' followed at 517 days. Proven catalog tracks outlast most new releases.

3. **October is the peak month** — **221 distinct songs** charted in October, driven by Q4 album campaigns. January and February are the quietest (88–91 songs) — the biggest release window opportunity.

4. **Singles outperform albums in popularity** — Singles average a popularity score of **91.86** vs **88.30** for album tracks, supporting a singles-first streaming strategy.

5. **Reaching #1 is extremely rare** — Only **37 out of 794 songs** (4.7%) ever hit Position #1. 'Die With A Smile' (Lady Gaga & Bruno Mars) held the top spot for **77 days** — the longest #1 streak.

6. **Older catalog earns higher scores** — Songs released in **2019 average 94.9 popularity** vs 88.0 for 2024 releases. Only the strongest catalog tracks survive to today's chart, giving them a structural scoring advantage.

---

## ✅ Recommendations

| # | Strategy | Insight Behind It |
|---|---|---|
| **R1** | **Target Aug–Oct for major releases** | Chart activity peaks at 212–221 distinct songs/month in this window |
| **R2** | **Lead with a single before the album** | Singles score 3.5 pts higher on average (91.86 vs 88.30) |
| **R3** | **Re-promote catalog tracks actively** | 'I Wanna Be Yours' (2013) charted 548 days; 2019 releases average 94.9 popularity |
| **R4** | **Invest in high-profile collaborations** | 'Die With A Smile' held #1 for 77 days; 'One Of The Girls' charted for 378 days |
| **R5** | **Build multi-language global strategies** | Latin (Eslabon Armado: 40 days at #1) and K-Pop (Jung Kook & Latto: 69 days at #1) consistently break into the global Top 50 |
| **R6** | **Monitor Popularity Score < 85 as an early-warning KPI** | Avg chart score is 89.6; tracks below 85 are at risk of dropping off — flag early in Power BI |

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard design, visuals, slicers, drill-through |
| **DAX** | KPI measures — distinct counts, avg popularity, position hit flags |
| **Microsoft Excel / CSV** | Data source (`spotify-top-50-world.csv`) |
| **Power Query** | Data cleaning and type transformation |
| **Python (pandas)** | Exploratory data analysis during development |

---

## 📂 Project Structure

```
spotify-top-50-powerbi/
│
├── spotify-top-50-world.csv       # Raw dataset (27,800+ rows)
├── spotify.pbix                   # Power BI report file
├── Spotify_Dashboard.pptx         # Presentation deck
├── Business_Requirements.docx     # Business requirements document
└── README.md                      # This file
```

---

## ▶ How to Use

1. **Clone this repository**
```bash
   git clone https://github.com/your-username/spotify-top-50-powerbi.git
```

2. **Open the dashboard**
   - Open `spotify.pbix` in **Power BI Desktop** (free download from Microsoft)

3. **Refresh the data** *(if needed)*
   - Go to **Home → Transform Data → Close & Apply**
   - Ensure `spotify-top-50-world.csv` is in the same folder as the `.pbix` file

4. **Explore the dashboard**
   - Navigate using the **Home / Overview / Artists / Songs** buttons
   - Use slicers to filter by year, month, album type, or explicit flag
   - Click any bar or donut segment to cross-filter all visuals on the page

---

## 👤 Author

**Supratim Maity**
B.Sc. (Hons) Statistics — University of Calcutta (Asutosh College)
Entry-Level Data Analyst · SQL · Python · Power BI · Tableau · Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github)](https://github.com/your-username)

---

*Built as a Data Analyst portfolio project. Data sourced from Spotify's public Top 50 World chart.*
