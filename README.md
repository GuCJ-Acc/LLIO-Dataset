# LLIO-Dataset
This is a legged robot dataset containing leg kinematics (joint encoders), imu and lidar.

<p align='center'>
    <img src="https://github.com/GuCJ-Acc/LLIO-Dataset/blob/master/figure/datasetOverview.png" alt="drawing" width="600"/>
</p>


## sequence
- **forest**: The robots operating in the forests, which face monotonous environments and are prone to deterioration in localization performance.
- **grass**: The robot operating on the grass, where the ground is uneven and open.
- **parks**: The robot operating on large flat surfaces.
- **roughTerrain**:  The robot operating on uneven terrain in the wild, where contain gravel, soft ground covered in leaves, loose sand and slopes.
- **wild-01**: The robot operating on various types of terrain, including all terrain types in the sequence of **roughTerrain**, flat roads, and forest environments.
- **wild-02**: The robot operating in large-scale environments, including all terrain environments in the sequences of **roughTerrain** and **wild-01**, as well as open sports field environments.


### Rosbag Download
- Some of the sequence is provided in link [Google Drive](https://drive.google.com/drive/folders/1w2_4lR7wVIgLpnxfRJwVT1kJBXl-jMyI), which contains the ground truth. We obtain truth values through RTK sensor. We will publish other datasets in the future.
- The sequence with **A1_** label can be used for testing the [Leg-KILO](https://github.com/ouguangjun/Leg-KILO), and our tested the pole length parameters of the legged robot as follows:

```
# A1 pole length parameters
legOffsetX: 0.1881
legOffsetY: 0.04675
legCalfLength: 0.213
legThighLength: 0.213
legThighOffset: 0.08

# X20 pole length parameters
legOffsetX: 0.292
legOffsetY: 0.08
legCalfLength: 0.345
legThighLength: 0.3
legThighOffset: 0.11642
```

## Sensor Information
### sensor type
The data set includes LiDAR, IMU, joint encoders, etc. Taking the sequence **roughTerrain** as an example, the specific data format types are as follows:

```
path:        roughTerrain.bag
version:     2.0
duration:    11:58s (718s)
start:       May 20 2025 16:57:04.69 (1747731424.69)
end:         May 20 2025 17:09:03.07 (1747732143.07)
size:        4.0 GB
messages:    376802
compression: none [3562/3562 chunks]
types:       sensor_msgs/Imu         [6a62c6daae103f4ff57a132d6f95cec2]
             sensor_msgs/JointState  [3066dcd76a6cfaef579bd0f34173e9fd]
             sensor_msgs/PointCloud2 [1158d486dd51d683ce2f1be655c3c181]
topics:      /joint_states      119398 msgs    : sensor_msgs/JointState 
             /velodyne_points     7122 msgs    : sensor_msgs/PointCloud2
             /xsens/imu/data    250282 msgs    : sensor_msgs/Imu
```
### sensor extrinsic parameters
Extrinsic parameters from IMU to LiDAR and from Robot-body to IMU.
```
# IMU to LiDAR extrinsic parameters
extrinsic_T: [ 0, 0, 0.05]
extrinsic_R: [ 1, 0, 0, 
                0, 1, 0, 
                0, 0, 1]

# Robot-body to IMU extrinsic parameters
extrinsic_T: [ 0, 0, 0.273]
extrinsic_R: [ 1, 0, 0, 
                0, 1, 0, 
                0, 0, 1]
```
### /velodyne_points : sensor_msgs/PointCloud2
This is the data provided by velodyne VLP16 lidar at roughly 10 HZ.
### /xsens/imu/data: sensor_msgs/Imu
This is the data provided by MTi 630, which contain measurement information of 9-axis (acceleration, angular velocity, quaternion).
### /joint_states: sensor_msgs/JointState
This is the data provided by X20 joint encoder, which contain measurement information of joint angle, joint angular velocity and joint torque.

### Note
For detailed information on sequences with the **A1_** label, please refer to the [legkilo-dataset](https://github.com/ouguangjun/legkilo-dataset/tree/main).
