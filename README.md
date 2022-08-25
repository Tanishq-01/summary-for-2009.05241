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
<img src="https://github.com/Tanishq-01/summary-for-2009.05241/blob/main/Screenshot%202022-08-25%20032519.png" width="400" height="200" />

Here the loss function contains two terms.First term is the loss function for the classifiaction task. The second term is the proposed regularizer and it promotes uncertainty of output for a given input. In other words different inputs be mappped to same or very similar outputs(for a given input) which also increases the variance.
This makes X to be less likely determined from a given y.
lambda here in second term is a normal constant which we can control to intensify the effect of regularizer term.

<img src="https://github.com/Tanishq-01/summary-for-2009.05241/blob/main/Screenshot%202022-08-25%20034500.png" width="400" height="200" />

It can be inferred from images that including the regularizer term has made distribution of predicted values concentrated across lot of labels instead of single label.

### Experiment
The efficacy of MID is commpared against several effective MI attacks. Defense baseline is compared with DP as well as other defences available for single model or attacks as well as some specialised defences.

Evaluation of performance of model is in terms of privacy and utility. We have parameters using which we can inncrease robustness but utility comes down then. Utility is measured by MSE, or f1 score depending on case to case.

### Results
<img src="https://github.com/Tanishq-01/summary-for-2009.05241/blob/main/Screenshot%202022-08-25%20040356.png" width="800" height="200" />

We can see that MID defense achieves better privacy-utility tradeoff compared to other defenses. Another point to notice is that increasing model utility increases the vulnerability to attacks. It has also been shown in the paper that even for whitebox settings the MID defence is much more successful and features cannot be extracted while in other defences they are.

### Conclusion

All in all it can be concluded that MID defence is more successful in almost all settings and the idea of limiting relation between X and y works. What i think can be done further is that we can increase number of subclasses to confuse the attacker.
