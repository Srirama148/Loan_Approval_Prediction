# 📊 Instagram Data Analysis — Alfido Tech

## 📌 Project Overview

This project analyzes Instagram data for **Alfido Tech** to understand post performance, audience engagement, content types, hashtags, and follower-growth signals.

The main goal is to use historical Instagram data to identify useful engagement patterns and create a practical content strategy for improving Instagram performance.

---

## 🎯 Objectives

The project focuses on the following objectives:

* Analyze Instagram post performance
* Calculate likes and comments per post
* Calculate engagement rate
* Compare different content types
* Analyze hashtag performance
* Analyze follower vs non-follower engagement
* Investigate posting-day and posting-time patterns
* Identify follower-growth signals
* Create an optimized content calendar
* Recommend 5 strategies to increase engagement

---

## 📂 Dataset

The Instagram export contains the following CSV files:

```text
data/
│
├── comments.csv
├── follows.csv
├── likes.csv
├── photo_tags.csv
├── photos.csv
├── tags.csv
└── users.csv
```

### Dataset description

| File             | Description                             |
| ---------------- | --------------------------------------- |
| `photos.csv`     | Instagram post information              |
| `likes.csv`      | Like activity                           |
| `comments.csv`   | Comment activity                        |
| `follows.csv`    | Follower/following relationships        |
| `photo_tags.csv` | Relationship between posts and hashtags |
| `tags.csv`       | Hashtag information                     |
| `users.csv`      | User information                        |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data cleaning and analysis
* **NumPy** — Numerical calculations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook** — Analysis and documentation

---

## 📁 Project Structure

```text
Alfido_Instagram_Analysis/
│
├── data/
│   ├── comments.csv
│   ├── follows.csv
│   ├── likes.csv
│   ├── photo_tags.csv
│   ├── photos.csv
│   ├── tags.csv
│   └── users.csv
│
├── output/
│   ├── charts/
│   └── reports/
│
├── Alfido_Instagram_Analysis.ipynb
│
├── README.md
│
└── requirements.txt
```

---

# 🔄 Project Workflow

The project follows this data-analysis pipeline:

```text
Instagram Export
       ↓
Load CSV Files
       ↓
Data Cleaning
       ↓
Date/Time Processing
       ↓
Combine Datasets
       ↓
Calculate Engagement Metrics
       ↓
Content Analysis
       ↓
Hashtag Analysis
       ↓
Follower Analysis
       ↓
Data Visualization
       ↓
Business Recommendations
       ↓
Content Calendar
```

---

# 📊 Key Metrics

## 1. Engagement

Engagement is calculated as:

```text
Engagement = Likes + Comments
```

For example:

```text
Likes = 100
Comments = 20

Engagement = 100 + 20
           = 120
```

---

## 2. Engagement Rate

The project calculates engagement rate using:

```text
Engagement Rate =
(Likes + Comments) / Followers
```

In Python:

```python
post_data["engagement_rate"] = (
    post_data["engagement"] /
    post_data["followers"]
)
```

This allows posts to be compared relative to the size of the follower base.

---

# 🔍 Analysis Performed

## 1. Post Analysis

The project calculates:

* Number of posts
* Likes per post
* Comments per post
* Total engagement
* Engagement rate
* Top-performing posts

---

## 2. Content Type Analysis

Posts are grouped according to their content type.

Examples include:

* Photo
* Video
* Carousel

The average performance of each content type is compared using:

```text
Average Likes
Average Comments
Average Engagement
Average Engagement Rate
```

This helps identify which types of content deserve more testing.

---

## 3. Hashtag Analysis

Hashtags are connected to their corresponding posts using:

```text
photo_tags.csv
        +
tags.csv
        +
photos.csv
```

The project calculates:

* Number of posts using each hashtag
* Average likes
* Average comments
* Average engagement rate

A minimum-post threshold is used when interpreting hashtag performance so that hashtags used only once or twice do not produce misleading conclusions.

---

## 4. Follower vs Non-Follower Analysis

The likes dataset contains information about whether the person giving the like was already following the account.

This is used to calculate:

```text
Follower Likes
Non-Follower Likes
```

The non-follower percentage provides a useful **content-discovery signal**.

It should not be interpreted as direct follower acquisition because the supplied data does not connect individual likes to subsequent follows.

---

# ⏰ Posting-Time Analysis

The project checks:

* Posting date
* Day of week
* Posting hour

Normally, this can be used to determine which days and hours generate the highest engagement.

### Dataset limitation

The supplied Instagram export contains the same timestamp for all 257 posts.

Therefore, the dataset does **not** provide enough variation to reliably determine the best posting day or hour.

Instead of creating a misleading result, the project proposes a controlled posting experiment.

---

# 📅 Recommended Test Content Calendar

The following schedule can be tested for four weeks:

| Day       | Time (IST) | Content                          |
| --------- | ---------: | -------------------------------- |
| Monday    |   12:30 PM | Educational carousel             |
| Tuesday   |    7:30 PM | Short technology video           |
| Wednesday |   12:30 PM | Case study / result              |
| Thursday  |    7:30 PM | Team / behind-the-scenes         |
| Friday    |   12:30 PM | Industry insight                 |
| Saturday  |   10:30 AM | Poll / Q&A                       |
| Sunday    |          — | Stories and community engagement |

These times are **test slots**, not claims that the supplied dataset proves they are optimal.

After four weeks, compare:

