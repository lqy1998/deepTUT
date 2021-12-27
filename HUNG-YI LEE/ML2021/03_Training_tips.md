# Training tips

## why failed
* zero gradient ==> critical point  

	<img src="https://user-images.githubusercontent.com/68600731/147410004-f0e53136-7cd6-40ed-90ea-4b1b7e07eb4c.png" width="300">

* which type critical point ==> how loss function looks like ==> taylor approximation  

	<img src="https://user-images.githubusercontent.com/68600731/147410469-1d12be34-0f3e-4c40-b464-a096df151355.png" width="300">	
	<img src="https://user-images.githubusercontent.com/68600731/147410519-d6820424-6aac-4d11-a44f-d856d12467f2.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147410605-be0fec03-7ea8-47e0-a22a-dec4b1c3cc25.png" width="300">

* eg. one training data, two parameters  

	<img src="https://user-images.githubusercontent.com/68600731/147428853-efa5e0e8-36b1-4641-8b4b-070439b36da7.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147429408-c3790663-3425-4837-9c42-13007773fa35.png" width="300">

* if it's a saddle point ==> give up `g`, turn to `H` ==> huge work, seldom calculated in practice

	<img src="https://user-images.githubusercontent.com/68600731/147429758-9592b67d-843c-43d2-b808-fcbc1b3edeff.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147430907-5f3d0c8f-b989-4420-a200-e747b0d3b837.png" width="300">

* local minimum is rare when you have lots of parameters ==> it'a saddle point in higher dimension

	<img src="https://user-images.githubusercontent.com/68600731/147431462-0434f5a6-8b09-44eb-9a8a-14d81dd03036.png" width="300">


## batch
* shuffle after each epoch

	<img src="https://user-images.githubusercontent.com/68600731/147445287-a17e3337-55df-444c-8f04-79bea5bd8886.png" width="300">

* small batch v.s. large batch   

	<img src="https://user-images.githubusercontent.com/68600731/147448710-1bb2ed1b-6bd7-463f-a6ba-03076bc6d351.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147448985-af18c002-06c1-41df-b683-267a8c235a17.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147451254-acb57b54-d264-41be-b079-31ea2e853525.png" width="300">

* considering parallel computation, large batch isn't worse than small batch   

	<img src="https://user-images.githubusercontent.com/68600731/147449479-2b3fce25-cfd4-42a9-bc60-418b90ccfcf7.png" width="300">
	
* but `noisy` sometime is a good stuff    

	<img src="https://user-images.githubusercontent.com/68600731/147450900-780df913-0015-40d7-88ea-f145173abb1a.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147450571-d11e22f9-e586-48ec-b156-1e960a2e1873.png" width="300">
	
* small batch is better on testing data
	* good minimum ==> flat 
	* bad minimum ==> sharp 
	<img src="https://user-images.githubusercontent.com/68600731/147452494-25dd0009-9826-40eb-8c92-5542996a92ae.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147452607-63ac2f19-c9c2-4d9b-b316-c0e91ae3e499.png" width="300">

## momentum




## learning rate






## loss function







## batch normalization

















