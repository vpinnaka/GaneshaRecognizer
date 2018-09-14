# GaneshaRecognizer

Lord Ganesha is worshipped in many parts of the world as God of intellect and wisdom and also known as the patron of arts and sciences. Sep 13 is Ganesh chaturdi, a festival celebrated as the birth of Ganesha. On this auspicious day, I want to offer my gratitude to Lord Ganesha by building a simple deep learning model that recognizes Ganesha images. I prototyped this model very fast but I am able to achieve an accuracy score of around 80%. I have used Convolution neural networks for achieving this image classification task. The improvements that can be made for better accuracy, are trying different optimizers, increasing more layers and changing the stride and learning rate.

I have used googleimagesdownload package for obtaining the data, used two classes for training 'ganesh'(most of the images that belong to this class are Lord Ganesh portraits in sitting posture) and 'notganesh'(used person images, also some other Hindu god images). I have augmented the images since the data size is small. I have used 'Adem' as an optimizer for model. The architecture of the CNN model is pretty simple(at least I am thinking).

**Tricking the model**:

Lord Ganesh has a very peculiar feature, he has an elephant head(resembling the big brain, great intelligence), so it is not surprising for me that model learned that feature pretty well. I have purposefully not given elephant images in 'notganesh' class, I am in an assumption that model will fail for Elephant images, to my surprise, it did pretty good, you can see it in the results section(but the first image in tricky). The model failed for all 'laughing budda' images(technically speaking laughing buddha is known as Chinese Ganesha I don't know how my model knows this), the reason that I can think of is, most of the images under 'ganesh' label have sitting postures of Ganesha, so the model might have confused with the same sitting posture of 'laughing budda'. One other image that model got confused with is with the black and white image in third row second one. I am assuming that the trunk of the head is curly, so it has mistaken it as not Ganesha. Overall it is a good learning experience for me and I am very satisfied that I have offered prayers to Lord Ganesha in this manner.

I would like to know your valuable feedback and suggestion, you can connect me on:

* [LinkedIn](https://www.linkedin.com/in/vinaydatta2020/)
* [Twitter](https://twitter.com/vinay4B7)

## How to recreate this work?
* Please clone the repo to your local and run the jupyter notebook in 'conda' environment
* To download the dataset, uncomment the first section of jupyer notebook and run the cell

## Environment
* I would highly suggest Linux encironment with 'anaconda' installed, but it is doable in windows
* I have used 'aws p2.xlarge' instance with nvidia tesla GPU for training, but it is managable with out GPU as well
