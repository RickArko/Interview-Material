# Classification Performance Metrics

## Accuracy
The fraction of predictions the model gets right.
$$
Accuracy = \frac{TP+TN}{TP+TN+FP+FN}
$$

## Precision
What proportion of position predictions is correct.
$$
Precision = \frac{TP}{TP+FP}
$$

## Recall
What proportion of actual positives was correctly identified.
$$
Recall = \frac{TP}{TP+FN}
$$

## F1
The F1-score combines the precision and recall of a classifier into a single metric by taking their **harmonic mean**. It is primarily used to compare the performance of two classifiers. Suppose that classifier A has a higher recall, and classifier B has higher precision. In this case, the F1-scores for both the classifiers can be used to determine which one produces better results.

$$
F1 = \frac{2*Precision*Recall}{Precision+Recall} = \frac{2*TP}{2*TP+FP+FN}
$$

## Sensitivity
Sensitivity is a measure of how well a machine learning model can detect positive instances. It is also known as the **true positive rate (TPR)** or **recall**. Sensitivity is used to evaluate model performance because it allows us to see how many positive instances the model was able to correctly identify

$$
Sensitivity = Recall = \frac{TP}{TP+FN}
$$

## Specificity
Specificity measures the proportion of true negatives that are correctly identified by the model. This implies that there will be another proportion of actual negative which got predicted as positive and could be termed as false positives. This proportion could also be called a **True Negative Rate (TNR)**. The sum of specificity (true negative rate) and false positive rate would always be 1. High specificity means that the model is correctly identifying most of the negative results, while a low specificity means that the model is mislabeling a lot of negative results as positive.

$$
Specificity = \frac{TN}{FP+TN}
$$
