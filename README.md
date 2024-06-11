# $R^2$
---

The $R^2$ score, also known as the coefficient of determination, is a statistical measure that helps evaluate the goodness-of-fit of a regression model. It indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. Here’s how the $R^2$ score can help in choosing the best regression model:

1. **Explained Variance**: The $R^2$ value ranges from 0 to 1. An $R^2$ of 0 means that the model does not explain any of the variance in the dependent variable, while an $R^2$ of 1 means that the model explains all the variance. Higher $R^2$ values indicate better fit and more accurate predictions.

2. **Comparison of Models**: When comparing multiple regression models, the $R^2$ score can help determine which model better fits the data. A model with a higher $R^2$ score is generally preferred, as it indicates a better fit to the observed data.

3. **Model Complexity**: While a higher $R^2$ score indicates a better fit, it is also essential to consider the complexity of the model. Overly complex models (those with many parameters) can lead to overfitting, where the model performs well on the training data but poorly on new, unseen data. Therefore, it's often useful to consider adjusted $R^2$ for multiple regression models, which adjusts the $R^2$ value based on the number of predictors in the model.

4. **Interpretation and Diagnostic**: $R^2$ helps in diagnosing the model performance. If $R^2$ is very low, it suggests that the model might be missing key predictors or that the relationship between the predictors and the response variable is not linear. In such cases, alternative modeling approaches might be considered.

### Limitations of $R^2$ Score

While $R^2$ is a valuable measure, it is not without its limitations:

- **Non-linearity**: $R^2$ does not account for non-linear relationships between the variables. For non-linear models, other metrics or transformations of the variables might be necessary.
- **Predictive Performance**: A high $R^2$ does not necessarily mean that the model has good predictive power, especially if the model is overfitted to the training data.
- **Incremental Improvement**: Adding more predictors to a model will generally increase $R^2$, but this does not always mean that the new model is better. It is important to evaluate whether the increase in $R^2$ justifies the added complexity.

### Using Adjusted $R^2$

To account for the number of predictors and avoid overfitting, the adjusted $R^2$ score can be used. Adjusted $R^2$ adjusts the $R^2$ value based on the number of predictors in the model, providing a more accurate measure of model performance, particularly when comparing models with different numbers of predictors.

### Summary

- Use $R^2$ to measure how well the model explains the variance in the dependent variable.
- Compare $R^2$ scores of different models to select the one with a better fit.
- Consider adjusting $R^2$ to account for the number of predictors and avoid overfitting.
- Be aware of the limitations of $R^2$
 and supplement it with other diagnostic tools and validation techniques to ensure robust model selection.

The $R^2$ score, or coefficient of determination, measures how well the regression model explains the variation of the dependent variable. It is calculated using the following formula:

$R^2 = 1 - \frac{SS_{\text{res}}}{SS_{\text{tot}}}$

where:
- $SS_{\text{res}}$ (Residual Sum of Squares) is the sum of the squared differences between the observed values and the predicted values.
- $SS_{\text{tot}}$ (Total Sum of Squares) is the sum of the squared differences between the observed values and the mean of the observed values.

Here are the steps to calculate $R^2$:

1. **Calculate the Mean of the Observed Values $(\bar{y})$**:
   
   $\bar{y} = \frac{1}{n} \sum_{i=1}^{n} y_i$

3. **Calculate $SS_{\text{tot}}$**:
   
   $SS_{\text{tot}} = \sum_{i=1}^{n} (y_i - \bar{y})^2$

5. **Calculate the Predicted Values $(\hat{y_i})$** using the regression model.

6. **Calculate  $SS_{\text{res}}$**:
   
   $SS_{\text{res}} = \sum_{i=1}^{n} (y_i - \hat{y_i})^2$

8. **Calculate $R^2$**:
   
   $R^2 = 1 - \frac{SS_{\text{res}}}{SS_{\text{tot}}}$
