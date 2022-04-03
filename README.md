# drone_extend
`drone_extend` is an extension simulation of [px4_fast_planner](https://github.com/mzahana/px4_fast_planner). This repository is a version of `px4_fast_planner` with `D435i Depth Camera`.

## Show simulation
* To use max performance, you must enable NVIDIA graphic driver

<img src="https://user-images.githubusercontent.com/69444682/161436743-24bf3fba-152f-46b6-afeb-8c8111feed8b.png" width="425"> <img src="https://user-images.githubusercontent.com/69444682/161436744-ff26448c-d852-4861-832e-317c51d954ff.png" width="400">

* Check `/camera/imu` topic and view_frames. Type as below:
```shell
$ rosrun tf view_frames && evince frames.pdf
```
<img src="https://user-images.githubusercontent.com/69444682/161424850-f0777c14-0e91-49b4-b0b0-c5ebf77abcb6.png" width="325"> <img src="https://user-images.githubusercontent.com/69444682/161437262-020d612a-654a-4ffd-9b4d-45b3d327fdb7.png" width="490">
![Screenshot from 2022-04-03 23-58-41](https://user-images.githubusercontent.com/69444682/161439279-d4dff821-48c1-4543-935a-9b57441047e7.png)

```shell
$ rostopic echo /camera/color/camera_info
#
D: []
K: [462.266357421875, 0.0, 320.0, 0.0, 462.266357421875, 240.0, 0.0, 0.0, 1.0]
R: [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]
P: [462.266357421875, 0.0, 320.0, 0.0, 0.0, 462.266357421875, 240.0, 0.0, 0.0, 0.0, 1.0, 0.0]
#
$ rostopic echo /camera/depth/camera_info
#
D: []
K: [319.9348449707031, 0.0, 320.0, 0.0, 319.9348449707031, 240.0, 0.0, 0.0, 1.0]
R: [0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]
P: [319.9348449707031, 0.0, 320.0, 0.0, 0.0, 319.9348449707031, 240.0, 0.0, 0.0, 0.0, 1.0, 0.0]
#

```
<img src="https://user-images.githubusercontent.com/69444682/161438532-848282e9-aa7e-4526-808d-4ad98a3bcee0.png" width="400"> <img src="https://user-images.githubusercontent.com/69444682/161438530-efd8c5ac-1aaa-498c-ac74-7f890c29b904.png" width="400">

## Change
To use VIO, you must change some parameters.
| Param | Original | After |
| --- | --- | --- |
| EKF2_AID_MASK | 1 | 24 |
| EKF2_HGT_MODE | 0 | 3 |

![Screenshot from 2022-04-03 22-04-06](https://user-images.githubusercontent.com/69444682/161434374-f3bc683e-49c7-4d66-aaef-a83267a49db8.png)
