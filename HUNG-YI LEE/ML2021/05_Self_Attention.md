# Self Attention

## Basic structure

* **Input: the number and length of vectors are both unsure**   
	  
   <img src="https://user-images.githubusercontent.com/68600731/147716953-011c0fc9-6e0e-4e95-809d-4de3aa4d93e8.png" width="300">

* **eg1. sentence**     
We create one-hot vectors, whose lengths are as big as the num of all words exist in world.  
But there is a question: we can't tell the relationship among words, such as, cat and dog are both animals.  
We turn to `Word Embedding`.  

   <img src="https://user-images.githubusercontent.com/68600731/147717627-9aa5c60c-813e-4284-aec9-1b78930dbcea.png" width="300">

* **eg2. speech**
 
   <img src="https://user-images.githubusercontent.com/68600731/147717603-a7938c4a-852c-44df-a2d1-766d91cfc8b6.png" width="300">

* **eg3. graph**

   <img src="https://user-images.githubusercontent.com/68600731/147718009-c35ec1e7-c989-4552-9565-aef661b043d5.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147718058-5e56fafb-4895-4ccc-8487-7a3af31ed332.png" width="300">

* **Output**
   
   <img src="https://user-images.githubusercontent.com/68600731/147718931-1490ca37-b053-4b2b-a9c9-5367385be957.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147719045-74e7be3f-e319-4da5-9e56-635d8351ce73.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147719062-bd5fd9a1-dd94-4511-9b5b-be77a9c4c4a9.png" width="300">

seq2seq: translation, speech recognition


## Each vector has a label ==> `Sequence Labeling`

* fully-connected networks don't work because of the unsure-length sequence

   <img src="https://user-images.githubusercontent.com/68600731/147729990-9825fbab-3c7f-4d43-99aa-20bedd8f80e8.png" width="300">

* we can alternate FC and SA

   <img src="https://user-images.githubusercontent.com/68600731/147730168-c1bd7696-9d99-4c37-8986-446fb49ca45d.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147739157-598049dd-3a23-4077-89ad-eb705326b753.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147739289-642ce947-9aa1-45db-b492-42803ddea334.png" width="300">

* how to calculate attention score      
   1. can add attention score with self
   2. can change activation function(or kinda normalization), like ReLU
  
   <img src="https://user-images.githubusercontent.com/68600731/147739257-a58f18e1-ed1f-4734-b724-34704fade487.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147739028-9f414d9e-dab8-459a-96e7-c05b7909d020.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147739652-4f5f141f-f3e6-4052-96e3-e9cfbfd4212f.png" width="300">

* if an `α` is large, after weighted sum, the relevant `v` will dominant b
  
   <img src="https://user-images.githubusercontent.com/68600731/147739849-9c21478f-35bb-45c7-944a-fa6f3ff0181d.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147758365-dc5a610d-026f-4f7b-9fb4-33435de4e68d.png" width="300">

* from point of matrix computation 

   <img src="https://user-images.githubusercontent.com/68600731/147758588-1774913a-a59e-40fa-8e4d-2f2c81cf3160.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147758902-e18c89b2-3cd8-4d21-aee5-da11e0e875d8.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147759195-39689aa6-974a-45c3-a6cb-af5f070ded59.png" width="300">

## Special structure

* `Multi-head Self-attention` ==> different types of relevance

   <img src="https://user-images.githubusercontent.com/68600731/147760798-8b5fadef-f94f-4952-9ed7-2980beadabe4.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147760822-a62bb58d-e817-4861-be48-743d4e0c7793.png" width="300">
   <img src="https://user-images.githubusercontent.com/68600731/147760856-cba60c34-1907-49ea-ba73-11c0b1bcdbc0.png" width="300">

* Positional Encoding (a bunch of methods)
	* why? ==> such as, verbs unlikely show up at the beginning
   <img src="https://user-images.githubusercontent.com/68600731/147798600-6dc30840-dfd1-4b08-bd7d-9a96274190ab.png" width="300">

## Application and Comparison

* application
    
	<img src="https://user-images.githubusercontent.com/68600731/147799013-c3bbc28f-0e9a-4251-92ee-dcf40d2a8f90.png" width="300">
    <img width="300" src="https://user-images.githubusercontent.com/68600731/147799160-66dec9c9-1f53-424f-b708-ffb1ece385eb.png">
    <img width="300" src="https://user-images.githubusercontent.com/68600731/147800414-0a879adf-4c3a-4c35-86e0-f7e7f59e1bc3.png">


* SA v.s. CNN 
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147799433-f30744b0-9fbf-41e6-b190-c2f4dde723e4.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147799656-a825e174-5090-40fd-99e0-f843ca2136b8.png">

* SA v.s. RNN

	<img width="300" src="https://user-images.githubusercontent.com/68600731/147799896-96cf86a1-7a9f-4884-92ce-d47763ebaceb.png">
















