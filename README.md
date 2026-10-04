Dataset generated with shape: (4000, 6)

--- 1. Stratified Split ---
Train set shape: (3200, 5), Test set shape: (800, 5)
Train class balance: [0.85 0.15]
Test class balance:  [0.85 0.15]

--- 2. Missing Value Comparison (Column: income) ---
Raw Drop:   Mean = 66085.12, Std = 73210.45 (Rows retained: 3008)
Median Imp: Mean = 64391.20, Std = 71204.18
KNN Imp:    Mean = 65980.40, Std = 72890.11

--- 3. Outlier Flagging ---
IQR Flags:        284
Z-Score Flags:    38
Percentile Flags: 62
Overlap (IQR & Z-score):    38
Overlap (IQR & Percentile): 62

--- 4. Feature Encoding Columns ---
Initial categorical columns: 3
After One-Hot Encoding:      5
After Ordinal Encoding:      5
After Frequency Encoding:    5

--- 5. Handling Unseen Categories ---
Transformed output with unseen category (all zeros in dummy positions):
[[0. 0. 0.]
 [0. 0. 1.]]

--- 6. Scaling Comparison ---
Saved scaling_comparison.png successfully.

--- 7. Skewness Transformation ---
Original Skewness:      3.4210
After log1p:            0.4128
After Yeo-Johnson:      0.0312

--- 8. Pipeline Output Shapes ---
Train processed shape: (3200, 6)
Test processed shape:  (800, 6)

--- 9. Data Leakage Demonstration ---
Leaked Scaled (first 5):  [-0.3214  0.4128 -0.1205  1.8491 -0.5812]
Correct Scaled (first 5): [-0.3182  0.4173 -0.1179  1.8584 -0.5786]
Absolute Difference:      [0.0032 0.0045 0.0026 0.0093 0.0026]

--- 10. Imbalanced Target Handling ---
Target ratio before SMOTE: [0.85 0.15]
Class counts before SMOTE: [2720  480]
Class counts after SMOTE on train: [2720 2720]
Test set remains untouched with counts: [680 120]

--- 11. Loaded Pipeline Transformation ---
Transformed single test row output:
[[ 0.32514 -0.71241  2.       1.       0.       0.     ]]
