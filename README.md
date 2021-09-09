# LVI-SAM-MODIFIED

This repository is a modified version of [LVI_SAM](https://github.com/TixiaoShan/LVI-SAM).

---

## Modification

- Custom extrinsic parameters are adopted in the code.
- The original code assumes there are no translation between the sensors. Now extrinsic parameters including both translation and rotation among IMU, Camera, LiDAR in .yaml in the ```config``` folder are correctly used.
  - params_lidar.yaml: lidar to imu extrinsic (i.e. imu pose w.r.t lidar frame)
  - params_camera.yaml: imu to cam, lidar to cam, lidar to imu extrinsic (sorry for the cubersome process...)  


---

## Warnings

- Currently, the code is modified to use the ```Ouster```.
- If you want to use the ```velodyne```, you have to uncomment [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L4-L17) and [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L523) and comment [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L19-L35) and [here](https://github.com/epicjung/LVI_SAM_fixed/blob/311368c75e3be5cc1fc631ef257bbae501b3f605/src/lidar_odometry/imageProjection.cpp#L524).
- Also, you need to change the .yaml file. 
---

## Acknowledgement

  - The original version is from [LVI-SAM](https://github.com/TixiaoShan/LVI-SAM).
