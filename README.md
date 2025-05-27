# LLIO-Dataset
This is a legged robot dataset containing leg kinematics (joint encoders), imu and lidar.

## sequence
- **forest**: The robots operating in the forests, which face monotonous environments and are prone to deterioration in localization performance.
- **grass**: The robot operating on the grass, where the ground is uneven and open.
- **parks**: The robot operating on large flat surfaces.
- **roughTerrain**:  The robot operating on uneven terrain in the wild, where contain gravel, soft ground covered in leaves, loose sand and slopes.
- **wild-01**: The robot operating on various types of terrain, including all terrain types in the sequence of **roughTerrain**, flat roads, and forest environments.
- **wild-02**: The robot operating in large-scale environments, including all terrain environments in the sequences of **roughTerrain** and **wild-01**, as well as open sports field environments.


### Rosbag Download
Some rosbag for the sequence is provided in link [Google Drive](https://drive.google.com/drive/folders/1w2_4lR7wVIgLpnxfRJwVT1kJBXl-jMyI), which contains the ground truth. We obtain truth values through RTK sensor.
