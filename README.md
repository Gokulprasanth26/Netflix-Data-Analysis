# Netflix Data Analysis

A beginner exploratory data analysis project exploring **8,807 Netflix movies and
TV shows** with Python, Pandas, NumPy, Matplotlib, and Seaborn.

**[Start here: main submission](notebooks/Netflix_Submission.ipynb)** ·
[Secondary enhanced notebook](notebooks/Netflix_EDA.ipynb) ·
[Dataset](data/netflix.csv)

## Choose a notebook

| Notebook | Role | What to expect |
|---|---|---|
| **[Netflix_Submission.ipynb](notebooks/Netflix_Submission.ipynb)** | **Main project** | The original project submission, covering data exploration, cleaning, visualizations, observations, and recommendations. Start here when reviewing the project. |
| [Netflix_EDA.ipynb](notebooks/Netflix_EDA.ipynb) | Secondary reference | An enhanced version developed with AI assistance, including additional validation, reusable plotting helpers, and exported figures. Retained for comparison and further learning. |

The main notebook is the supplied **Netflix submission project.ipynb**, renamed
only for a consistent repository filename. Both notebooks retain their existing
code, written explanations, and saved outputs.

## What the main project explores

- The balance of movies and TV shows in the dataset.
- Missing values and preparation of country, cast, director, genre, and date fields.
- Content patterns across countries, genres, ratings, and years.
- Movie runtimes, TV season counts, and potential outliers.
- Observations and proposed business recommendations from the exploration.

**Tools used:** Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Reading the results

This is a historical catalog snapshot, with recorded addition dates through
**September 25, 2021**. It describes the supplied dataset rather than Netflix's
current catalog.

The submission's recommendations should be read as ideas for further investigation.
The dataset has no viewership, revenue, subscriber, or licensing-cost measures, so
catalog counts alone cannot establish popularity, retention, or profitability.
The 2021 period is incomplete; a single recorded TV season does not establish that
a show was cancelled. Country and genre counts may overlap because one title can
have multiple labels.

## Repository structure

```text
Netflix-Data-Analysis/
├── README.md
├── AGENTS.md
├── requirements.txt
├── .gitignore
├── netflix.csv                     # Original URL used by the main submission
├── data/
│   └── netflix.csv                 # Local data used by the secondary notebook
├── notebooks/
│   ├── Netflix_Submission.ipynb     # MAIN: original project submission
│   └── Netflix_EDA.ipynb            # SECONDARY: AI-assisted enhanced analysis
└── images/                         # Six figures from the secondary notebook
```

The two CSV files are identical. The root copy preserves the data URL already
used by the main submission; the `data/` copy preserves the secondary notebook's
local file path. This lets both notebooks keep their existing code.

## Open and run locally

Both notebooks can be viewed on GitHub with their saved outputs. To work locally:

```bash
git clone https://github.com/Gokulprasanth26/Netflix-Data-Analysis.git
cd Netflix-Data-Analysis
python -m venv .venv
```

Activate the environment:

```powershell
# Windows PowerShell
.venv\Scripts\Activate.ps1
```

```bash
# macOS / Linux
source .venv/bin/activate
```

Install the project dependencies and open JupyterLab:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

- **Main submission:** open `notebooks/Netflix_Submission.ipynb`. It loads the
  CSV from this repository's public GitHub URL, so running it requires internet
  access.
- **Secondary reference:** open `notebooks/Netflix_EDA.ipynb`. It reads
  `data/netflix.csv` locally and regenerates the six figures in `images/` when run.

Run cells in order using **Restart Kernel and Run All Cells**. The pinned
`requirements.txt` describes the Python 3.12 environment used for the enhanced
notebook. The main submission's saved metadata records Python 3.10.11; its
original package versions were not recorded, so these pins do not reproduce that
original environment exactly.

## Secondary notebook: findings and figures

The exported figures below belong to the **AI-assisted enhanced notebook**.
They are supporting reference material; the main submission's own charts remain
inside its notebook.

<details>
<summary>View enhanced findings and six supporting charts</summary>

| Question | Result reported in the enhanced analysis |
|---|---|
| Content mix | 6,131 movies (69.6%) and 2,676 TV shows (30.4%). |
| Most recorded additions | 2019: 2,016 titles. Ten undated titles are excluded; 2021 is incomplete. |
| Most associated titles by country | United States: 3,690; India: 1,046. Co-productions count in multiple countries. |
| Largest listed category | International Movies: 2,752 titles; Dramas: 2,427. Category counts overlap. |
| Most common content rating | TV-MA: 3,207 titles. Content ratings are not viewer scores. |
| Duration | Median movie runtime: 98 minutes. 1,793 TV shows (67.0%) have one recorded season. |

The enhanced workflow adds checks for title keys, relationship-table joins,
missing metadata, percentage denominators, date coverage, and separate duration
units for movies and TV shows. It also handles three runtime values stored in
the rating field while preserving the source CSV.

![Content mix: 6,131 movies and 2,676 TV shows](images/content_type_distribution.png)

![Recorded additions by year, with 2021 marked as incomplete](images/recorded_additions_by_year.png)

![Top ten countries by associated titles; countries can overlap](images/top_10_countries.png)

![Top ten listed categories; categories can overlap](images/top_10_genres.png)

![Titles by content rating](images/content_ratings.png)

![Movie runtime distribution with a 98-minute median](images/movie_duration_distribution.png)

</details>

## Data provenance

The CSV is preserved byte-for-byte from this repository's original dataset at
commit [`5e4a68f`](https://github.com/Gokulprasanth26/Netflix-Data-Analysis/tree/5e4a68f).
The upstream publisher, collection method, and redistribution license were not
documented in the original repository; no upstream attribution or license is
assumed.

**Author:** [Gokul Prasanth](https://github.com/Gokulprasanth26)
