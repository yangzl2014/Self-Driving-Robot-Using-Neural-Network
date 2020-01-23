# Self-Driving-Robot-Using-Neural-Network 
### Python + Tensorflow + OpenCV
### Overview
    1) The Robot uses neural network to learn and predict decisions just like human brains work.
    2) The model is built using Neural Networks . The model is trained by feeding in images of tracks which will be labeled (direction) and these data sets will be used to train the model. 
    3)After the model is trained it will be capable of taking its own decisions. The main prediction work will be done on laptop due to larger memory requirements and flexibility. Raspberry pi will be used to stream the video to laptop using Pi-camera. 
    4) First we will teach the model by labeling the output to the image and run all these data on the model. After learning, the model will learn to predict the direction of the robot by just looking at the video.
    5) Raspberry Pi will stream the live feed to the laptop and the predictions will be sent back to the raspberry pi to execute these decisions.
    6) The raspberry pi will be connected to motor driver which will control the wheels of the bot. Ultrasonic sensor makes sure that the robot does not collide with anything. Once trained it can run autonomously and make its decisions.It will try to maintain its path along the track and prevent from collisions. 

### For more detailed explanation, please view my IEEE paper titled <a href="https://ieeexplore.ieee.org/document/8533870" target="_blank">"Self Driving Robot using Neural Network"</a> or view <a href="https://drive.google.com/file/d/1H88Ns1iP7Ow5b2O4E5hxdy6M_rmgmLdV/view?usp=sharing">PDF</a> 
    
![alt text](https://github.com/akshay1997feb/Self-Driving-Robot-Using-Neural-Network/blob/master/pic1.png)
    
### A) Hardware Design
    The Hardware components used for this project are as follows:
    
    1) Raspberry pi-3.
    2. Pi Camera.
    3. Robot (Chassis, Wheels (4), Motors (2).
    4. Ultrasonic Sensor.
    5. Motor control (L293D).
    
    Raspberry pi will work as a brain of the robot, which takes all the decision of the robot and live streams video to
    the laptop. Ultrasonic sensor is used to calculate the distance of the obstacles ahead.
    

![alt text](https://github.com/akshay1997feb/Self-Driving-Robot-Using-Neural-Network/blob/master/pic2.png)

### B) Software Used:-
    1) Python(2.7)
    2) TensorFlow
    3) OpenCV

## Working
* Data Collection
    Images for training is collected by driving the robot.
    * Run File "" on Raspberry Pi and simultaneouly run File "" on your PC. A server client connection is established between Rpi and your computer. Ensure that they are on the same Network.
    * Pygame is used for driving the robot, it is driven by using Keyboard (w-forward, a-left, d-right). When a key is pressed the image with its label is saved.
    * NumPy is used to save the data and its corresponding label.
* Model Training
    * Tensorflow is used to create the model.
    * After sufficient data is collected, run file "" on your PC (Ensure all the paths in code is correct).
    * Training the model will take some time and post completion the model will be saved.
