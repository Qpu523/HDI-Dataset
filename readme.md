# Drone Data Analytics for Measuring Traffic Metrics at Intersections in High-Density Areas
## Introduction
This study employed over 100 hours of high-altitude drone video data from eight intersections in Hohhot to generate a unique and extensive dataset encompassing high-density urban road intersections in China. This research has enhanced the YOLOUAV model to enable precise target recognition on unmanned aerial vehicle (UAV) datasets. An automated calibration algorithm is presented to create a functional dataset in high-density traffic flows, which saves human and material resources. This dataset can capture up to 200 vehicles per frame while accurately tracking over 1 million road users, including cars, buses, and trucks. Moreover, the dataset has recorded over 50,000 complete lane changes. It is the largest publicly available road user trajectories in high-density urban intersections. Furthermore, this paper updates speed and acceleration algorithms based on UAV elevation and implements a UAV offset correction algorithm. A case study demonstrates the usefulness of the proposed methods, showing essential parameters to evaluate intersections and traffic conditions in traffic engineering. The model can track more than 200 vehicles of different types simultaneously in highly dense traffic on an urban intersection in Hohhot, generating heatmaps based on spatial-temporal traffic flow data and locating traffic conflicts by conducting lane change analysis and surrogate measures. With the diverse data and high accuracy of results, this study aims to advance research and development of UAVs in transportation significantly.

## Trajectory, Speed, Acceleration, and Direction Extraction
This section provides an overview of the methods used to extract trajectory, speed, acceleration, and directional data from the high-altitude UAV footage. These metrics are crucial for analyzing traffic flow dynamics and understanding vehicular behavior in complex urban environments.

