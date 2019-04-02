This is an image classification project. First the program tests if a given image is that of a dog's or a human's. If it is a dog's picture,
the classifier detects the breed of the dog. If the image is that of a human's, the classifier states the breed of the dog that would have 
matched it. had the human been a dog. 

We use ImageNet class of 1000 classes to define our outputs. 
In the [dictionary](https://gist.github.com/yrevar/942d3a0ac09ec9e5eb3a), the categories corresponding to dogs appear in an uninterrupted 
sequence and correspond to dictionary keys 151-268, inclusive, to include all categories from 'Chihuahua' to 'Mexican hairless'. Thus, 
during training, we restrict ourselves to these 118 classes. 

In order to detect dog breed, we implement two ways, the first is by scratch - we create and deply a CNN by defining all the layers and initial
weights from scratch. The second way is to use a pretrained model that has already been trained on the ImageNet data and then to further finetune
it to our special case. In this case, we use a pretrained VGG16 model.
