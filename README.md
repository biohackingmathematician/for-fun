# for-fun
Mini projects from my graduate program at Columbia University. Spanning biostatistics, quantitative research, and socioeconomic data analysis.

# Divorce Prediction: Multidimensional Analysis

**A comprehensive data science project analyzing economic, emotional, and psychological predictors of marital dissolution.**

## 📊 Project Overview

This project investigates the complex factors influencing divorce probability using advanced statistical and machine learning techniques. We analyze data from 115 married couples across 30+ variables spanning socioeconomic, emotional, and psychological domains.

**Course:** Advanced Data Analysis  
**Institution:** Columbia University  
**Academic Year:** 2024-2025

---

## 🎯 Research Question

*To what extent can socioeconomic, emotional, and psychological factors predict the likelihood of marital dissolution, and which domain—economic, emotional, or psychological—has the strongest influence on divorce probability?*

---

## 🔑 Key Findings

### Domain Influence Hierarchy
- **Economic Domain:** ~43-44% (education, income, economic similarity)
- **Psychological Domain:** ~43-44% (mental health, addiction, self-confidence)
- **Emotional Domain:** ~14-20% (love, loyalty, commitment)

### Top Individual Predictors
1. **Education** (strongest single factor, ~15% feature importance)
2. Economic Similarity
3. Good Income
4. Mental Health
5. Addiction (key risk amplifier)

### Critical Insights
- ✅ Divorce risk is **interactive, not additive**
- ✅ Economic structure + psychological maturity are both essential
- ✅ Emotional factors amplify but cannot compensate for foundational deficits
- ✅ Nonlinear relationships: diminishing returns after moderate thresholds
- ✅ Three distinct relationship archetypes identified through clustering

---

## 📁 Project Structure

```
divorce-prediction/
├── notebooks/
│   ├── divorce_analysis_professional.ipynb    # Main analysis notebook
│   └── exploratory_analysis.ipynb             # Initial EDA (optional)
├── data/
│   └── README.md                               # Data source information
├── reports/
│   ├── final_report.pdf                        # Academic report
│   └── presentation_slides.pdf                 # Project presentation
├── results/
│   ├── model_performance.csv                   # Model comparison results
│   └── feature_importance.csv                  # Feature importance scores
├── requirements.txt                            # Python dependencies
└── README.md                                   # This file
```

---

## 🛠️ Methodology

