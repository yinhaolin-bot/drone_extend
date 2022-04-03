# drone_extend
drone_extend is an extension simulation of [px4_fast_planner](https://github.com/mzahana/px4_fast_planner). This repository is a version of px4_fast_planner with D435i Depth Camera.

* To use max performance, you must enable NVIDIA graphic driver
<img src="https://user-images.githubusercontent.com/69444682/161436743-24bf3fba-152f-46b6-afeb-8c8111feed8b.png" width="100" height="100">
![Screenshot from 2022-04-03 22-58-23](https://user-images.githubusercontent.com/69444682/161436743-24bf3fba-152f-46b6-afeb-8c8111feed8b.png)
![Screenshot from 2022-04-03 22-58-50](https://user-images.githubusercontent.com/69444682/161436744-ff26448c-d852-4861-832e-317c51d954ff.png)

* Check `/camera/imu` topic. Type as below

![Screenshot from 2022-04-02 23-28-19](https://user-images.githubusercontent.com/69444682/161424850-f0777c14-0e91-49b4-b0b0-c5ebf77abcb6.png)

## Change
To use VIO, you must change some parameters.
| Param | Original | After |
| --- | --- | --- |
| EKF2_AID_MASK | 1 | 24 |
| EKF2_HGT_MODE | 0 | 3 |

![Screenshot from 2022-04-03 22-04-06](https://user-images.githubusercontent.com/69444682/161434374-f3bc683e-49c7-4d66-aaef-a83267a49db8.png)
