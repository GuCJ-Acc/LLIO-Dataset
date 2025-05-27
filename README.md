# LLIO-Dataset
This is a legged robot dataset containing leg kinematics (joint encoders), imu and lidar.

<p align='center'>
    <img src="https://github.com/GuCJ-Acc/LLIO-Dataset/blob/master/figure/dataset-wildOvervie.png" alt="drawing" width="600"/>
</p>


## sequence
- **forest**: The robots operating in the forests, which face monotonous environments and are prone to deterioration in localization performance.
- **grass**: The robot operating on the grass, where the ground is uneven and open.
- **parks**: The robot operating on large flat surfaces.
- **roughTerrain**:  The robot operating on uneven terrain in the wild, where contain gravel, soft ground covered in leaves, loose sand and slopes.
- **wild-01**: The robot operating on various types of terrain, including all terrain types in the sequence of **roughTerrain**, flat roads, and forest environments.
- **wild-02**: The robot operating in large-scale environments, including all terrain environments in the sequences of **roughTerrain** and **wild-01**, as well as open sports field environments.


### Rosbag Download
- Some rosbag for the sequence is provided in link [Google Drive](https://drive.google.com/drive/folders/1w2_4lR7wVIgLpnxfRJwVT1kJBXl-jMyI), which contains the ground truth. We obtain truth values through RTK sensor.
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


