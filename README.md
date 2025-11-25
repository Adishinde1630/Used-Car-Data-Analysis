# Used Car Insights 🚗📊

> Hands-on EDA and scraping for used car listings (Cars24 dataset).

This small project contains Jupyter notebooks used to scrape used car listings and perform exploratory data analysis (EDA) and visualizations to surface insights about pricing, trends, and attributes.

**Repository structure**

- `Cars24-Scrapping.ipynb`: Notebook that demonstrates how the Cars24 listings were scraped (data collection). Includes scraping code, examples, and notes on legal/ethical considerations.
- `Cars24-EDA.ipynb`: EDA and visualization notebook. Data cleaning, feature engineering, exploratory charts, summary statistics, and actionable insights.

**Highlights**

- Clean, repeatable notebooks for scraping and analysis.
- Clear visualizations showcasing price distributions, mileage vs price, brand-wise trends, and outlier detection.
- Minimal, reproducible environment: run the notebooks locally or in a cloud notebook environment.

## Quickstart

1. Clone the repo (if you haven't already):

```powershell
git clone <your-repo-url>
cd Used_Car_Insights
```

2. Create a Python environment (recommended) and install dependencies.

Using venv + pip:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -U pip
pip install jupyter pandas numpy matplotlib seaborn plotly requests beautifulsoup4 lxml tqdm
```

Or create a `requirements.txt` and run `pip install -r requirements.txt` if you prefer.

3. Launch Jupyter Notebook or JupyterLab and open the notebooks:

```powershell
jupyter notebook
```

Open `Cars24-Scrapping.ipynb` first if you want to reproduce the dataset; otherwise, open `Cars24-EDA.ipynb` to explore the analysis using an existing CSV.

## Data

- The scraping notebook (`Cars24-Scrapping.ipynb`) documents how raw listing data was collected. If you run it, it will produce a CSV/JSON dataset in the notebook's working directory (see notebook cells for exact filename and output path).
- If the dataset is already present (CSV), `Cars24-EDA.ipynb` expects a typical cleaned table with columns such as `price`, `km_driven`, `fuel_type`, `brand`, `model`, `year`, etc.

Notes on scraping: always respect the target website's Terms of Service and robots.txt. This project is for educational purposes—do not use scraping scripts against services where it is disallowed.

## Notebooks & What to Run

- `Cars24-Scrapping.ipynb` — Run the cells sequentially. It contains parameter cells to control page ranges, delay between requests, and output filename. Test with a small range first.
- `Cars24-EDA.ipynb` — Run top-to-bottom to reproduce the analysis. Adjust the data path if your CSV lives in a different folder.

## Reproducibility Tips

- Use a dedicated virtual environment and pin package versions if you need exact reproducibility.
- If you want to run the notebooks in the cloud, try Binder or Google Colab. For large scraping runs, prefer running in a controlled VM and throttle requests to avoid rate limits.

## Suggested Next Steps

- Add a `requirements.txt` or `environment.yml` to pin dependencies.
- Convert key analysis cells into scripts or a small package for automation.
- Add unit tests for data-cleaning functions (if extracting utility functions from notebooks).

## Contribution

Contributions are welcome. If you plan to modify the notebooks or add derived data, please:

1. Create an issue describing your change.
2. Open a PR with a short summary and small, focused commits.

## License & Ethics

This repository is provided for educational purposes. Verify that any web scraping you perform is compliant with legal and site-specific rules. No license file is included — add one if you intend to publish or share this project more widely.

---

If you'd like, I can also:

- generate a `requirements.txt` from the notebooks,
- add a short `environment.yml` for conda users,
- or create a small helper script to export cleaned CSVs from the scraping notebook.

Tell me which of these you'd like next.
