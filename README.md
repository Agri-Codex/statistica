# Statistica - Statistical Analysis Platform

A comprehensive statistical analysis platform powered by Python and R CRAN libraries. Statistica provides an intuitive web interface for running various statistical tests, from basic descriptive statistics to advanced hypothesis testing.

### link to access tool
https://replit.com/@plantbreeder202/Agri-Statistics?s=app
## Features

### Statistical Tests Available

1. **Descriptive Statistics**
   - Mean, median, mode
   - Standard deviation, variance
   - Quartiles, IQR
   - Skewness, kurtosis
   - Confidence intervals

2. **T-Tests**
   - One-sample t-test
   - Independent samples t-test
   - Paired samples t-test
   - Effect size (Cohen's d)

3. **ANOVA**
   - One-way ANOVA
   - Effect size (eta-squared)
   - Group statistics

4. **Chi-Square Tests**
   - Test of independence
   - Goodness of fit test
   - Effect size (Cramér's V)

5. **Correlation Analysis**
   - Pearson correlation
   - Spearman rank correlation
   - Confidence intervals

6. **Regression Analysis**
   - Simple linear regression
   - R² and adjusted R²
   - F-statistic

7. **Normality Tests**
   - Shapiro-Wilk test
   - Kolmogorov-Smirnov test

8. **Non-Parametric Tests**
   - Mann-Whitney U test
   - Wilcoxon signed-rank test
   - Kruskal-Wallis H test

## Tech Stack

### Frontend
- React + TypeScript
- Vite
- Tailwind CSS
- shadcn/ui components
- GSAP for animations

### Backend
- Python Flask
- NumPy & Pandas for data manipulation
- SciPy for statistical computations
- R integration via rpy2 (optional)

## Installation

### Prerequisites
- Node.js 18+
- Python 3.9+
- R (optional, for extended functionality)

### Frontend Setup

```bash
cd app
npm install
npm run dev
```

### Backend Setup

```bash
cd backend
pip install -r requirements.txt
python start_server.py
```

The backend server will start on `http://localhost:5000`.

## API Endpoints

### Descriptive Statistics
- `POST /api/descriptive` - Calculate descriptive statistics

### T-Tests
- `POST /api/ttest/one-sample` - One-sample t-test
- `POST /api/ttest/independent` - Independent samples t-test
- `POST /api/ttest/paired` - Paired samples t-test

### ANOVA
- `POST /api/anova/one-way` - One-way ANOVA

### Chi-Square
- `POST /api/chisquare/independence` - Chi-square test of independence
- `POST /api/chisquare/goodness-of-fit` - Chi-square goodness of fit

### Correlation
- `POST /api/correlation` - Pearson and Spearman correlation

### Regression
- `POST /api/regression/linear` - Simple linear regression

### Normality Tests
- `POST /api/normality/shapiro-wilk` - Shapiro-Wilk test
- `POST /api/normality/kolmogorov-smirnov` - Kolmogorov-Smirnov test

### Non-Parametric Tests
- `POST /api/nonparametric/mann-whitney` - Mann-Whitney U test
- `POST /api/nonparametric/wilcoxon` - Wilcoxon signed-rank test
- `POST /api/nonparametric/kruskal-wallis` - Kruskal-Wallis H test

## Request/Response Format

### Example: Independent T-Test

**Request:**
```json
{
  "group1": [12, 15, 18, 14, 16, 19, 13, 17],
  "group2": [22, 25, 28, 24, 26, 29, 23, 27],
  "equal_var": true
}
```

**Response:**
```json
{
  "success": true,
  "data": {
    "test": "Independent Samples T-Test",
    "equal_variances_assumed": true,
    "group1": {
      "n": 8,
      "mean": 15.5,
      "std": 2.33
    },
    "group2": {
      "n": 8,
      "mean": 25.5,
      "std": 2.33
    },
    "t_statistic": -8.485,
    "p_value": 0.000001,
    "significance": "p < 0.001 ***",
    "df": 14,
    "cohens_d": -4.24,
    "effect_size": "Large"
  }
}
```

## Development

### Frontend Development
```bash
cd app
npm run dev
```

### Backend Development
```bash
cd backend
python start_server.py --debug
```

### Building for Production
```bash
cd app
npm run build
```

## License

MIT License - Built for analysts, researchers, and teams.
