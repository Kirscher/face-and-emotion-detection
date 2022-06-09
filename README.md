# Face & Emotion Detection in Python using Deep Learning

## CNN Model for Facial and Emotion Detection!
Structure of a basic CNN. Credit: Jie & Yongsheng.
![image](https://user-images.githubusercontent.com/85068746/172878268-46d8067f-225c-48b8-9f0e-3490fc4b9ad4.png)


## The face-recognition 1.3.0 library
https://pythonhosted.org/face_recognition

I used **face-recognition 1.3.0** open-source library to find faces in picture / camera input.

+ The trained model used in this library is a **ResNet network** with 29 convolutional layers. It is a version of the ResNet-34 network from the paper *Deep Residual Learning for Image Recognition* by He, Zhang, Ren, and Sun with a few layers removed and the number of filters per layer reduced by half.

![image](https://user-images.githubusercontent.com/85068746/172878620-715d9045-2776-4e35-9a0d-14114f4b703e.png)


+ The network was trained on a dataset of about **3 million faces** derived from a number of datasets (scrub dataset, the VGG dataset, …)

+ the **load_image_file()** method, loads the image file into a numpy array
+ the **face_locations()** method, retrieves a list of tuples containing face locations (top, right, bottom, left)

## The fer 22.4.0 library
https://pypi.org/project/fer

I used **fer 22.4.0** open-source library to predict emotions on faces.

+ The library is based on *OpenCV* and *TensorFlow*
+ FER bundles a *Keras* model. The model is a Convolutional Neural Network (CNN).

+ The detector returns a list of JSON objects.
+ the **detect_emotions()** method returns the emotions formatted into a JSON object with the keys '*anger*', '*disgust*', '*fear*', '*happy*', '*sad*', '*surprise*', and '*neutral*'.
+ the **top_emotion()** method returns the emotion with the higher score and its score


## Example
![image](https://user-images.githubusercontent.com/85068746/172881823-dbdf6784-0b84-4b70-b67f-641616987e38.png)
