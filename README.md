# Live-camera-image-classifier
You can use common objects or face/body gestures to capture images for each of the three classes. Each time you click one of the "Add" buttons, one image is added to that class as a training example. While you do this, the model continues to make predictions on webcam images coming in and shows the results in real-time.
We will make a custom 3-class object classifier using the webcam on the fly. We're going to make a classification through MobileNet, but this time we will take an internal representation (activation) of the model for a particular webcam image and use that for classification.

We'll use a module called a "K-Nearest Neighbors Classifier", which effectively lets us put webcam images (actually, their MobileNet activations) into different categories (or "classes"), and when the user asks to make a prediction we simply choose the class that has the most similar activation to the one we are making a prediction for.
