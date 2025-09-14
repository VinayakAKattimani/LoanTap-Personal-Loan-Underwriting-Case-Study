## Insights & Recommendations  

-  The model is performing well, and further hyperparameter tuning did not significantly improve results.  

-  **Class Imbalance**  
  - Precision for **charged-off loans (class 0)** is low (0.38).  
  - This is likely due to fewer real-world defaults in the dataset.  
  - More balanced data would improve model performance.  

-  **Model Choice**  
  - Logistic Regression works, but given the dataset’s **categorical-heavy features**, alternative models (Random Forest, XGBoost) might yield better predictive power.  

-  **Precision & Sensitivity**  
  - Precision for **loan repayment** = **0.90** → The model correctly identifies 90% of reliable borrowers.  
  - Precision for **charged-off loans** = **0.38** → Lower accuracy in predicting risky borrowers.  
  - Sensitivity for **both classes** = **0.71** → The model captures 71% of true cases for both repaid and defaulted loans.  

-  **Key Features Influencing Outcomes**  
  - `grade`: LoanTap’s internal risk rating plays a major role in prediction.  
  - `pub_rec`: Borrower’s negative public credit records heavily influence outcomes.  

-  **Geographic Insights**  
  - Applicants from certain pincodes (`11650`, `86630`, `93700`) have not made any repayments.  
  - Either data is missing for these regions, or these applicants are **high-risk borrowers**.  
  - LoanTap should carefully evaluate applicants from these regions before disbursing loans.  

---
