# Movie Recommender System

A Movie Recommendation System built on collaborative filtering and matrix factorization. The core analysis is delivered via `Movie_Recommender_Systems.ipynb`, which loads raw data, performs cleaning & feature engineering, trains models, and generates personalized movie recommendations.

## 1. Overview
This repo walks through a complete movie recommendation pipeline using user ratings data:
- Load raw `.dat` files from `data/`
- Clean & standardize movie/user/rating records
- Explore data and derive features
- Train collaborative filtering / matrix factorization models
- Evaluate model performance and generate recommendations

## 2. Contents
- `Movie_Recommender_Systems.ipynb` — main analysis notebook
- `DATA_DICTIONARY.md` — dataset schema and field definitions
- `data/` — expected location for raw `.dat` dataset files
- `clean_data/` — (optional) cleaned exports or intermediate results

## 3. Key Highlights
- Robust data cleaning for malformed `zee-*.dat` records
- Genre normalization and correction mapping
- EDA including rating distributions and user/item profiles
- Matrix factorization using `cmfrec`
- Evaluation with RMSE/MAPE and recommendation ranking

## 4. Quickstart
### 4.1 Create and activate a Python virtual environment (Windows example)
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 4.2 Install core dependencies (recommended)
```powershell
pip install -r requirements.txt
```
> If `requirements.txt` is not provided, install at least:
> - pandas
> - numpy
> - matplotlib
> - seaborn
> - plotly
> - scikit-learn
> - cmfrec

### 4.3 Launch the notebook and run cells
1. Open `Movie_Recommender_Systems.ipynb` in Jupyter or VS Code.
2. Ensure `data/` contains:
   - `zee-movies.dat`
   - `zee-ratings.dat`
   - `zee-users.dat`
3. Run cells sequentially from top to bottom.

## 5. Usage and Reproducibility
### 5.1 Run the Analysis Notebook
- The notebook is designed to be executed in order.
- If you restart the notebook kernel, rerun all cells from the beginning.
- Confirm the `data/` folder is present and contains the required `.dat` files.

## 6. Results (summary)
The notebook produces:
- Cleaned and standardized user/movie/rating tables
- Performance metrics (RMSE, MAPE) for recommendation models
- Top-N movie recommendations for sample users

## 7. Recommendations
- Keep the `data/` folder and `.dat` filenames unchanged to avoid path modifications.
- If datasets are updated, rerun the notebook end-to-end to refresh results.
- Use the model evaluation section as a template for comparing new algorithms.

## 8. Notes & Caveats
- Raw `.dat` files include inconsistent formatting; the notebook includes custom parsing/cleanup logic.
- The notebook currently assumes Windows-style working directories; adjust any hardcoded paths when running elsewhere.
- Processing may take longer on large datasets; monitor memory usage when running model training.
