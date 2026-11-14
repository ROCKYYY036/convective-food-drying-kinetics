# Python-Based Convective Food-Drying Kinetics and Model Comparison

**Author:** Md. Rakibul Islam Rocky  
**Affiliation:** Dept. of Mechanical Engineering, Rajshahi University of Engineering & Technology (RUET)  
**Research Focus:** Scientific Computing, Transport Phenomena, Physics-Informed Neural Networks (PINNs)

---

## 📌 Overview
This repository contains a reproducible Python workflow for fitting and evaluating classical thin-layer drying kinetics models (Newton, Page, and Henderson–Pabis) against published experimental convective drying data for apple slices at 50°C. 

This work provides a quantitative **conventional modeling baseline** for upcoming research exploring Physics-Informed Neural Networks (PINNs) for uncertainty-aware food dehydration modeling.

---

## 📊 Summary of Model Performance

| Model | Parameters | RMSE | MAE | $R^2$ |
| :--- | :---: | :---: | :---: | :---: |
| **Newton** | $k = 0.01582\text{ min}^{-1}$ | 0.01888 | 0.01607 | 0.9956 |
| **Page** | $k = 0.01317$, $n = 1.0424$ | **0.01765** | **0.01595** | **0.9961** |
| **Henderson–Pabis** | $a = 1.0041$, $k = 0.01589$ | 0.01883 | 0.01650 | 0.9956 |

### Key Findings:
1. **Model Goodness-of-Fit:** All three models fit the experimental data well ($R^2 > 0.995$), with the **Page model** providing the lowest error ($RMSE = 0.01765$).
2. **Residual Structure:** Residual plots reveal systematic U-shaped bias, indicating empirical inadequacy in capturing the physical transition across drying phases.
3. **Sensitivity Analysis:** The Page model is significantly more sensitive to the shape exponent $n$ than the rate constant $k$.

---

## 🚀 How to Run the Code

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/convective-food-drying-kinetics.git
   cd convective-food-drying-kinetics
   ```

2. Install dependencies:
   ```bash
   pip install numpy scipy matplotlib pandas
   ```

3. Run the analysis:
   ```bash
   python drying_kinetics.py
   ```

---

## 📄 Technical Report
Read the full report: [`Rocky_2026_Convective_Drying_Kinetics_Baseline.pdf`](./Rocky_2026_Convective_Drying_Kinetics_Baseline.pdf)

---

## 📚 Reference
* Menges, H. O., & Ertekin, C. (2006). *Mathematical Modeling of Thin Layer Drying of Golden Apples*. **Journal of Food Engineering**, 77(1), 119-125.