![Video Preview](https://github.com/Qpu523/High-density-Intersection-Dataset/blob/ed9805a5d68c1fba75130c7e56014c3ea489f764/Datashare/11.jpg)

[Watch the Video](https://github.com/Qpu523/High-density-Intersection-Dataset/blob/3e808ab6db80f6a9262a8eb99d99264aee201447/Datashare/1.mp4)



## Dataset Structure
This is a raw data, you can perform data smoothing and preliminary processing according to your needs.
The dataset consists of the following files:
- `video`: Original UAV recorded video.
- `CSV file`: Contains the vehicle data extracted from UAV video.
- `Dataset Sample`


| Frame Num | ID  | Type | Xmin | Ymin | Xmax | Ymax | Speed (km/h) | Direction | Acceleration (m/s²) | UP | RIGHT | DOWN | LEFT |
|-----------|-----|------|------|------|------|------|--------------|-----------|---------------------|----|-------|------|------|
| 5         | 103 | car  | 790  | 709  | 812  | 764  | 27           | DOWN      | -0.08               | 22 | 8     | 25   | 9    |
| 5         | 104 | car  | 1482 | 613  | 1550 | 637  | 18           | RIGHT     | -0.08               | 22 | 9     | 25   | 9    |
| 5         | 105 | car  | 807  | 523  | 827  | 577  | 24           | DOWN      | 0.04                | 22 | 9     | 26   | 9    |


## Location Information of  HDI Dataset

![Video Preview](https://github.com/Qpu523/HDI-Dataset/blob/8369f364d6e329575cc480cb3cb2a8c33442c592/Datashare/Location2.png)


## DownLoad intersection HDI Dataset

<table>
<tr>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/EkF262NRK1lKveY8YIgisbYB8H8bCtOd-heAbXXpdZuzKA?e=4R0poG">A. Zhandong Road<br></a>(新华大街与展览馆东路交叉口)</th>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/ElI0FBgqHZVPhT5n_qPzvS4BJHmrzOS9p-LzFF_fu-Pssg?e=enWkHS">B. Dongying Road<br></a>(新华大街与东影南路交叉口)</th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/A.%20Zhandong%20Road.jpg" alt="A. Zhandong Road" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/B.%20Dongying%20Road.jpg" alt="B. Dongying Road" /></td>
</tr>
<tr>

<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/ErdeZ63lkilFp551i3kKBlMBrwmzUajjj1FpcP9N-NcpOw?e=73rb23">C. Ulanqab East Street<br></a>(新华大街与兴安南路交叉口)</th>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/EhslYEyJxkdPgwB_cK9HwgMBOjCa767Id6r8meT_zDHCUg?e=BLfgmJ">D. Xing'an South Road‎<br></a>(兴安南路与乌兰察布东街交叉口)</th>
</tr>
<tr>

<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/921f389b07943e26cd354f5a729d3c615f90d496/Datashare/D.%20Ulanqab%20East%20Street.jpg" alt="C. Ulanqab East Street" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/C.%20Xing'an%20South%20Road%E2%80%8E.jpg" alt="D. Xing'an South Road‎" /></td>
</tr>
<tr>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/Eh6eA0HKtLZBrurIjroURQoBpCerwNl0T05cfEbKvEc1Jg?e=B2sk6Z">E. People's Hall<br></a>(新华大街与呼伦贝尔北路交叉口)</th>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/EoqhenU9U2RFqJgxDeBEqoEBWuSa89xabR_zyaDB6ZFIpQ?e=ms7iWh">F. South intersection<br></a>(中山路与呼伦贝尔路交叉口)</th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/E.%20People's%20Hall.jpg" alt="E. People's Hall" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/F.%20South%20intersection.jpg" alt="F. South intersection" /></td>
</tr>
<tr>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/Eq7IaCfOvLxNu9QF1phcIwIBcRTzzz41JjZc1yUrXRRikQ?e=Fxt1xL">G. Xinhua Square<br></a>(新华大街与锡林北路交叉口)</th>
<th><a href="https://1drv.ms/f/c/54547f6bb45158b3/EqZP4i54-VBJrU06-q2GW-oBJUXbfPP5qWq24l6DScJqUw?e=iUnA0u">H. Zhongshan Road<br></a>(中山路与锡林南路交叉口)</th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/G.%20Xinhua%20Square.jpg" alt="G. Xinhua Square" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/H.%20Zhongshan%20Road.jpg" alt="H. Zhongshan Road" /></td>
</tr>
<tr>
  <th><a href="https://1drv.ms/f/c/54547f6bb45158b3/Es9p2iuAr_1EufuhhdKwYnsBmvyb8el96prvbcO3asj2pg?e=ask2ow">Mixed Road User Interaction <br> (Cars, Pedestrians, E-bikes)</a></th>
  <th></th>
</tr>
<tr>
  <td align="center">
    <img src="https://github.com/Qpu523/HDI-Dataset/blob/449906a6b8d50986aa5c673123488f90a984131f/Datashare/car%2Bpedestrian%2BE-bike.png" alt="Mixed Road User Interaction (Cars, Pedestrians, E-bikes)" />
  </td>
  <td></td>
</tr>

    
</table>


## Support by

<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/071e90b832a8ec69f72ee375b21a95f051d3ad77/Datashare/IMU.png" alt="Inner Mongolia Center for Transportation Research" style="width: 400px; height: auto; margin-right: 20px;">
    <div>
        <strong>Inner Mongolia Center for Transportation Research</strong><br>
        Inner Mongolia Engineering Research Center for Urban Transportation Data Science and Applications,<br>
        Transportation Data Analysis and Visualization Laboratory.
    </div>
</div>

<div style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/d30ea0e5b03a7d6220c42eaa7c12d2e646875ab1/Datashare/ODU%20.jpg" alt="Old Dominion University" style="width: 400px; height: auto; margin-right: 20px;">
    <div>
        <strong>SenseLane Lab, Old Dominion University</strong><br>
        <strong>Transportation Informatics Lab, Old Dominion University</strong><br>
    </div>
</div>







## Accessing more Data
If you want to access more data, please contact zhuyuan@imu.edu.cn, qpu001@odu.edu.

## Citation
If you use this dataset and method in your research, please use the following citation:
```bibtex
@article{pu2025drone,
  title={Drone Data Analytics for Measuring Traffic Metrics at Intersections in High-Density Areas},
  author={Pu, Qingwen and Zhu, Yuan and Wang, Junqing and Yang, Hong and Xie, Kun and Cui, Shunlai},
  journal={Transportation Research Record},
  year={2025},
  volume={0},
  number={0},
  doi={10.1177/03611981241311566},
  publisher={SAGE Publications}
}

@article{pu2025curvttc,
  title={Modeling crash avoidance behaviors in vehicle-pedestrian near-miss scenarios: Curvilinear time-to-collision and Mamba-driven deep reinforcement learning},
  author={Pu, Qingwen and Xie, Kun and Guo, Hongyu and Zhu, Yuan},
  journal={Accident Analysis & Prevention},
  volume={214},
  pages={107984},
  year={2025},
  publisher={Elsevier},
  doi={10.1016/j.aap.2025.107984},
  url={https://doi.org/10.1016/j.aap.2025.107984}
}
@article{wang2025shockwave,
  title={A simulation study on traffic conflict risk under shockwave propagation at signalized intersections},
  author={Wang, Junqing and Yang, Hong and Zhu, Yuan and Xie, Kun and Yan, Zizheng and Pu, Qingwen},
  journal={Accident Analysis & Prevention},
  volume={218},
  pages={108081},
  year={2025},
  publisher={Elsevier},
  doi={10.1016/j.aap.2025.108081},
  url={https://doi.org/10.1016/j.aap.2025.108081}
}




