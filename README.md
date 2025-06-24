# 🛰️ InSAR Phase Simulation and Deformation Modeling

This project simulates synthetic InSAR (Interferometric Synthetic Aperture Radar) phase data based on a modeled ground deformation event, performs phase unwrapping, and fits a physical model to interpret the deformation. It demonstrates key steps in satellite-based deformation monitoring aligned with modern geodesy and remote sensing techniques.

## 📌 Objectives

- Simulate a ground deformation event (e.g., subsidence)
- Convert it to synthetic SAR phase using the radar wavelength
- Perform 2D phase unwrapping
- Fit a 2D Gaussian model to the deformation to extract physical parameters
- Visualize results and residual errors

## 🧪 Tools & Libraries

- Python 3
- NumPy
- Matplotlib
- SciPy

## 🌀 Workflow

1. **Deformation Simulation**  
   A Gaussian deformation is generated over a 2D grid simulating subsidence (~5 cm).

2. **Phase Generation**  
   The deformation is converted into wrapped phase values using Sentinel-1 radar wavelength (5.6 cm).

3. **Phase Unwrapping**  
   A basic 2D unwrapping algorithm using `np.unwrap()` is applied row- and column-wise.

4. **Model Fitting**  
   The recovered deformation is fitted with a 2D Gaussian model to retrieve amplitude, center, and spread.

## 📊 Sample Results

| Simulation Stage       | Visualization |
|------------------------|---------------|
| Simulated Deformation  | ![Sim](images/simulated_deformation.png) |
| Wrapped Phase          | ![Wrapped](images/wrapped_phase.png)     |
| Unwrapped Phase        | ![Unwrapped](images/unwrapped_phase.png) |
| Fitted Model           | ![Model](images/fitted_gaussian.png)     |
| Residuals              | ![Residual](images/residual_error.png)   |

## 🔍 Physical Parameters Extracted

- **Amplitude**: ~-0.05 m (subsidence)
- **Center**: (x ≈ 0, y ≈ 0)
- **Sigma**: ~10 units

## 🧠 Insights

This simple yet realistic simulation reflects how InSAR data is used in geodesy and satellite interferometry to monitor surface deformation, and demonstrates understanding of the entire chain: from data to model.

## 📂 License

MIT License

## 📬 Contact

Created by Syed Aqib Mehdi | Email: aqibmehdi510@gmail.com
