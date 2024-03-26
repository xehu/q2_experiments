# q2_experiments

The Q^2 is a statistical quantity derived from the jackknifed residuals of the prediction sum of squares (PRESS), also known as leave-one-out cross validation.

The general idea behind this metric is that we want to measure the “goodness of fit” of a model through its loss (i.e., reduction of error); Q^2 therefore measures the proportion by which the model reduces error on the PRESS of squares residuals.

Q^2 has a number of key benefits: because of its similarity to the familiar metric R^2, it is interpretable and intuitive; however, because it is sensitive to outliers, Q^2 is more effective at detecting influential observations (i.e., measuring data quality), and is also sensitive to overfitting -- if you overfit a model by adding many explanatory variables, you can raise the R^2 but you will ultimately deflate the Q^2 if you end up with a huge residual on the “held-out” value.

However, there is a possibility that Q^2 generates biased estimates due to the cross-validation at the heart of the approach. See [this document](https://docs.google.com/document/d/12p1ZIXzdDf2HkRRlxjZTLISoBtR7isxCjMiiBeOFViQ/edit) for more background on the advantages and challenges of the Q^2 metric.

The objective of this repository is to empirically explore possible biases, limitations, and advantages of Q^2.
