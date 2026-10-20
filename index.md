# Shi Hao He

Data science student at the **University of Macau** (CISC7204 Data Science and Data
Visualization, CISC7026 Introduction to Deep Learning). I like turning small, messy datasets
into something you can look at and argue with - and I try to be explicit about what the data
does *not* support.

## About me

I am currently finishing my coursework in data science, working mostly in Python: cleaning
tables with pandas, checking them before trusting them, and then choosing a visualisation that
answers one question well instead of five badly.

The project below is a good example: 268 incident reports, a spatial question, and a data
dictionary that turned out to be wrong.

## Technical skills

- **Python** - pandas, NumPy, scikit-learn, matplotlib, seaborn
- **Deep learning** - PyTorch (feed-forward networks, training and evaluation loops)
- **Geospatial visualisation** - geoplotlib, coordinate data, k-means clustering
- **Tools** - Jupyter Notebook, Git / GitHub, Markdown

## Project showcase

### Reported poaching incidents in Tanzania (2005-2015)

**Research question:** where are the 268 reported poaching incidents concentrated, and how
much can the dates in the dataset actually tell us?

![Incident clusters in Tanzania](images/incident_clusters.png)

**What I found**

- The largest of three spatial clusters holds **113 of 268 reports (42.2%)**, centred near
  **34.49 E, 7.72 S**; a cluster-free hexbin view picks out the same hotspot (busiest cell: 6
  reports).
- **The data dictionary does not hold:** in **62.3%** of rows the "report created" date is
  *earlier* than the incident date, and one incident date is reused 9 times. So I dropped the
  seasonality idea and reported the date problem instead.
- **Limitation:** there is no denominator (patrol effort, protected-area size), so these are
  268 *reports* - the clusters show where incidents were reported, not where poaching is worst.

**Status:** completed

**Code and data:** [data-science-project](https://github.com/3gg3g3g3g/data-science-project)

## What I want to improve next

Add a proper basemap and protected-area boundaries so the clusters can be checked against the
parks they fall inside, and replace k-means with a density-based method that does not require
choosing the number of groups in advance.

---

*Built with GitHub Pages. The project repository contains the notebook, the data, the
requirements file and the figures.*
