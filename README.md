# ML-Based-Risk-Prediction-Model-for-Loan-Applications-Enhancing-Decision-Making-and-Prevention
## 📌 Introduction
The goal of this project was to develop and evaluate machine learning models for predicting loan approval outcomes. We trained three classification models—**Logistic Regression, Random Forest, and XGBoost**—on historical loan application data. To assess their performance, we applied **confusion matrices, ROC curves, feature importance analysis, and prediction distributions**.

This analysis not only helps in **choosing the best model for deployment** but also provides **valuable business insights** for financial institutions.

---

## 📍 Model Performance Evaluation

### **1️⃣ Logistic Regression Model Evaluation**
- **Accuracy:** **90.76%**
- **Key Findings:**  
  - High accuracy but **poor recall** for approved applications.  
  - Precision and recall for **approved loans (class 1) are extremely low (0.00)**, meaning the model fails to correctly identify successful loan applicants.

### **2️⃣ Random Forest Model Evaluation**
- **Accuracy:** **90.35%**
- **Key Findings:**  
  - Performs similarly to logistic regression.  
  - Also **fails to predict successful applications** due to class imbalance.

### **3️⃣ XGBoost Model Evaluation**
- **Accuracy:** **89.67%**
- **Key Findings:**  
  - Slightly lower accuracy but **better recall for approved applications (class 1: recall = 7%)** compared to other models.  
  - More **balanced performance** than logistic regression and random forest.

🛑 **Issue:** All models struggle with **class imbalance**, leading to poor recall for approved loans. This means **many potential good applicants are being rejected.**

---

## 📍 Key Findings & Insights

### **1️⃣ Confusion Matrix Analysis (Misclassifications)**
- **Purpose:** Shows how well the models distinguish between approved and rejected applications.
- **Findings:**  
  - The **Random Forest and Logistic Regression models** had a **high rate of false negatives**, failing to approve valid applications.
  - XGBoost improved slightly but still showed **weak recall for successful loans**.
- **Business Impact:**  
  - A high false positive rate (**wrongly approving risky loans**) can **increase default rates**, leading to financial losses.
  - A high false negative rate (**wrongly rejecting safe applicants**) can **reduce revenue potential** and **damage customer relationships**.

✅ **Optimized model selection reduces bad loans while maximizing approval of creditworthy customers.**

---

### **2️⃣ ROC Curve & Model Performance**
- **Purpose:** Evaluates how well each model distinguishes between approved and rejected loans.
- **Findings:**  
  - The **XGBoost model achieved the highest AUC score**, meaning it **provides the best trade-off between recall and precision**.
  - Logistic Regression and Random Forest had similar AUC values but suffered from **zero recall for approved loans**.
- **Business Impact:**  
  - **Better model accuracy means more reliable lending decisions.**  
  - Higher recall ensures **fewer missed opportunities**, while higher precision reduces **approval of high-risk applicants**.

✅ **A strong ROC curve ensures that lenders minimize financial risk while maintaining profitability.**

---

### **3️⃣ Feature Importance (Key Factors in Loan Approval)**
- **Purpose:** Identifies which features impact loan approval decisions the most.
- **Findings:**  
  - The most influential factors included **loan amount, term length, employment type, and applicant's credit history.**
  - Features related to **outstanding balance and past defaults** strongly influenced loan decisions.
- **Business Impact:**  
  - Helps banks **streamline the approval process** by focusing on the most impactful factors.
  - Enables **personalized loan offers** based on applicant profiles.
  - Improves transparency in credit risk assessment, reducing regulatory and compliance risks.

✅ **A data-driven loan approval strategy helps improve risk management and customer satisfaction.**

---

### **4️⃣ Prediction Distribution (Model Alignment with Real Data)**
- **Purpose:** Compares actual vs predicted loan approvals to assess model bias.
- **Findings:**  
  - The **Random Forest and XGBoost models closely aligned with actual data**, showing high accuracy.
  - Logistic Regression had a **wider variance**, indicating a less reliable prediction pattern.
- **Business Impact:**  
  - If a model consistently over-predicts approvals, banks **increase their default exposure**.
  - If a model under-predicts approvals, banks **miss out on potential revenue**.
  - **Balanced predictions ensure a steady flow of approved loans while managing risk.**

✅ **A well-calibrated model helps financial institutions strike the right balance between growth and risk.**

---

## 📍 Final Business Impact Summary
✅ **Improved Loan Approval Efficiency** → Reduces manual review time & accelerates decisions.
✅ **Lower Default Rates** → Data-driven approvals minimize high-risk loans.
✅ **Increased Revenue** → Fewer false rejections mean **more approved loans & higher profits**.
✅ **Better Customer Experience** → Faster and fairer decisions lead to **higher customer trust**.
✅ **Regulatory Compliance** → Transparency in loan decisions aligns with financial regulations.

**🚀 Deploying the best-performing model (XGBoost) with class balancing techniques will maximize profitability, reduce risk, and enhance customer experience in loan processing.**
