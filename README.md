# Tanzanian Waterwells Project

## Overview  
The **Tanzanian Waterwells Project** is an initiative aimed at predicting water pump functionality to ensure clean water access for the people of Tanzania. This project utilizes **machine learning (ML)** techniques to classify water wells as **functional, non-functional, or in need of repair**. By leveraging data analysis and model optimization, our goal is to provide the people of Tanzania a ML model that can make accurate predictions on water pumps that are functional and produce clean water.

## Team  
- **Shefat Moral**  
- **Gabriel Santorelli**  
- **David Jimenez**  

## Project Goals  
- Our goal for this project was to build an effective ML model that can predict water pump functionality for the purpose of bringing clean water to the people of Tanzania 🇹🇿.   

---

## Data Exploration (EDA)  
### Key Findings:  
- The dataset contained **three well statuses**:  
  - **Functional**  
  - **Non-Functional**  
  - **Functional Needs Repair**  
- **Functionality by Region:** Analyzed geographic patterns of well status.  
- **Water Quality Analysis:** Functioning wells did not always provide clean water.  
  - Categories like **Unknown, Fluoride Abandoned, and Salty** were among the lowest quality.  

---

## Model Development  
### **Baseline Model: Decision Tree**  
- Initial accuracy: **75%**  
- Strengths: Identified **Class 0 (Functional)** and **Class 2 (Non-Functional)** well.  
- Weakness: Struggled with **Class 1 (Needs Repair)**.
- Class Balancing: Addressed class imbalance with **class_weight** and **SMOTE (Synthetic Minority Over-sampling Technique)**. 

### **Improved Model: Random Forest**  
- Initial accuracy: **79%**  
- Improved precision for **Class 1 (60%)** and **Class 2 (84%)**.  
- Struggled to distinguish **Class 1 from Class 2**.
- Further EDA to determine the next steps in optimization.

### **Feature Engineering & Model Optimization**  
- **Correlating Features:** Engineered features based on relationships (e.g., **gps_height, function_years**).  
- **Hyperparameter Tuning:** Adjusted parameters for better classification performance.
- **Error Analysis:** looked into the features that were potentially causing false positives.
 

### **Final Model Performance**  
- **Optimized Random Forest Model**  
  - **Error Analysis:** Pumps that needed repair weren't producing good water. Grouped Needs Repair with Not functional.
  - **Accuracy:** up to **81%**, that's a 6% increase from our baseline model(75%).
  - **Precision:** up to **.82**, that's a 36% increase from our baseline model(.46).
  - **Recall:** up to **.74**, that's a 42% increase from our baseline model(.32).
  - **F1-Score:** up to **.78**, that's a 40% increase from our baseline model(.38).
  - **Reduced false positives by 200 cases.**
  - **Mean CV Accuracy:** .793, indicating there is no overfitting or data leakage.
  - **Standard deviation:** of **0.0025**, indicating model stability.
  

---

## Future Improvements  
- **Continue Error Analysis:** Keep exploring features that are causing false positives.
- **Explore additional models:** Like SVM, Gradient Boosting, etc., to enhance the accuracy of the model further.

### **Acknowledgments**
- We appreciate the Tanzanian government and local organizations for bringing clean water to communities. Special thanks to our fellow peers and instructor for their guidance throughout this project.
