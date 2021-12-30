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


## eg. Each vector has a label ==> `Sequence Labeling`

* fully-connected networks don't work because of the unsure-length sequence

   <img src="https://user-images.githubusercontent.com/68600731/147729990-9825fbab-3c7f-4d43-99aa-20bedd8f80e8.png" width="300">

* we can alternate FC and SA

   <img src="https://user-images.githubusercontent.com/68600731/147730168-c1bd7696-9d99-4c37-8986-446fb49ca45d.png" width="300">






## 




























