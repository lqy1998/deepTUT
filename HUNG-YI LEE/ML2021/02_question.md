# Question
<img src="https://user-images.githubusercontent.com/68600731/147384985-f9ea4b03-3fcc-4ebb-8ef5-a30969dbec7e.png" width="300">

## Model Bias vs Optimization
<img src="https://user-images.githubusercontent.com/68600731/147384583-9c92795a-1616-4d1e-8352-b60777afa07d.png" width="300">  <img src="https://user-images.githubusercontent.com/68600731/147384788-d2010417-4d64-45c4-814e-59f5b1a3f1ba.png" width="300"> 

<img src="https://user-images.githubusercontent.com/68600731/147384918-4b297d87-fca0-4e7d-ad52-95b70d212dfe.png" width="300">  <img src="https://user-images.githubusercontent.com/68600731/147384960-2910a4bc-fc07-41ae-ac94-18dca17ca340.png" width="300">	

## Overfitting
* we found a loser function, an extreme eg.  
<img src="https://user-images.githubusercontent.com/68600731/147385075-1030c100-c9f7-45c1-a88f-b12de7cdc009.png" width="300">	

* what is overfitting  
<img src="https://user-images.githubusercontent.com/68600731/147385127-24865676-e30f-4d64-b831-c30915666ee7.png" width="300">	
 
* how to solve overfitting  
1. find more data
<img src="https://user-images.githubusercontent.com/68600731/147385364-3c505a3a-468f-4904-baa4-9c00cdd929d4.png" width="300">	

2. data augmentation
* but should be reasonable, you can flip the cat picture horizontally, or enlarge it, but it doesn't make sense to turn it upside down. There is no cat like that!  
<img src="https://user-images.githubusercontent.com/68600731/147385374-9ad28dcd-c2ef-4dd8-81d2-eec6b1f2119d.png" width="300">	

3. constrained model
* thus less flexibility  
<img src="https://user-images.githubusercontent.com/68600731/147385410-73f110d6-5968-49c6-a871-bd1629b24f28.png" width="300">

* but not too much ==> back to model bias  
<img src="https://user-images.githubusercontent.com/68600731/147385800-8161e317-9b38-4348-9114-9e024c4dd62e.png" width="300">

* Bias-Complexity Trade-off
<img src="https://user-images.githubusercontent.com/68600731/147385894-1f5217f7-22ea-4780-8525-2b28a7f4f4c8.png" width="300">

* constraining approaches 
	* less parameters
	* sharing parameters
	* Early stopping
	* Regularization
	* Dropout

## choose the right model

<img src="https://user-images.githubusercontent.com/68600731/147386203-be39d02e-b526-4eef-8bb1-7fa472fe3522.png" width="300">  <img src="https://user-images.githubusercontent.com/68600731/147386208-47414d73-1d01-4385-be94-2b6c91900333.png" width="300">

This explains why machine usually beats human on benchmark corpora.

* cross-validation  
<img src="https://user-images.githubusercontent.com/68600731/147386353-34c9a8f7-c996-4ece-83e6-c9af0ab40fd3.png" width="300">  
<img src="https://user-images.githubusercontent.com/68600731/147386479-52108fe8-f5b0-43e4-bb64-03d04106a217.png" width="300">

## mismatch(kinda overfitting)
<img src="https://user-images.githubusercontent.com/68600731/147386666-e248b70d-c5fc-4e6e-9786-ffe181fe0426.png" width="300">
