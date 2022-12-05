# RBTrajectoryDataReadme

## About the dataset
The dataset contains the vehicle trajectory data perceived by the roadside perception system deployed at the two-lane roundabout at the intersection of State St. and W. Ellsworth Rd. in Ann Arbor, Michigan.
+ The data was collected from 9am to 7pm in September 2022.
+ The data sample rate is 2.5Hz.
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
  |-2022-09-01.zip
  |-2022-09-02.zip
  ...
  `-2022-09-30.zip
```
Each zip file contains multiple json files. 
```
2022-09-01.zip
  |-2022-09-01 09-00-28-452291.json
  |-2022-09-01 09-00-28-841508.json
  |-2022-09-01 09-00-29-252612.json
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
    "uuid": "d3175b38-4e73-42f9-abb3-564b05788e90",       # the universal unique id of the vehicle
    "category": 0.0,      # the category of the vehicle (0: cars, 1: truck/bus/trailer)
    "speed": 1.536,      # the speed of the vehicle (m/s)
    "speed_heading": -1.741,      # the heading of the vehicle (north: 0, clock-wise)
    "predicted_future":     # predicted future vehicle position at the next six frames by our trajectory prediction model
      {
        "mean":     # the mean of the predicted future vehicle position
          [
            [42.22948273444069, -83.73878684072021], 
            [42.22951917166349, -83.73882189902272], 
            [42.22955463092418, -83.73885653671525], 
            [42.22959806281623, -83.73889505995245], 
            [42.229641211286584, -83.73891961750685], 
            [42.229683881407645, -83.73894786679861]
          ], 
        "std":     # the variance of the predicted future vehicle position
          [
            [0.0, 0.0], 
            [3.3877596180390264e-06, 5.4456512171775565e-06], 
            [3.7547065911662862e-06, 5.874294391702309e-06], 
            [4.419491663688003e-06, 6.963602536202044e-06], 
            [5.08341492670003e-06, 8.755623608381619e-06], 
            [6.052037926312747e-06, 1.0661085971328865e-05]
          ]
      }
```

## Download
[Download link]()

## Terms of use

## License

## Acknowledgment

The dataset is supported by [Mcity](https://mcity.umich.edu/) and [National Science Foundation](https://www.nsf.gov/).
