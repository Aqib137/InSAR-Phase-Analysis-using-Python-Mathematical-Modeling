# 🛰️ InSAR Phase Analysis using Python + Mathematical Modeling

This project simulates synthetic InSAR (Interferometric Synthetic Aperture Radar) data to model ground deformation using mathematical and geophysical principles. The full process includes deformation modeling, phase wrapping, unwrapping, and Gaussian fitting — a mini pipeline that reflects core tasks in geodesy, remote sensing, and InSAR processing.

---

## 📁 Project Structure
InSAR_Phase_Modeling_Project/
├── notebooks/
│ └── phase_simulation_and_modeling.ipynb
├── images/
│ ├── simulated_deformation.png
│ ├── wrapped_phase.png
│ ├── unwrapped_phase.png
│ ├── fitted_gaussian.png
│ └── residual_error.png
├── report.pdf
└── README.md

---

## 📌 Objectives

- ✅ Simulate ground deformation (e.g., land subsidence)
- ✅ Convert deformation to synthetic InSAR phase
- ✅ Apply phase unwrapping using NumPy
- ✅ Fit a physical (Gaussian) model to recover geophysical parameters
- ✅ Visualize and validate with residual errors

---

## 🌍 Deformation Simulation

A 2D Gaussian subsidence field is generated to mimic a realistic event like land sinking due to groundwater extraction.

### 📷 Simulated Deformation

![Simulated Deformation](images/simulated_deformation.png)

---

## 🌈 Wrapped and Unwrapped Phase

SAR satellites observe phase differences — but these are **wrapped** within `-π to +π`. We unwrap this to estimate actual displacement.

### 📷 Wrapped Phase

![Wrapped Phase](images/wrapped_phase.png)

### 📷 Unwrapped Phase

![Unwrapped Phase](images/unwrapped_phase.png)

---

## 📐 Model Fitting: 2D Gaussian

We fit a Gaussian model to the unwrapped deformation. This helps estimate the physical parameters:
- **Amplitude**
- **Deformation center (x, y)**
- **Standard deviation (σx, σy)**

### 📷 Fitted Model

![Fitted Gaussian](images/fitted_gaussian.png)

### 📷 Residual Error

![Residual Error](images/residual_error.png)

---

## 🧠 Results

| Parameter     | Value (approx.)  |
|---------------|------------------|
| Amplitude     | -0.050 m         |
| Center (x, y) | (0, 0)           |
| Sigma         | (10, 10)         |

Model fitting was accurate, with minimal residual error.

---

## 📄 Report

📥 [Click here to download the full project report (PDF)](report.pdf)

---

## ⚙️ Tools & Libraries

- Python 3.x
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

---

## 👨‍💻 Author

**Syed Aqib Mehdi**  
📧 aqibmehdi.dev@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/YOUR_LINK) *(optional)*  
🎯 PhD Applicant in Geodesy, Remote Sensing, and Quantum-Secure Systems

---

## 📜 License

This project is licensed under the MIT License.

---

> ⭐ *If you find this project useful, feel free to star the repo or share your feedback!*
