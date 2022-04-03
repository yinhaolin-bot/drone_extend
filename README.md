# drone_extend
drone_extend is an extension simulation of [px4_fast_planner](https://github.com/mzahana/px4_fast_planner). This repository is a version of px4_fast_planner with D435i Depth Camera.

![Screenshot from 2022-04-03 17-37-16](https://user-images.githubusercontent.com/69444682/161423568-9e9745f3-2495-4862-88ad-cf51b8f227a2.png)
![Screenshot from 2022-04-02 23-28-19](https://user-images.githubusercontent.com/69444682/161424850-f0777c14-0e91-49b4-b0b0-c5ebf77abcb6.png)

## Change
To use VIO, you must change some parameters.
| Param | Original | After |
| --- | --- | --- |
| EKF2_AID_MASK | 1 | 24 |
| EKF2_HGT_MODE | 0 | 3 |

![Screenshot from 2022-04-03 22-04-06](https://user-images.githubusercontent.com/69444682/161434374-f3bc683e-49c7-4d66-aaef-a83267a49db8.png)
