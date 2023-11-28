# Ann Arbor Intersection Trajectory Data

## Introduction
The dataset contains the vehicle trajectory data perceived by the roadside perception system deployed in the City of Ann Arbor, Michigan, through the [Smart Intersections Project](https://sip.umtri.umich.edu/).
+ The data was collected at the roundabout, signalized intersections, and pedestrian crossing midblock of City of Ann Arbor, Michigan.
+ The data was collected from 9am to 6pm in the third quarter of 2023.
+ Msight roadside perception system is used to extract the vehicle trajectories from raw video frames.

## Citation
> [Design, Implementation, and Evaluation of a Roadside Cooperative Perception System](https://drive.google.com/file/d/1lNYbGUzCMqt1zLPuyrfwM0NuiCS9hfpf/view)<br />
> Rusheng Zhang, Zhengxia Zou, Shengyin Shen, and Henry X. Liu<br />
> *Transportation Research Record, 2022*
> ```
> @article{zhang2022design,
>     author = {Rusheng Zhang and Zhengxia Zou and Shengyin Shen and Henry X. Liu},
>     title ={Design, Implementation, and Evaluation of a Roadside Cooperative Perception System},
>     journal = {Transportation Research Record},
>     volume = {2676},
>     number = {11},
>     pages = {273-284},
>     year = {2022},
>     doi = {10.1177/03611981221092402},
> }
> ```

> [Real-time full-stack traffic scene perception for autonomous driving with roadside cameras](https://drive.google.com/file/d/1PNY7u606XHUJIs7t1GYU59yzGXQ5PBi_/view?usp=sharing)<br />
> Zhengxia Zou, Rusheng Zhang, Shengyin Shen, Gaurav Pandey, Punarjay Chakravarty, Armin Parchami, and Henry X. Liu<br />
> *International Conference on Robotics and Automation, 2022*
> ```
> @inproceedings{zou2022real,
>   title={Real-time full-stack traffic scene perception for autonomous driving with roadside cameras},
>   author={Zou, Zhengxia and Zhang, Rusheng and Shen, Shengyin and Pandey, Gaurav and Chakravarty, Punarjay and Parchami, Armin and Liu, Henry X},
>   booktitle={2022 International Conference on Robotics and Automation (ICRA)},
>   pages={890--896},
>   year={2022},
>   organization={IEEE}
> }
> ```
## Data format
The dataset is formatted into multiple zip files. Each zip file contains the vehicle trajectory data within one day.
```
root/
  |-state_ellsworth/
  | |-2023-07-08.zip
  | |-2023-07-09.zip
  | ...
  | `-2023-07-14.zip
  |
  `-main_stadium/
    |-2023-09-24.zip
    |-2023-09-25.zip
    ...
    `-2023-09-30.zip
```
Each zip file contains multiple json files. 
```
2023-07-08.zip
  |-2023-07-08 09-00-28-452291.json
  |-2023-07-08 09-00-28-841508.json
  |-2023-07-08 09-00-29-252612.json
  ...
```
Each json file contains the vehicle trajectory data of one frame. Here is an example of the data in a json file
```
[
  {
    "id": "1",    # id of the vehicle (not universal unique id)
    "confidence": 0.849,    # confidence of the vehicle detection
    "lat": 42.301,    # the latitude coordinate of the vehicle position
    "lon": -83.698,   # the longitude coordinate of the vehicle position
    "category": 0.0,      # the category of the vehicle (0: cars, 1: truck/bus/trailer)
    "speed": 1.536,      # the speed of the vehicle (m/s)
    "speed_heading": -1.741,      # the heading of the vehicle (north: 0, clock-wise)
      }
```

## Download

## Terms of use

### Licenses
Unless specifically labeled otherwise, these Datasets are provided to You under a Creative Commons Attribution-Sharealike 4.0 International Public License (“CC BY-SA 4.0”) The CC BY-SA 4.0 may be accessed at https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode. When You download or use the Datasets from the Website or elsewhere, You are agreeing to comply with the terms of CC BY-SA 4.0 and also agreeing to the Dataset Terms. Where these Dataset Terms conflict with the terms of CC BY-SA 4.0, these Dataset Terms shall prevail.

## Acknowledgment

The dataset is supported by [Mcity](https://mcity.umich.edu/) and [National Science Foundation](https://www.nsf.gov/).

## Developers

Depu Meng (depum@umich.edu)

Rusheng Zhang (rushengz@umich.edu)

Boqi Li (boqili@umich.edu)

## Contact

Henry Liu (henryliu@umich.edu)

Sean Shen (shengyin@umich.edu)
