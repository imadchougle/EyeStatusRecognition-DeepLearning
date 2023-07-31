# EyeStatusRecognition-DeepLearning

**Eye Status Detection using DeepLearning**

This project focuses on developing a deep learning-based solution to detect the status of eyes, distinguishing between open and closed states. Using the powerful InceptionV3 pre-trained model from Keras and employing transfer learning, i aim to achieve high accuracy with minimal data requirements. 


This project stands out because i created a special dataset using my own eye images. 100 images of closed eyes and 100 images of opened eyes. By using my personal eye images the model gains a better understanding of different conditions it might encounter. you can find the images in the PrepareData.rar file

![Eyes](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/91762815-c879-48af-a9fb-68929443eb44)

**About Dataset** All images are grayscale images, To ensure uniformity and ease of processing, all the images have been resized to the same dimensions of 110x110 pixels. All images are .png. The grayscale format simplifies data representation, making it easier for the model to detect eye status based on shades of gray. The Dataset has been already divided into 80-20 ratio, i test and train sub-folders

**Splitting the dataset** The data has been divided into 80% and 20% train and test ratio in the main directory itself. using the rest 0.2 as the validation data

**InceptionV3 Pretrained Model** load the InceptionV3 model pre-trained on the ImageNet dataset, but the last classification layer (1000 classes) is excluded. The model will retain its powerful feature extraction capabilities without being restricted to the original 1000 classes.

Additional layers are added, including a dense layer with 64 neurons, a dropout layer for regularization, and a final output layer with 2 neurons representing the open and closed eye classes

**Haar cascades** are utilized as a preliminary step to efficiently extract eye regions from images

**Model Performance and Visualization**: Model got 100% on the 13th epoch with the learning rate of 0.001 thus the Best Accuracy is saved in the model. The localized eye regions serve as focused inputs to our deep learning model.

![modelaccuracy](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/5a4b011f-89bc-4f2e-9221-c8155879c06f)

Training Loss also reduced significant

![loss](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/77a186e7-01ab-47cb-b945-bba3c0353b13)

**Predicting the New (unseen image) Data**

![BeFunky-collage (1)](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/b091a5f5-4b1b-4e3c-95c8-8d512da01661)


![BeFunky-collage](https://github.com/imadchougle/EyeStatusRecognition-DeepLearning/assets/54437743/3e358ee2-e9ab-4e87-a89c-0d9dd06196cd)

***Amazing!! The model is performing well, accurately predicting the eye status with high probability scores. By combining a custom dataset and transfer learning with InceptionV3, i achieved robust feature extraction. The integration of Haar cascades and deep learning making the model suitable for real-time applications.***

By using this approach you can create your own custom dataset and develop eye status detection models tailored to your specific requirements. 

With Haar cascades you can  extract eye regions from facial images ensuring relevant inputs for your deep learning model. 

By pre-trained models like InceptionV3 with your dataset you gain powerful feature extraction capabilities and achieve accurate eye status predictions


