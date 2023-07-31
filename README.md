# EyeStatusRecognition-DeepLearning

**Eye Status Detection using DeepLearning**

This project focuses on developing a deep learning-based solution to detect the status of eyes, distinguishing between open and closed states. Using the powerful InceptionV3 pre-trained model from Keras and employing transfer learning, i aim to achieve high accuracy with minimal data requirements. 


This project stands out because i created a special dataset using my own eye images. 100 images of closed eyes and 100 images of opened eyes. By using my personal eye images the model gains a better understanding of different conditions it might encounter. you can find the images in the PrepareData.rar file

![Eyes](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/91762815-c879-48af-a9fb-68929443eb44)

**About Dataset** All images are grayscale images, To ensure uniformity and ease of processing, all the images have been resized to the same dimensions of 110x110 pixels. All images are .png. The grayscale format simplifies data representation, making it easier for the model to detect eye status based on shades of gray.

**Splitting the dataset** The data has been divided into 80% and 20% train and test ratio in the main directory itself. using the rest 0.2 as the validation data

**InceptionV3 Pretrained Model** load the InceptionV3 model pre-trained on the ImageNet dataset, but the last classification layer (1000 classes) is excluded. The model will retain its powerful feature extraction capabilities without being restricted to the original 1000 classes.

Additional layers are added, including a dense layer with 64 neurons, a dropout layer for regularization, and a final output layer with 2 neurons representing the open and closed eye classes
