# TEXT-TO-IMAGE GENERATION USING DEEP CONVOLUTIONAL GENERATIVE ADVERSARIAL NETWORK

## PRE-PROCESSED AND PREPARED DATA:
The  data is prepared, pre-processed and stored into ./text-to-image directory as .npy files.
1.	train_captions.npy
2.	train_images.npy

## Dependencies:
* python 3.5
* TensorFlow 1.1
* [Optional] Torch is needed, if using the pre-trained char-CNN-RNN text encoder.
* The word to image caption and caption to the word mapping are done and stored into ./dictionary directory as:
     * id2Word.npy
     * word2ID.npy
     * vocab.npy
     
## ARCHITECTURE:

![DCGAN - ARCHITECTURE](https://github.com/arunvignesh28/Text-to-Image-Generation-using-GAN/blob/master/Text%20to%20Image%20Conversion%20using%20DC-GAN/Text-to-Image%20GAN/Pictures%20Report/Gen.JPG)
![DCGAN - ARCHITECTURE](https://github.com/arunvignesh28/Text-to-Image-Generation-using-GAN/blob/master/Text%20to%20Image%20Conversion%20using%20DC-GAN/Text-to-Image%20GAN/Pictures%20Report/Discriminator.JPG)

## EXECUTION:
* Run ./Text-to-Image-GAN/train.py to train the DCGAN model on the Oxford 102-Flowers dataset using the pre-trained Word-ID embedding Numpy array model.
* The results will be stored to ./Text-to-Image-GAN/train_samples/.
* If you want to try your own datasets, we encourage to try different hyper-parameters and architectures, especially for more complex datasets like MS-COCO datasets.
* Inorder to improve the performance of the DCGAN, you can also use other techniques as follows:
    * Normalize the inputs
    * A modified loss function
    * Batch normalization
    * Avoid sparse gradients: ReLU, MaxPool

## SAMPLE INPUT SENTENCES:
* The flower shown has yellow anther red pistil and bright red petals.
* This flower has petals that are yellow, white and purple and has dark lines
* The petals on this flower are white with a yellow center
* This flower has a lot of small round pink petals.
* This flower is orange in color, and has petals that are ruffled and rounded.
* The flower has yellow petals and the center of it is brown
* This flower has petals that are blue and white.
* These white flowers have petals that start off white in color and end in a white towards the tips.

## RESULT:
     AFTER 600 EPOCH, (We assume better results can be achieved by playing with the hyper-parameters)
     
![Image - Epoch 600](https://github.com/arunvignesh28/FYP/blob/master/Text%20to%20Image%20Conversion%20using%20DC-GAN/Text-to-Image%20GAN/output/train_599.png)     
 


