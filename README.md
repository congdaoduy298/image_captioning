# image_captioning
IMAGE CAPTIONING WITH KERAS 

 This project includes: 
  + Data Collection : Flickr8k( containing training set, test set, dev set corresponding 6k, 1k, 1k images).

  + Clean Data : using some basic cleaning : lower-casing all the words ('Hello' -> 'hello), removing special tokens ('%', '$', etc.), eliminating words which contain numbers ('hey199').

   + I using InceptionV3 model with pre-trained weights on ImageNet not to classify the image but just get fixed- length informative vector for each image. This process is called automatic feature engineering. I encode all imagesand save them in the file "encoded_train_images.pkl" and "encoded_test_images.pkl".

   + Data processing - Captions: create two dictionary name char2int ( word to index ) and int2char ( index to word ).

   + Word Embedding : I use pre-trained GLOVE model to map the every word to a 200-long vector -> create embedding matrix.

   + Set up model : (Input1: Partial Caption -> LSTM), (Input2: Image Features), (Output: Dense layer with activation='softmax') ---> Train model. 

   + Test : generate captions on images from the test dataset.

# Reference : 
https://towardsdatascience.com/image-captioning-with-keras-teaching-computers-to-describe-pictures-c88a46a311b8
https://nttuan8.com/bai-15-ung-dung-them-mo-ta-cho-anh-image-captioning/
