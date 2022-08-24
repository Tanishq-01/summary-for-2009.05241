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
![This is an image]()


