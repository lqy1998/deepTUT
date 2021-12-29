# CNN

## Basic structure
* First, rescale images to the same size    
  
    <img src='https://user-images.githubusercontent.com/68600731/147622663-f91bbcd7-c7b0-4f67-98b4-688968131dda.png' width='300'>

* a RGB image = 3d `Tensor`    
  
    <img src='https://user-images.githubusercontent.com/68600731/147622749-af6173a1-0dd5-4a57-a68e-afe84d43ce2c.png' width='300'>

* if we straighten the image to a vector ==> overfitting  
  
    <img src='https://user-images.githubusercontent.com/68600731/147622844-1438355d-63ce-472b-894f-1eb66e9aa947.png' width='300'>

## Normal settings
* Identifying some critical patterns ==> various `receptive fields` 

    <img src='https://user-images.githubusercontent.com/68600731/147623752-f63a109d-26b1-48cf-b27e-d40c6b332388.png' width='300'>
    <img src='https://user-images.githubusercontent.com/68600731/147637637-0bcd5b0a-3144-4038-b003-90df84fca799.png' width='300'>
    <img src='https://user-images.githubusercontent.com/68600731/147637759-74f4a99d-1957-436e-bcdf-cb0b5c95a927.png' width='300'>

* Typical setting of receptive field 
	1. all channels
	2. kernal size = 3*3
	3. stride = 1 or 2
	4. each receptive field has a set of neurons
	5. padding 0 or average or edge, whatever   
	
	<img src='https://user-images.githubusercontent.com/68600731/147640103-6de74e19-e0f3-41e4-bf3f-f7d1282f6cc1.png' width='300'>

* One pattern could exist in different positions ==> neurons of different fields sharing parameters         

	<img src='https://user-images.githubusercontent.com/68600731/147640957-022f5045-7b8d-4af8-9c6b-74f5fd6af7b4.png' width='300'>
	<img src='https://user-images.githubusercontent.com/68600731/147640729-b807ba4f-7648-4fad-8bac-2c3e4894b829.png' width='300'>

* Typical setting of parameters sharing 

	<img src='https://user-images.githubusercontent.com/68600731/147641609-201d5afa-fc6d-4331-9216-100723ebc16b.png' width='300'>

## Benefit of Convolutional Layer
<img src='https://user-images.githubusercontent.com/68600731/147642052-178f81f1-31b5-4031-be84-c5244d3ad367.png' width='300'>

## Another edition of CNN


















