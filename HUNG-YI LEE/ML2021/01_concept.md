# Concept
## Machine Learning = Looking for Function

> **Different types of Functions:**
1. **`Regression`:** The function outputs a scalar
2. **`Classification`:** Given options(classes), the function outputs the correct one  
* **eg.** AlphaGo 19 * 19 each position is a class
3. **`Stuctured Learning`:** The function create something with structure(image, document)

> **Steps to find the function(but just training, not on unseen test data):**
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

## Linear models are too simple, we need more sophisticated models ==> `Model Bias`
* all piecewise linear curves ==> constant + a set of __/¯¯  
	<img src="https://user-images.githubusercontent.com/68600731/147311761-20125462-6418-42d9-b783-f0cc9f945687.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147312311-3546f3c5-613d-404a-a539-a25a891b790e.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147312704-5afe21e1-eea1-4a02-abe4-9706f509a7f6.png" width="300">

* `sigmoid` ==> __/¯¯ (hard sigmoid)     
	<img src="https://user-images.githubusercontent.com/68600731/147325915-27b54a1f-76b1-4cef-b2f2-a020ebcbe5c1.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147326082-6cd8c834-2544-49ff-b675-c4da9618cf3b.png" width="300">

* build a sophisticated function   
	<img src="https://user-images.githubusercontent.com/68600731/147330432-07306a43-451c-4066-976f-4d6daf6994bf.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147330548-2d66c2e0-71d9-4f2f-89f6-c39126ddec40.png" width="300">	
	<img src="https://user-images.githubusercontent.com/68600731/147330899-33dce85f-1d0d-424f-96a0-23ff5806186c.png" width="300">
	
	<img src="https://user-images.githubusercontent.com/68600731/147331055-e152e785-5d1c-428d-bdcb-b7dfeb1be4d5.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147331933-45a4af7a-9025-47c5-916b-f2680a678029.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147332765-a57b05d5-ab1c-4279-8f86-931e898afde3.png" width="300">

* `epoch` and `update`   
	<img src="https://user-images.githubusercontent.com/68600731/147332995-204c3fcd-8290-4290-8769-8fa41e77dec4.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147336063-2bacd795-eebd-45ef-a29e-918e64c9d109.png" width="300">

* `ReLU` ==> hard sigmoid   
	<img src="https://user-images.githubusercontent.com/68600731/147338129-04d4f935-6226-4e35-8538-399a0e8dfd0c.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147338281-8969c0be-c041-4020-986c-93c81e8fdb92.png" width="300">

* more and more and more layers  

	<img src="https://user-images.githubusercontent.com/68600731/147340145-20cebf0e-50ea-4139-aef5-9a79f6a83e75.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147340799-bdbf4b7a-18d4-46d5-8aa0-4ff9096aff38.png" width="300">

* deep learning is cooler than fat learning?

* why don't we go deeper ==> overfitting
<img src="https://user-images.githubusercontent.com/68600731/147341142-1e2b827e-9604-4c0b-ba91-35627304a200.png" width="300">

**In following experiments, `ReLU` is chosen as the `activation function` rather than `sigmoid`**

