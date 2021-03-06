# Transformer

## `Seq2Seq`

* examples
   
    <img width="300" src="https://user-images.githubusercontent.com/68600731/147801367-c2a6a522-e189-46a6-9531-33a5cacaa628.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147809817-68c46e94-e3ac-453b-831e-7576fb10047b.png">  
    <img width="300" src="https://user-images.githubusercontent.com/68600731/147808683-64b54973-6b8c-49be-9f7d-4988fb07a466.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147809799-76b0f2c5-f8f1-4114-bb7f-71cadff0822c.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147809822-71e72fca-bc95-487b-b982-85b5120a9eef.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147810881-6650ea89-4669-455c-90c9-a4ae9a276f9d.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147811481-ca198b44-a5f3-47e7-8683-37743cb4f0a3.png">

    <img width="300" src="https://user-images.githubusercontent.com/68600731/147811498-3b372c84-9468-4d28-a7bc-833a8863ed89.png">

* `Question Answering (QA)`
    
	<img width="600" src="https://user-images.githubusercontent.com/68600731/147810235-236a3378-a8b8-41b2-8581-f7819ac3c64c.png">

## Seq2Seq Basic Structure

<img width="300" src="https://user-images.githubusercontent.com/68600731/147813162-8c852a2d-7482-430c-baf5-370671180862.png">

* Encoder
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147814165-970ab4fc-aa10-491b-b10e-ffb182a60b8c.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147814176-e9942b39-0068-4270-864a-d5b8ec034bd0.png">
	<img width="300" alt="image" src="https://user-images.githubusercontent.com/68600731/147814484-f43bc6e2-b81c-4225-a887-07ae7018f31b.png">

* Decoder ==> eg. `Autoregression`(AT)

	* Begin token     
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147852788-77dfa05c-be27-408e-8da4-3537c778390a.png">
	
	* can use letter/word/subword/汉字     	
	
	* may cause `Error Propagation`
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147852879-9a341754-64cc-4522-9231-2306955ff847.png">

	* Masked-Self-attention         	
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/147852934-0fcbdedb-3711-409d-9d5f-08ea26533c5c.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148148800-b0a20116-8f32-4d51-9562-ae5a7f9370c2.png">

	* Stop token     
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148149285-fc80ed97-f442-43b6-b329-b6b44d9a66f1.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148150337-2acd06d4-38e7-4240-a247-3df4eea31259.png">

* Decoder ==> eg. `Non-autoregression`(NAT) ==> not popular till self-attention

	* AT v.s. NAT   
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148153636-6b2b9139-3479-48fe-8136-9c28c74cd023.png">
	
	* speaking speed controller ==> predict a shorter output length ==> speak faster

* `Transformer` ==> `Cross attention` = bridge between encoder and decoder    
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148154151-526bb184-32cb-44ae-87e3-3fc3997d4e04.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148154787-eacc36d6-05ce-4da9-8e0d-3b44d2f9e42f.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148154865-6dfdc713-121f-4598-98c3-6f4f209990bc.png">
	
	* eg.  
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148155610-1ebbae2f-ab7a-489d-94cc-dd09d1f8950a.png">
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148155962-aa9be128-59c9-43b2-8b41-075c7b5fecba.png">

* Training  
	
	<img width="300" src="https://user-images.githubusercontent.com/68600731/148172725-fe83f4c6-4a3f-49c8-8044-b6d9b1d60b4d.png">

	* `Teacher Forcing` ==> but during inference(testing) no ground truth could be inputed ==>  `Mismatch`!!!      
		* `Exposure bias` ==> `Scheduled Sampling`  
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148173866-c38c1706-b14a-4062-a08e-bcd4ca8bdf7d.png"> <img width="300" src="https://user-images.githubusercontent.com/68600731/148179135-d9d502ea-62b0-431f-928e-32def48f19e1.png"> <img width="300" src="https://user-images.githubusercontent.com/68600731/148179161-8859ff21-cc07-451a-b645-3de0bff7d77c.png">


	* Tips	
		* no need to create new ==> `Copy Mechanism`
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148175296-33994498-e464-40b4-ab43-c2b6d4957e35.png">
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148175268-2ed03836-10bc-4c55-9e38-e44ba25b6ab4.png">

		* learn strange features ==> `Guided Attention`   
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148176351-31a6cd8d-f6fc-4b62-9913-2f10a895090e.png">

		* happy ending without happy beginning ==> `Beam Search`
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148177486-d96a249a-81ab-41eb-9e2c-7d3badb097d2.png">

		* random noise   
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148178146-05ffc111-13e9-4dd4-a1ab-92c6b4a5b2bc.png">

		* Optimization ( to be learnt)
		
		<img width="300" src="https://user-images.githubusercontent.com/68600731/148178715-641b72de-44a4-4e46-86dd-c85fd3c89700.png">







