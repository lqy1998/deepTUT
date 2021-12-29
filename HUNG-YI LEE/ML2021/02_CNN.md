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

## `Convolution`

* `Feature Map`   

    <img src='https://user-images.githubusercontent.com/68600731/147642841-b0ce831f-212f-47ce-abdc-e7acc79bec1a.png' width='300'>
    <img src='https://user-images.githubusercontent.com/68600731/147642863-431a1041-2903-4c36-a636-6b9e8e84890b.png' width='300'>
    <img src='https://user-images.githubusercontent.com/68600731/147642967-3be519c2-cb42-435c-9759-98e5f1c1bd42.png' width='300'>

* multiple convolutional layers

    <img src='https://user-images.githubusercontent.com/68600731/147643238-8258e932-0b4f-43e7-8929-e8dd7e1351ee.png' width='300'>

* deeper network ==> larger pattern

    <img src='https://user-images.githubusercontent.com/68600731/147643378-d46aa79a-5438-471f-a967-57b0afd6a9cc.png' width='300'>

* filter = parameters (we ignore bias)
    
	<img src='https://user-images.githubusercontent.com/68600731/147643657-c91375d6-4e9f-4acc-9a02-cca90ad3d08c.png' width='300'>
    <img src='https://user-images.githubusercontent.com/68600731/147643699-34126d72-ae74-4ec7-966f-7faa59df208a.png' width='300'>

## `Pooling`

* Max Pooling (Min/Mean...) ==> an operator like an activation function
	1. Max/Min/Mean...
	2. size can be whatever you like
	<img src='https://user-images.githubusercontent.com/68600731/147643952-aa24635a-9a1d-42d8-ac92-2f770f6da905.png' width='300'>
	<img src='https://user-images.githubusercontent.com/68600731/147644934-cced9761-e712-47f2-8d73-0fc9e2cea44c.png' width='300'>
	<img src='https://user-images.githubusercontent.com/68600731/147644957-ea3872a4-35e9-45d6-a56e-4fc03b495a0d.png' width='300'>

* convolution and pooling (ababab or aabaabaab or whatever)
	
	<img src='https://user-images.githubusercontent.com/68600731/147645177-dbf90010-0960-4a45-a25f-bd4172eb9fba.png' width='300'>

btw, just drop pooling layers if computation capacity is enough.

## The whole CNN

<img src='https://user-images.githubusercontent.com/68600731/147645482-636d3193-9848-4f68-b12d-68f61ed6d4a0.png' width='300'>

* eg. AlphaGo
	
	<img src='https://user-images.githubusercontent.com/68600731/147645911-587fb883-a4d9-456b-b848-973193225b50.png' width='300'>
	<img src='https://user-images.githubusercontent.com/68600731/147646002-59255eb6-9081-4013-a7f4-9ba07cf016c4.png' width='300'>
	<img src='https://user-images.githubusercontent.com/68600731/147646548-b3faba57-8597-4d8f-89f3-febd1760d2ba.png' width='300'>

* cannot deal with scaling and rotation ==> Spatial Transformer Layer
	
	<img src='https://user-images.githubusercontent.com/68600731/147646631-6564675f-c032-44dd-a275-1aa2c8aff53f.png' width='300'>





