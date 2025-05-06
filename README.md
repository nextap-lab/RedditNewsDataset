# Reddit News Headlines Dataset (2008–2016)

A high-quality collection of **73,608** English-language news headlines submitted to a prominent global news aggregation community between **June 2008** and **July 2016**. Each entry captures the top-ranked news headlines of the day based on dynamic community engagement, offering a natural, crowdsourced record of what dominated global attention during that time.

---

## 📦 Dataset Overview

| File             | Records | Columns | Size    |
| ---------------- | ------- | ------- | ------- |
| `RedditNews.csv` | 73,608  | 2       | \~12 MB |

### Columns

| Column | Description                                                |
| ------ | ---------------------------------------------------------- |
| `Date` | Date of the snapshot (UTC, format: YYYY-MM-DD)             |
| `News` | Raw headline text ranked highest that day by the community |

---

## 📊 Data Summary

* **Time range:** 08 June 2008 – 01 July 2016
* **Total unique days:** 2,943
* **Average headlines/day:** 25.0
* **Unique headlines:** 73,537
* **Average headline length:** 109 characters

This dataset provides a clean and continuous view of public news salience and can be used to study media trends, sentiment shifts, or event impact over nearly a decade.

---

## 🧠 Use Cases

* News-based trend detection and timeline reconstruction
* Sentiment, stance, and topic classification
* Linguistic evolution in media headlines
* Financial or geopolitical correlation modeling
* Training summarization and rewriting models

---

## 🛠 Quick Start (Python)

```python
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("RedditNews.csv", parse_dates=["Date"])
print(df.sample(5))

# Visualize headline count over time
df.groupby("Date").size().plot(figsize=(12, 4), title="Daily Headline Volume")
plt.xlabel("Date")
plt.ylabel("Count")
plt.tight_layout()
plt.show()
```

---

## 📁 Directory Structure

```
📦 Dataset Root
├── RedditNews.csv         # Headlines data (73k+ rows)
├── README.md              # Documentation (this file)
└── LICENSE                # Usage and fair-use information
```

---

## ⚠️ License & Usage

This dataset contains content originally produced by third-party news outlets. It is redistributed **for non-commercial academic and research purposes only** under a fair-use understanding. Do not use for commercial applications. All rights remain with the original content creators.

---

## 📚 Citation

If you use this dataset in your work or publication, please cite it as follows:

```
@dataset{redditnews_2008_2016,
  title  = {Reddit News Headlines Dataset (2008–2016)},
  author = {Your Name},
  year   = {2025},
  url    = {https://github.com/nextap-lab/nextap.github.io}
}
```

---

## 🤝 Contributions

We welcome contributions and derivative analysis! If you build something interesting using this data, feel free to open a PR or link back to us.

> Maintained by [@nextap-lab](https://github.com/nextap-lab) · Updated: May 2025
