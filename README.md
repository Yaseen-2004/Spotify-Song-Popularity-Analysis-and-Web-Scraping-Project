# Spotify Song Popularity Analysis and Web Scraping Project

An end-to-end Python data science project combining **Spotify song popularity analysis, machine learning, unsupervised learning, web scraping, exploratory data analysis, visualization, and automated artifact generation**.

---

## Project Overview

This project is divided into two major components:

### 1. Spotify Song Popularity Analysis

The Spotify analysis investigates the relationship between song characteristics, platform metrics, and song popularity.

It includes:

- Data loading and inspection
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Popularity distribution analysis
- Top 10 most popular songs
- Genre-wise analysis
- Correlation analysis
- Audio-feature regression models
- Full-feature Random Forest model
- Model performance comparison
- Feature importance analysis
- K-Means clustering
- Elbow Method
- Silhouette Score
- PCA visualization
- Cluster profiling
- Model persistence
- CSV export

### 2. Web Scraping and Data Analysis

The second component demonstrates practical web scraping using Python.

It includes:

- HTTP requests
- HTML parsing
- BeautifulSoup
- Pagination handling
- Book data extraction
- Data cleaning
- Data transformation
- Exploratory Data Analysis
- Price analysis
- Rating analysis
- Availability analysis
- Quotes scraping
- Generic webpage scraping
- Dashboard generation
- Workflow diagrams

---

# Project Architecture

```text
                         ┌──────────────────────────┐
                         │        PROJECT START      │
                         └────────────┬─────────────┘
                                      │
                     ┌────────────────┴────────────────┐
                     │                                 │
                     ▼                                 ▼
          ┌──────────────────────┐          ┌──────────────────────┐
          │   SPOTIFY DATASET    │          │    WEB SOURCES       │
          │   Spotify CSV        │          │ books.toscrape.com   │
          └──────────┬───────────┘          │ quotes.toscrape.com  │
                     │                      │ example.com           │
                     │                      └──────────┬───────────┘
                     ▼                                 │
          ┌──────────────────────┐                     ▼
          │ Data Inspection      │          ┌──────────────────────┐
          │ Missing Values       │          │ HTTP Requests        │
          │ Duplicates           │          │ Pagination           │
          │ Data Types           │          └──────────┬───────────┘
          └──────────┬───────────┘                     │
                     │                                 ▼
                     ▼                      ┌──────────────────────┐
          ┌──────────────────────┐          │ BeautifulSoup        │
          │ Data Cleaning        │          │ HTML Parsing          │
          │ Type Conversion      │          │ Data Extraction       │
          │ Missing Value        │          └──────────┬───────────┘
          │ Handling             │                     │
          └──────────┬───────────┘                     ▼
                     │                      ┌──────────────────────┐
                     ▼                      │ Scraped DataFrame     │
          ┌──────────────────────┐          └──────────┬───────────┘
          │ Exploratory Data     │                     │
          │ Analysis             │                     ▼
          │ Visualization        │          ┌──────────────────────┐
          │ Correlation          │          │ Data Cleaning        │
          └──────────┬───────────┘          │ Transformation       │
                     │                      └──────────┬───────────┘
          ┌──────────┴──────────┐                     │
          │                     │                     ▼
          ▼                     ▼          ┌──────────────────────┐
 ┌──────────────────┐  ┌──────────────────┐│ EDA & Visualization │
 │ Regression       │  │ K-Means          ││ Price / Rating      │
 │ Machine Learning │  │ Clustering       ││ Availability         │
 └────────┬─────────┘  └────────┬─────────┘└──────────┬───────────┘
          │                     │                     │
          ▼                     ▼                     ▼
 ┌──────────────────┐  ┌──────────────────┐ ┌──────────────────────┐
 │ Model Evaluation │  │ PCA Visualization│ │ EDA Dashboard        │
 │ MAE / RMSE / R²  │  │ Cluster Profiles │ │ Workflow Diagrams    │
 └────────┬─────────┘  └────────┬─────────┘ └──────────┬───────────┘
          │                     │                     │
          └─────────────────────┴──────────────┬──────┘
                                               ▼
                                  ┌────────────────────────┐
                                  │  PROJECT ARTIFACTS     │
                                  │ CSV / PKL / PNG / HTML │
                                  └────────────────────────┘
