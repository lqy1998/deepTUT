# Training tips

## 3.1 critical point
### 3.1.1 why stuck ==> small gradient ==> critical point    
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


### 3.1.1 how to escape ==> batch
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

### 3.1.2 how to escape ==> momentum
* `Vanilla Gradient Descent`

	<img src="https://user-images.githubusercontent.com/68600731/147454578-b02514e0-8384-4387-a405-739a5704ddb7.png" width="300">

* `Momentum`

	<img src="https://user-images.githubusercontent.com/68600731/147454648-db59fc1e-35a3-45df-9b07-dc34b64ec570.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147454702-c9c7b86f-e2e7-4750-bf9f-40491e01b131.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147454727-a990de86-ce22-44a4-a1ce-3d2dc50fbab7.png" width="300">

## 3.2 learning rate
* loss doesn't get no lower, gradients still concuss but not be small

	<img src="https://user-images.githubusercontent.com/68600731/147457629-a6df79bf-f526-4cf4-8227-077a621a9b41.png" width="300">
	
* though critical point is rare, training is still difficult

	<img src="https://user-images.githubusercontent.com/68600731/147457693-bacbe16e-d000-40d3-b2f2-64c518cec73f.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147458045-0deefbda-6830-4102-82ed-4402b4be864b.png" width="300">

* different parameters, different learning rates
1. Root Mean Square ==> Adagrad

	<img src="https://user-images.githubusercontent.com/68600731/147539095-9a5f6596-a4fb-4579-903f-7c030d87ca1c.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147539129-eff6f4be-585f-41b3-8730-f176ae32d3e0.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147539571-157107eb-9796-4715-9657-8d42139139d9.png" width="300">

gradient needs to change more violently and sensitively:point_down:

2. RMSProp ==> Adam = RMSProp + Momentum ==> RAdam(explain warm up)

	<img src="https://user-images.githubusercontent.com/68600731/147539881-d3c3871d-fd4d-4be8-85d1-8d0d6570c604.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147539978-bb1ecf6a-2ccd-403c-a1c9-2346c640ae34.png" width="300">
	
3. learning rate scheduling

If we only use Adagrad, after a cumulation of small gradients, it cycles between explosion and convergence.      
	<img src="https://user-images.githubusercontent.com/68600731/147540059-392586ba-7606-43dc-a666-41a6a6153957.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147540355-cd2ea1e9-ae83-4aa0-b1a4-e13f25b9701b.png" width="300">

At beginning, model has only seen a small part of data, which is not representative. Thus, we use warm up to set a small lr value       <img src="https://user-images.githubusercontent.com/68600731/147540386-375ab130-e482-47bd-9e66-a3646134ddd0.png" width="300">

### Gradient Descent Tips ==> Momentum + learning rate  
<img src="https://user-images.githubusercontent.com/68600731/147540409-92abf71b-182c-4329-92b1-ea1f8900752f.png" width="300">


## loss function
* classification

	<img src="https://user-images.githubusercontent.com/68600731/147542259-36646857-d315-4f0c-bf3b-f4820f0d194c.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147542395-26dc05b1-4dce-423f-9f0f-27170dde16a8.png" width="300">
	<img src="https://user-images.githubusercontent.com/68600731/147542918-3a536ed3-0f68-4319-aa40-7415792a6d03.png" width="300">

* `soft-max`(three or more classes) = sigmoid(two classes)
	* normalization
	* make differences more obvious

	<img src="https://user-images.githubusercontent.com/68600731/147543358-6149e34e-a331-46ab-96e7-895f8899f1b1.png" width="300">

* Loss of Classification

	<img src="https://user-images.githubusercontent.com/68600731/147543602-4d4a6045-c678-4b89-b3e3-3e310ffb0a1a.png" width="300">

In pytorch, soft-max is bound to cross-entropy and is built automatically.

* why `cross-entropy` is better in classification

	<img src="https://user-images.githubusercontent.com/68600731/147544118-083d34f0-ff0b-4aa6-ab64-58111300dcf6.png" width="300">

## batch normalization

















