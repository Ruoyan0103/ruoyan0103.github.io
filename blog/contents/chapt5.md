## Chapter 5. Train and Evaluate Your Model
### The Simplest Appropriate Model
1. No need to try <span style="color:blue">every</span> model, it might add unknown 
<span style="color:blue">assumptions</span> about the data in the way they learn. 
- Different models make different assumptions about the data.
- Model explainability and interpretability, such as verifying that our models are not biased in undesirable ways or explaining to a user what they could do to <span style="color:blue">improve</span> prediction results
- Deployable. Consider whether you can <span style="color:blue">deploy</span> it.
- The prediction time for user not only include inference, but data processing.

2. From Patterns to Models
- Some models are affected by feature scales. <span style="color:blue">(use zero mean, and unit variance.)</span>
- Convolutional neural networks (CNNs) have proven useful through their ability to learn <span style="color:blue">translation-invariant filters</span>.

3. Split Your Dataset
- Validation dataset: 
> _cross-validation_ (control variance due a particular choice of validation set)
> _hyperparameter tuning_ (tune **hyperparameters** on validation set the same way as tune **parameters** on training set)
- Test dataset: **unseen data**, only use it at the very end.
- **Data leakage**: For example, features that would not be available at prediction time will lead to overly optimistic performance estimates.

4. Judge performance
- Overfitting (high variance), underfitting (high bias). 
- Either high bias or high variance, the error is high. When validation error is much higher than training error, the model has higher variance comparing to bias. Or the other way round.

### Evaluate Your Model: Look Beyond Accuracy
1. Confusion Matrix

2. ROC curve

3. Calibration curve

4. Dimension reduction visualization

5. Top-k best performace examples, to identify which <span style="color:blue">features</span> the model is leveraging well.

6. Worst-k performace examples, to identify which <span style="color:blue">additional features</span> needed. AND on validation dataset, check these examples to see how the training and validation datasets differ.

7. Top-k uncertain examples.


### Evaluate Feature Importance
1. Simple models: get <span style="color:blue">feature importance scores</span>.

2. Ablation study: remove one feature at a time, and see how the model performance changes.







