# summary-for-2009.05241
Tianhao Wang1, Yuheng Zhang2, Ruoxi Jia3

## Summary
The paper has proposed Mutual Information Regularisation based defence (MID) against MI attacks. Paper also presents various approximations 
to the regularizer for linear regression, descision trees and neural networks. It also highlights inefficacy of DP in defending against  MI attacks.

### Idea
MI attacks exploit the correlation between model input and output.The idea is to limit this relation to a certain extent such that utility of the model does not fade away as well.

### Problem-Setup
The attacker ha access to a model that ouptuts label for images.Attcker's goal is to find representational image for the label y building upon some auxilary knowledge about the data that he might have. Our goal is to train the model such that access to model does not allow attacker to infer information about X(image).

### Loss Function.
![This is an image](https://github.com/Tanishq-01/summary-for-2009.05241/blob/main/Screenshot%202022-08-25%20032519.png)

Here the loss function contains two terms.First term is the loss function for the classifiaction task. The second term is the proposed regularizer and it promotes uncertainty of output for a given input. I other words different inputs be mappped to same or very similar outputs(for a given input) which also increases the variance.
This makes X to be less likely determined from a given y.
lambda here in second term is a normal constant which we can control to intensify the effect of regularizer term.

![](https://github.com/Tanishq-01/summary-for-2009.05241/blob/main/Screenshot%202022-08-25%20034500.png)

It can be inferred from images that including the regularizer term has made distribution of predicted values concentrated across lot of labels instead of single label.


