# LVI-SAM-MODIFIED

This repository is a modified version of [LVI_SAM](https://github.com/TixiaoShan/LVI-SAM).

<p align='center'>
    <img src="./doc/demo.gif" alt="drawing" width="800"/>
</p>

---

## Modification

- Custom extrinsic parameters are adopted in the code.
- The original code assumes there are no translation between the sensors. Now extrinsic parameters including both translation and rotation among IMU, Camera, LiDAR in .yaml in the ```config``` folder are correctly used.


---

## Warnings

- Currently, the code is modified to use the ```Ouster``` lidar sensor.
- If you want to use the velodyne sensor, you have to uncomment [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L4-L17) and [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L523) and comment [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L19-L35) and [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L524).
- Also, 
```
cd ~/catkin_ws/src
git clone https://github.com/TixiaoShan/LVI-SAM.git
cd ..
catkin_make
```

---


## Paper 

Thank you for citing our [paper](./doc/paper.pdf) if you use any of this code or datasets.

```
@inproceedings{lvisam2021shan,
  title={LVI-SAM: Tightly-coupled Lidar-Visual-Inertial Odometry via Smoothing and Mapping},
  author={Shan, Tixiao and Englot, Brendan and Ratti, Carlo and Rus Daniela},
  booktitle={IEEE International Conference on Robotics and Automation (ICRA)},
  pages={to-be-added},
  year={2021},
  organization={IEEE}
}
```

---

## Acknowledgement

  - The original version is from [LVI-SAM](https://github.com/TixiaoShan/LVI-SAM).