* Engagement rate
* Comments
* Saves
* Shares
* Profile visits
* Non-follower reach
* New followers

The results can then be used to refine the schedule.

---

# 🚀 Five Engagement Strategies

## 1. Create Saveable Educational Content

Create useful technical content such as:

* Python tips
* AI tools
* Coding tutorials
* Checklists
* Step-by-step guides
* Common programming mistakes

Educational carousels can be designed specifically to encourage saves and shares.

---

## 2. Increase Short-Form Video

Create short videos around:

* Technology tips
* Coding tricks
* AI tools
* Software demonstrations
* Before/after workflows
* Quick tutorials

The first few seconds should clearly communicate the value of the video.

---

## 3. Encourage Conversations

Instead of generic calls to action, ask specific questions.

Example:

```text
Which Python library do you use more?

A. Pandas
B. NumPy
C. Both
```

Specific questions make it easier for followers to participate.

---

## 4. Create Recurring Content Series

Create predictable weekly content such as:

```text
Tech Tip Tuesday
Tool of the Week
AI Friday
Coding Challenge
Build Breakdown
```

Recurring formats make content production easier and give followers a reason to return.

---

## 5. Use Continuous Experimentation

Test different:

```text
Content formats
        ↓
Topics
        ↓
Posting times
        ↓
Hashtag combinations
        ↓
Calls to action
```

Track the results and gradually improve the content strategy.

---

# 📈 Visualizations

The notebook contains visualizations for:

1. Posts by content type
2. Average likes by content type
3. Average comments by content type
4. Engagement rate by content type
5. Hashtag performance
6. Follower vs non-follower likes
7. Top-performing posts
8. Posting schedule/testing plan

Each visualization is intended to answer a specific business question rather than simply display data.

---

# 📌 Key Findings

Based on the supplied export:

* **257 posts** were analyzed.
* The dataset contains **8,782 likes**.
* The dataset contains **7,488 comments**.
* There are **16,270 recorded likes + comments**.
* Approximately **33.4% of recorded likes came from non-followers**.
* Content-type engagement rates are relatively close, so format selection should be validated through controlled testing.
* Hashtag performance should be interpreted using a minimum-post threshold.
* Historical best posting time cannot be reliably calculated because the supplied posts share the same timestamp.
* Historical follower-growth trends cannot be calculated because the follow records also share the same timestamp.

---

# ⚠️ Data Limitations

There are several limitations in the supplied dataset.

### 1. Identical timestamps

All posts have the same timestamp, so historical posting-time analysis is not reliable.

### 2. No historical follower-count series

The dataset provides follow relationships but does not provide daily/weekly follower counts.

Therefore, we cannot reliably calculate:

```text
Followers over time
Net follower growth by day
Follower growth caused by individual posts
```

### 3. Limited engagement metrics

The available data focuses mainly on likes and comments.

For a more complete Instagram strategy, future exports should include:

* Reach
* Impressions
* Saves
* Shares
* Profile visits
* Website clicks
* Reel views
* New followers
* Unfollows
* Follower demographics

---

# 🔮 Future Improvements

The project can be extended by adding Instagram Insights data.

With richer data, we could build:

```text
Follower Growth Dashboard
        +
Reach Analysis
        +
Best Posting Time Analysis
        +
Content Recommendation System
        +
Hashtag Recommendation System
        +
Monthly Performance Dashboard
```

A future version could also use machine learning to predict expected engagement based on:

* Content type
* Posting time
* Hashtags
* Caption characteristics
* Historical engagement
* Audience size

---

# ▶️ How to Run the Project

## Step 1 — Install Python

Download and install Python 3.x.

## Step 2 — Install required libraries

Run:

```bash
pip install pandas numpy matplotlib seaborn jupyter openpyxl
```

## Step 3 — Open Jupyter Notebook

Run:

```bash
jupyter notebook
```

## Step 4 — Open the notebook

Open:

```text
Alfido_Instagram_Analysis.ipynb
```

## Step 5 — Add the dataset

Make sure the CSV files are inside:

```text
data/
```

## Step 6 — Run the notebook

Run each cell from top to bottom.

---

# 💡 Interview Explanation

If asked to explain the project, you can say:

> "This project analyzes Instagram data for Alfido Tech to understand what factors are associated with higher engagement. I loaded the Instagram CSV data using Pandas, cleaned and parsed the dates, combined likes, comments, followers and hashtag information, and calculated post-level engagement and engagement rate. I then compared content types and hashtags and analyzed follower versus non-follower engagement. I also checked whether posting time could be analyzed. Because the supplied dataset contains identical timestamps for all posts, I avoided making an unsupported claim about the best posting time and instead designed a four-week controlled testing schedule. Finally, I converted the analysis into five practical engagement strategies and a content calendar."

---

# 👨‍💻 Skills Demonstrated

This project demonstrates:

* Python
* Pandas
* NumPy
* Data Cleaning
* Data Transformation
* Exploratory Data Analysis
* Data Aggregation
* Data Visualization
* Business Analytics
* Social Media Analytics
* KPI Analysis
* Data-driven Recommendations

---

# 📄 Project Deliverables

The project produces:

```text
1. Instagram Analysis Notebook
2. Post-level Engagement Dataset
3. One-page Strategy Document
4. Recommended Content Calendar
5. Five Engagement Strategies
```

---

# 👤 Author

**Alfido Tech Instagram Data Analysis Project**

Built using Python and Data Analytics.
