# Photometric Redshift Estimation and Spectral Classification of SDSS Sources

## Project Overview
This project investigates different machine learning approaches for estimating redshifts (distance measurements) and performing spectral classification of astronomical sources using photometric data from the Sloan Digital Sky Survey (SDSS). The work explores the accuracy and limitations of different algorithms when applied to stars, quasars (QSOs), and galaxies.

## Research Questions
- How do different ML algorithms perform for photometric redshift estimation across different source types?
- What are the optimal feature sets for distinguishing between stars, QSOs, and galaxies using photometric data?
- How does performance vary across different redshift ranges and source properties?

## Dataset
- SDSS photometric survey data

## Methodology
Machine learning algorithms evaluated:
* Random Forest
* Gradient Boosting
* Decision Tree
* Support Vector Machine
* K-Nearest Neighbors
* Neural Networks

## Notebooks
1. **1_classifying_spectra_type.ipynb** - Source classification using apparent magnitudes with/without colours (difference between apparent magnitudes)
2. **2_determining_redshift.ipynb** - Calculating redshifts using apparent magnitudes and evaluating accuracy for sources z ≤ 1 and z > 1
3. **3_determining_redshift_NN.ipynb** - Redshift estimation using neural networks
4. **4_determining_redshift_NN_color.ipynb** - Neural network approach incorporating color information
5. **5_determining_redshift_extraZ.ipynb** - Artificially augmenting dataset with high-redshift sources to address class imbalance

## Key Findings
- **Classification**: All models improved when incorporating colour information. Gradient Boosting Classifier with colours offers optimal balance of accuracy and computational efficiency. Support Vector Machine provides good alternative when memory usage is critical.
- **Dataset characteristics**: Strong bias toward low-redshift sources affects training performance for high-redshift objects.
- **Feature engineering**: Dividing the dataset by redshift ranges increased accuracy. Colour information improved MSE but did not exceed SDSS photometric pipeline performance.
- **Neural networks**: Showed improved MSE compared to traditional ML algorithms. Colour incorporation provided modest additional improvement.
- **Data augmentation**: Artificially adding high-redshift sources did not improve overall MSE performance.