### Data Source
- **Original Dataset:** Seyed Mousavi (2017)
- **Sample Size:** 115 married couples
- **Study Duration:** 5 years
- **Variables:** 31 (30 predictors + 1 target)
- **Access:** [Kaggle](https://www.kaggle.com/datasets/hosseinmousavi/marriage-and-divorce-dataset) | [Hugging Face](https://huggingface.co/datasets/hugginglearners/marriage-and-divorce-dataset)

### Statistical Methods

**Traditional Approaches:**
- Ordinary Least Squares (OLS) Regression
- LASSO Regression (L1 regularization)
- ElasticNet (L1 + L2 regularization)
- Bayesian Regression with PyMC
- Generalized Additive Models (Splines)
- One-way ANOVA

**Machine Learning:**
- Random Forest Regression
- Support Vector Machines (SVM)
- Neural Networks (Multilayer Perceptron)
- XGBoost with SHAP values

**Dimensionality Reduction & Clustering:**
- t-SNE visualization
- UMAP (Uniform Manifold Approximation)
- K-Means clustering

**Model Interpretation:**
- Partial Dependence Plots (PDPs)
- Permutation Importance (grouped by domain)
- SHAP (SHapley Additive exPlanations)

---

## 📈 Results Summary

### Model Performance (Test Set)
| Model | Test R² | Test RMSE | Notes |
|-------|---------|-----------|-------|
| Random Forest | 0.70-0.85 | 0.22 | Best overall performance |
| OLS | 0.65-0.75 | 0.25 | Strong baseline, interpretable |
| LASSO | 0.60-0.70 | 0.27 | Good feature selection |
| ElasticNet | 0.60-0.70 | 0.27 | Robust generalization |
| SVM | -0.10-0.20 | 0.45 | Poor for small data |
| Neural Network | -1.88-0.30 | 0.60 | Overfits with n=115 |

### Three Relationship Archetypes
1. **High-Risk / Emotionally Unstable:** Low education, high addiction, volatility
2. **Balanced / Economically Grounded:** Strong income/education, moderate stability
3. **Secure / Psychologically Resilient:** Strong mental health, high confidence

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
Jupyter Notebook or VS Code with Jupyter extension
```

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/biohackingmathematician/for-fun.git
cd for-fun/biostatistics/divorce-prediction
```

2. **Create virtual environment:**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. **Install dependencies:**
```bash
pip install -r requirements.txt
```

4. **Launch notebook:**
```bash
jupyter notebook notebooks/divorce_analysis_professional.ipynb
```

### Running the Analysis

The notebook is organized into 20 sections:
1. Setup and Data Loading
2. Exploratory Data Analysis
3. Data Preparation
4-8. Model Building (OLS, LASSO, RF, SVM, NN)
9. Model Comparison
10. Partial Dependence Analysis
11-13. Domain-Based Analysis
14. Dimensionality Reduction & Clustering
15. Advanced Techniques
16. Mental Health Simulation
17. Psychological Factor Analysis
18. ANOVA Testing
19. Final Summary
20. Results Export

**Expected Runtime:** 5-10 minutes (full notebook)

---

## 📊 Key Visualizations

- Correlation heatmap of all predictors
- Distribution plots for key variables
- Random Forest feature importance
- Partial dependence plots
- UMAP/t-SNE 2D embeddings
- Cluster visualizations
- Domain influence bar charts
- Mental health simulation curves

---

## 💡 Practical Implications

### For Marriage Counseling
- Address economic literacy and financial planning
- Screen for mental health issues (especially addiction)
- Provide integrated interventions (economic + psychological)
- Tailor approaches to relationship archetype

### For Public Policy
- Education programs benefit relationship outcomes
- Mental health services crucial for at-risk couples
- Target low-education, low-income couples for highest impact
- Addiction treatment should be prioritized

### For Individuals
- Education protects through multiple pathways
- Mental health is as important as financial stability
- Emotional connection needs supporting structures
- Small improvements across domains compound

---

## 🔬 Methodological Contributions

1. **Domain-based framework:** Novel grouping of predictors into theoretical domains
2. **Interactive effects:** Demonstrated that divorce risk is conditional, not additive
3. **Multiple method validation:** Convergent evidence across 10+ analytical approaches
4. **Nonlinear patterns:** Identified saturation effects and threshold relationships
5. **Archetype discovery:** Used unsupervised learning to find natural relationship types

---

## 📚 References

### Data Source
Mousavi, S. (2017). *Marriage and Divorce Dataset*. Retrieved from Kaggle/Hugging Face.

### Methodology
- James, G., et al. (2021). *An Introduction to Statistical Learning*
- Hastie, T., et al. (2009). *The Elements of Statistical Learning*
- Lundberg, S. M., & Lee, S. I. (2017). A unified approach to interpreting model predictions (SHAP)
- McInnes, L., et al. (2018). UMAP: Uniform Manifold Approximation and Projection

### Substantive Literature
- Gottman, J. M. (1994). *What Predicts Divorce?*
- Amato, P. R. (2010). Research on divorce: Continuing trends and new developments
- Bramlett, M. D., & Mosher, W. D. (2002). Cohabitation, marriage, divorce in the United States

---

## 🤝 Contributing

This is an academic project, but we welcome:
- Bug reports and fixes
- Suggestions for additional analyses
- Questions about methodology
- Discussions about findings

Please open an issue or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Authors

**Team Members:**
- [Your Name] - Lead Analyst & Modeling
- [Classmate Names] - Data Processing & Visualization
- [Classmate Names] - Statistical Testing & Validation

**Course Instructor:** [Professor Name]  
**Institution:** Columbia University

---

## 🙏 Acknowledgments

- Course: Advanced Data Analysis (Fall 2024)
- Professor [Name] for guidance and feedback
- Original data collectors (Seyed Mousavi, 2017)
- Open-source community (scikit-learn, PyMC, SHAP, UMAP)
- Columbia University for resources and support

---

## 📬 Contact

For questions about this project:
- **Email:** [your.email@columbia.edu]
- **GitHub Issues:** [Open an issue](https://github.com/biohackingmathematician/for-fun/issues)

---

<div align="center">

**📊 Data-Driven Insights into Relationship Dynamics**

*Columbia University | Advanced Data Analysis | 2024-2025*

[View Full Repository](https://github.com/biohackingmathematician/for-fun) • [Report Issue](https://github.com/biohackingmathematician/for-fun/issues) • [Request Feature](https://github.com/biohackingmathematician/for-fun/issues)

</div>
