# Concept
**Machine Learning = Looking for Function**

**Different types of Functions:**
1. **`Regression`:** The function outputs a scalar
2. **`Classification`:** Given options(classes), the function outputs the correct one  
* **eg.** AlphaGo 19 * 19 each position is a class
3. **`Stuctured Learning`:** The function create something with structure(image, document)

**Steps to find the function(but just training, not on unseen test data):**
1. **Function with unknown parameters** (based on domain knowledge)  
* L = b + wx 
* parameters will be learned from data  
* function =  `model`; x =  `feature` 

2. **Define `loss` from training data**
* Loss is a function of parameters: L(b, w)
* Loss evalustes how good the parameter-value-set is
* your loss your pleasure
* **eg.** MAE/MSE/Cross Entropy
* `Label`: $\hat{y}$
* can draw an `Error Surface`
3. **Optimization**
* w*, b* = argmin(L)
* `Gradient Descent` steplength depends on gradient and `hyperparameters`(learning rate...)
	* (Randomly)Pick initial values
	* Compute gradient
	* Update parameters iteratively
	<img src="https://user-images.githubusercontent.com/68600731/147309638-9386c3ab-b412-4693-ad4e-f28406e6e0a1.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147310667-ae3534f3-4b34-4a4f-b3b5-d4343b2d3fb8.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147311365-e80e8e6b-c486-46e0-b0a0-cdc42e7ea452.png" width="300">
* when to stop:
	* I stop it
	* gradient gets stuck at 0 ==> `Local minimum` ==> actually a fake problem
# Assignment





# Question
