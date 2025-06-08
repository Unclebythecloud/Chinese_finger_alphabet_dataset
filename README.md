# Chinese_finger_alphabet_dataset
 Chinese finger alphabet dataset baesd on sensor glove
 Our dataset originates from five participants, each contributing data to form an independent test set, ensuring unbiased validation across individual datasets. This results in a total of five distinct datasets, indexed from 0 to 4, where each dataset is 12-dimensional, reflecting the combined measurements from five bending sensors, one MPU6050 sensor, and one EMG sensor.
The sensors involved in data collection include:
 Five bending sensors: To measure the curvature of fingers and capture nuanced hand gestures. We placed them on five fingers to better capture finger curvature information.
One MPU6050 sensor: For recording inertial measurements, including acceleration and angular velocity, contributing three dimensions to the dataset.We place it on the back of the hand, at the position of the purlicue (the fleshy part between the thumb and index finger).
One EMG sensor: To monitor muscle electrical activity, providing additional information about muscle contractions during gestures, contributing one dimension to the dataset.We place it on the forearm to facilitate the collection of information from the forearm muscles.
Thus, the 12 dimensions of the dataset comprise measurements from these sensors, collectively offering a comprehensive view of the gestures performed.
Data preprocessing includes:
Kalman Filtering: Applied to MPU6050 sensor data with the following parameters: initial estimate = 0.0, initial estimate uncertainty = 1.0, process noise = 0.001, and measurement noise = 0.1. These values were empirically selected based on the sensor characteristics to optimize filtering performance.
Normalization: Performed using Z-Score normalization to standardize signal scales across all sensors.

