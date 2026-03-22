# Statistica - Professional Statistical Analysis Suite

## Overview
A client-side statistical analysis web application built with vanilla HTML, CSS, and JavaScript. All statistical computations are performed in the browser using math.js and Chart.js loaded from CDN.

## Project Structure
```
.
├── Index1.html   # Main application (single-file: HTML + CSS + JS)
├── serve.py      # Python HTTP server to serve the app on port 5000
├── README.md     # Project documentation
└── replit.md     # This file
```

## Features
- Descriptive Statistics (mean, median, mode, std dev, variance, quartiles, skewness, kurtosis)
- Hypothesis Testing (T-tests, ANOVA, Chi-Square)
- Correlation & Regression (Pearson/Spearman, linear regression)
- Normality Tests (Shapiro-Wilk approximation, skewness, kurtosis tests)
- Non-Parametric Tests (Mann-Whitney U, Wilcoxon, Kruskal-Wallis)

## Tech Stack
- **Frontend**: Vanilla HTML5 / CSS3 / JavaScript (single file: Index1.html)
- **Libraries (CDN)**: math.js, Chart.js, Google Fonts
- **Server**: Python `http.server` (serve.py) on port 5000

## Running the App
The app is served via `python serve.py` which binds to `0.0.0.0:5000`.

## Deployment
Configured for autoscale deployment using `python serve.py`.
