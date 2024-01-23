# WALL-F
The integration of Computer Vision and Robotics. Our robot, powered OpenCV Python, identifies and navigates with precision. Join us in reshaping the future at the UTRA hackathon!
Inspiration
Inspired by NASA's Mars Sample Return Project, our team crafted a robot in 26-hours. This innovative creation combines advanced computer vision firmware with robotic precision to autonomously identify and pick up targeted objects. Reflecting the synergy between space exploration and technological innovation, our project highlights the infinite possibilities of robotics and computer vision.

##What it does
Our robot features a sophisticated suite of capabilities powered by OpenCV, an open source Computer Vision recognition software. The robot adeptly identifies objects by dimensions, delivering precise centre coordinates for optimal control. The intricate network of communication includes seamless data transmission between the robot's camera and two separate computing systems. The first computer processes raw information from the camera, while the second translates this data into precise movement controls for the robot. This seamless integration ensures a swift and accurate response to the environment. Notably, our robot robot has endless possibilities. By giving the computer vision software different parameters, it can sort objects based on those parameters.

##How we built it
Computer Vision: The program consists of two parts tracking and object classification. We increase the image contrast by functions such as cvtColor(frame, cv2.COLOR_BGR2GRAY) which changes the input to monochrome, GaussianBlur(),.Canny(), dilate(), and erode() to acquire the edge of our targeting project, which further increases the accuracy of our detection. To classify our targets in the image and video inputs, we customize our parameters to differentiate our target with an area above 100x100 from the small objects that we see as rocks.

We return all our detecting objects as a dictionary with object names as keys and its x, and y positions as values through wireless internet transmission through Pyro5.

##Challenges we ran into
Our initial plan was to use an ESP32 camera and Raspberry Pi. Use R0S2 as the communication middleware. Run micro-ROS on ESP32-cam to send image to the Raspberry Pi that controls the rover. We first realized that Raspberry Pi 2 was clearly not powerful enough to run the Computer Vision algorithm designed for object detection. So, to demonstrate the concept, we opted to use a webcam and alaptop to run the CV algorithm, and send the processed object & rover coordinate data to Raspberry Pi using ROS.

##Accomplishments that we're proud of
We are proud of the learning that we accomplished in the past 26 hours. Even though none of our group members ever participated in a hackathon, we were successful at learning multiple skills such as implementing computer vision, building a robot and doing wireless transmission of information. Therefore, we are proud of the progress we made throughout the hackathon because we did everything from scratch, with no prior experience in hardware or software to implement.

##What we learned
Throughout the hackathon, we learned many essential skills. For instance, we learned to self-teach ourselves skills that we needed. Furthermore, we also learned about how to implement our ideas. Since our group are all first-time hackers, we had no prior experience. However, we were able to learn how to implement OpenCV, Pyro5 wireless transmission and the firmware required to set up a Raspberry Pi with ROS that is able to take wireless transmission data. Furthermore, we learned that even though some project may seem implausible at first or really difficult to accomplish, one must be in the process of doing it to truly know whether it is difficult or not.

##What's next for WALL-F
Wall-F is an unfinished product with endless potential. The next step is debugging our system and completing the product. Currently, the design acts as a proof of concept, and more minor adjustments must be made. Furthermore, every separate part of this build has been completed, but more time is needed to seamlessly combine all aspects of this build. The next step for Wall-F is turning it into a final product that incorporates every aspect that we have build.
