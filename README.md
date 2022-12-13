# cis520_final_proj

Problem: Impact of Data Scarcity on Binary Image Classification for Histopathologic Cancer Detection

Data: [PatchCamelyon](https://github.com/basveeling/pcam)

Models:
- Teammates:
  - LogReg
  - K-NN
  - SVM
  - XGBoost
  - CNN
- Me:
  - ResNet (PyTorch)
  - Vision Transformer (Google)
  - Data Exploration, Model Walkthrough

Metrics:
- Confusion Matrix (Accuracy, Precision, Recall, F1-score)
- ROC & AUC

Results:
- When medical image data is scarce, SVC, XGB and CNN are still great options in terms of recall and AUC. They achieve competitive performances with each other (especially XGB), and they take significantly less training and inference time compared to transfer learning.
- Transfer learning is still by far the most reliable on most metrics in both scarce and abundant data settings, but they require huge computational power and time for both training and inference.
- The AUC for most models increased after more training data become available, while the AUC for KNN dropped significantly. Both phenomena are expected.
- In simple models, when recall becomes unusually high, it is mostly accompanied by a low precision (i.e., misclassifying “0” as “1”). Depending on the need of the doctors, this could be useful. However, this could result from randomness in initialization as well.