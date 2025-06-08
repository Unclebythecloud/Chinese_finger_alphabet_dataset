# Chinese finger alphabet dataset based on sensor glove

## Dataset Source
Our dataset is sourced from five participants. Each participant contributes data to form an independent test set, which ensures unbiased validation across individual datasets. As a result, there are a total of five distinct datasets, indexed from 0 to 4. Each dataset is 12-dimensional, reflecting the combined measurements from five bending sensors, one MPU6050 sensor, and one EMG sensor.

## Sensors Involved in Data Collection
1. **Five bending sensors**:
   - **Function**: To measure the curvature of fingers and capture nuanced hand gestures.
   - **Placement**: We placed them on five fingers to better capture finger curvature information.
2. **One MPU6050 sensor**:
   - **Function**: For recording inertial measurements, including acceleration and angular velocity, contributing three dimensions to the dataset.
   - **Placement**: We place it on the back of the hand, at the position of the purlicue (the fleshy part between the thumb and index finger).
3. **One EMG sensor**:
   - **Function**: To monitor muscle electrical activity, providing additional information about muscle contractions during gestures, contributing one dimension to the dataset.
   - **Placement**: We place it on the forearm to facilitate the collection of information from the forearm muscles.

The 12 dimensions of the dataset comprise measurements from these sensors, collectively offering a comprehensive view of the gestures performed.

## Data Preprocessing
1. **Kalman Filtering**:
   - **Applied to**: MPU6050 sensor data.
   - **Parameters**:
     - Initial estimate = 0.0
     - Initial estimate uncertainty = 1.0
     - Process noise = 0.001
     - Measurement noise = 0.1
   - **Rationale**: These values were empirically selected based on the sensor characteristics to optimize filtering performance.
2. **Normalization**:
   - **Method**: Performed using Z-Score normalization to standardize signal scales across all sensors. 

