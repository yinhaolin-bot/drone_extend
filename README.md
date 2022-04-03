# drone_extend
drone_extend is an extension simulation of [px4_fast_planner](https://github.com/mzahana/px4_fast_planner). This repository is a version of px4_fast_planner with D435i Depth Camera.

## Show simulation
* To use max performance, you must enable NVIDIA graphic driver

<img src="https://user-images.githubusercontent.com/69444682/161436743-24bf3fba-152f-46b6-afeb-8c8111feed8b.png" width="400"> <img src="https://user-images.githubusercontent.com/69444682/161436744-ff26448c-d852-4861-832e-317c51d954ff.png" width="380">

* Check `/camera/imu` topic and view_frames. Type as below:
```shell
$ rosrun tf view_frames && evince frames.pdf
```
<img src="https://user-images.githubusercontent.com/69444682/161424850-f0777c14-0e91-49b4-b0b0-c5ebf77abcb6.png" width="300"> <img src="https://user-images.githubusercontent.com/69444682/161437262-020d612a-654a-4ffd-9b4d-45b3d327fdb7.png" width="450">

## Change
To use VIO, you must change some parameters.
| Param | Original | After |
| --- | --- | --- |
| EKF2_AID_MASK | 1 | 24 |
| EKF2_HGT_MODE | 0 | 3 |

![Screenshot from 2022-04-03 22-04-06](https://user-images.githubusercontent.com/69444682/161434374-f3bc683e-49c7-4d66-aaef-a83267a49db8.png)
