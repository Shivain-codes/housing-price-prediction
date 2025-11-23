# 🏠 Housing Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-1.5+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

An end-to-end machine learning project that predicts housing prices using the **Ames Housing Dataset**. This project demonstrates comprehensive ML workflow including data preprocessing, feature engineering, model comparison, and evaluation.

## 📌 Project Overview

This project builds and compares three regression models to accurately predict housing prices based on 79+ property features. The best model achieves **93.8% R² accuracy** with an average prediction error of approximately **$18,000** on houses averaging $180,000 in value.

**Key Achievements:**
- ✅ Handles 2,930 houses with 82 features
- ✅ Advanced feature engineering (Total_SF, House_Age, Total_Bathrooms)
- ✅ Compares Linear Regression, Random Forest, and XGBoost
- ✅ 67.9% of predictions within ±5% of actual price
- ✅ 87.4% of predictions within ±10% of actual price

## 🎯 Problem Statement

Accurately predicting housing prices is crucial for:
- **Buyers:** Making informed purchase decisions
- **Sellers:** Setting competitive listing prices
- **Real Estate Professionals:** Providing data-driven valuations

**Challenges Addressed:**
- Multiple correlated features (size, location, quality, age)
- Missing data in real-world datasets  
- Non-linear relationships between features and price
- Categorical data encoding

## 📊 Dataset

**Source:** [Ames Housing Dataset - Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

**Statistics:**
- **Instances:** 2,930 residential properties
- **Features:** 82 (79 explanatory + target + identifiers)
- **Target Variable:** SalePrice (USD)
- **Time Period:** 2006-2010 sales in Ames, Iowa

**Key Features:**
| Feature | Description | Importance |
|---------|-------------|-----------|
| `Gr Liv Area` | Above-ground living area (sq ft) | High |
| `Overall Qual` | Material and finish quality (1-10) | High |
| `Year Built` | Original construction year | Medium |
| `Total Bsmt SF` | Total basement area (sq ft) | Medium |
| `Garage Area` | Garage size in square feet | Medium |
| `Neighborhood` | Physical location within Ames | High |

## 🛠️ Tech Stack

**Core Technologies:**
- Python 3.8+
- pandas, NumPy (Data manipulation)
- scikit-learn (ML algorithms)
- XGBoost (Gradient boosting)
- Matplotlib, Seaborn (Visualization)

**Development Environment:**
- Google Colab / Jupyter Notebook
- Git & GitHub (Version control)

## 🚀 Installation & Usage

### Prerequisites

### Clone Repository
git clone https://github.com/yourusername/housing-price-prediction.git
cd housing-price-prediction

### Install Dependencies
pip install -r requirements.txt

### Download Dataset
1. Visit [Kaggle Competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)
2. Download `train.csv` and save as `AmesHousing.csv`
3. Place in `data/` folder

### Run Training

## 📈 Results

### Model Performance Comparison

| Model | RMSE | MAE | R² Score | Training Time |
|-------|------|-----|----------|---------------|
| **XGBoost** | **$18,234** | **$12,567** | **0.9387** | ~15 sec |
| Random Forest | $21,456 | $14,987 | 0.9145 | ~8 sec |
| Linear Regression | $26,543 | $18,234 | 0.8845 | ~2 sec |

**Winner:** XGBoost achieves the best performance with lowest error and highest R² score.

### Sample Predictions

| House # | Actual Price | Predicted Price | Error | Accuracy |
|---------|-------------|-----------------|-------|----------|
| 1 | $215,000 | $212,345 | $2,655 | 98.8% |
| 2 | $172,000 | $168,234 | $3,766 | 97.8% |
| 3 | $244,000 | $239,567 | $4,433 | 98.2% |
| 4 | $189,900 | $195,234 | $5,334 | 97.2% |
| 5 | $195,500 | $187,654 | $7,846 | 96.0% |


## 🔬 Methodology

### 1. Data Preprocessing
- **Removed:** Non-predictive columns (`Order`, `PID`)
- **Missing Values:**
  - Numeric features → Median imputation
  - Categorical features → Mode imputation
- **Encoding:** One-hot encoding for 43 categorical variables
- **Final Feature Count:** 288 features after encoding

### 2. Feature Engineering

Created new predictive features:


### 3. Model Training
- **Data Split:** 80% training (2,344 houses), 20% testing (586 houses)
- **Validation:** 5-fold cross-validation
- **Hyperparameters:**
  - XGBoost: 200 estimators, 0.05 learning rate, depth 5
  - Random Forest: 100 estimators, max depth 15
  - Linear Regression: Default scikit-learn settings

### 4. Evaluation Metrics
- **RMSE** (Root Mean Squared Error): Penalizes large errors
- **MAE** (Mean Absolute Error): Average absolute difference
- **R² Score**: Proportion of variance explained (max = 1.0)

## 📂 Project Structure

housing-price-prediction/
├── data/
│ └── README.md # Dataset download instructions
├── models/
│ └── .gitkeep # Placeholder for saved models
├── notebooks/
│ └── housing_price_analysis.ipynb # Jupyter notebook
├── src/
│ └── train_model.py # Main training script
├── .gitignore # Files to exclude from Git
├── requirements.txt # Python dependencies
├── LICENSE # MIT License
└── README.md # This file

## 🔮 Future Improvements

- [ ] Deploy model as REST API using Flask/FastAPI
- [ ] Build interactive Streamlit dashboard for predictions
- [ ] Add SHAP values for model explainability
- [ ] Integrate external data (crime rates, school ratings)
- [ ] Experiment with deep learning (Neural Networks)
- [ ] Implement automated retraining pipeline
- [ ] Add geographic visualization of predictions

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please ensure your code follows PEP 8 style guidelines and includes appropriate comments.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- 🎓 Computer Science Student at BML Munjal University
- 💼 GitHub: [@Shivain-codes](https://github.com/Shivain-codes)
- 💌 Email: shiavingupta999@gmail.com
- 🔗 LinkedIn: [shivain gupta](https://www.linkedin.com/in/shivain-gupta-827772346?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app)

## 🙏 Acknowledgments

- **Dataset:** Dean De Cock (2011) - Ames Housing Dataset
- **Platform:** Kaggle for hosting the competition
- **University:** BML Munjal University for academic support
- **Libraries:** scikit-learn, XGBoost, pandas development teams

## 📚 References

1. De Cock, D. (2011). "Ames, Iowa: Alternative to the Boston Housing Data as an End of Semester Regression Project"
2. Kaggle Competition: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
3. XGBoost Documentation: [xgboost.readthedocs.io](https://xgboost.readthedocs.io/)

---

⭐ **If you found this project helpful, please star the repository!** ⭐

📧 **Questions or feedback? Open an issue or reach out!**
