# Park EZ: An Automated Parking Management System for Easy Parking

Deep Learning Course Submission

See full report [HERE](https://github.com/mbdelaresma/automated-parking-management-computer-vision/blob/main/Technical_Report.ipynb)

![image](https://user-images.githubusercontent.com/71246479/188299598-ab431713-b792-4fc4-9d1c-86babd4819db.png)

# Executive Summary

Parking management systems tend to inconvenience customers and serve as cost centers to business owners. Park EZ remedies these pains by serving as a parking management system alternative which automates the entire process for the customer while reducing the costs needed from the owner.

Current automated parking management systems (PMS) involve sensors and computer systems which entail high costs. This project aims to be a jump off point in creating a PMS that relies only on CCTV camera feeds, which are commonly available in these establishments, and methods in computer vision.

The team sampled 156 frames from a CCTV footage of a parking lot, then train a custom YOLO model to detect cars with these manually labeled sampled images as training and validation set, The team created a rule based on the manually labeled irregular quadrilaterals for each of the parking spaces and the detected cars based on its Intersection Over Union (IoU) and its coordinates to decide if the parking space is taken or vacant. In order to attach a timer to each car, we located the centroid of each car and assigned a car id into it then time for each frame that the car id is in the view of the camera.

The application of transfer learning on YOLO has allowed for high precision of 100% on the validation set with fast detection. This allows for robust and real-time detection when deployed as a real-time car tracker. Thresholding for values for rules is dependent on the camera angle and distinguishes between parked cars and edge cases. Together with the timer and unique ID, Park EZ presents a proof of concept for a real time parking management system optimized custom for that parking lot.

Recommendations for this project involve additional features outside the current scope of the study but builds on the aspect of a fully developed parking management system for end-to-end deployment. To further improve this implementation, the authors suggest exploring security monitoring, deployment within a camera network, and a user app. Additional recommendations involve alternative use cases for the system. With modifications to the implementation, this system may be redeployed for employee monitoring, security systems, and traffic management.

![15](https://user-images.githubusercontent.com/71246479/188299646-ef5dbafc-1022-4c87-b3bc-b5f7bbde249f.png)

# Contributors

dela Resma, Marvee

La Rosa, Patrick

Pingol, Miguel

Soriano, Chris
