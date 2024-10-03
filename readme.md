# Drone Data Analytics for Measuring Traffic Metrics at Intersections in High-Density Areas
## Introduction
This study employed over 100 hours of high-altitude drone video data from eight intersections in Hohhot to generate a unique and extensive dataset encompassing high-density urban road intersections in China. This research has enhanced the YOLOUAV model to enable precise target recognition on unmanned aerial vehicle (UAV) datasets. An automated calibration algorithm is presented to create a functional dataset in high-density traffic flows, which saves human and material resources. This dataset can capture up to 200 vehicles per frame while accurately tracking over 1 million road users, including cars, buses, and trucks. Moreover, the dataset has recorded over 50,000 complete lane changes. It is the largest publicly available road user trajectories in high-density urban intersections. Furthermore, this paper updates speed and acceleration algorithms based on UAV elevation and implements a UAV offset correction algorithm. A case study demonstrates the usefulness of the proposed methods, showing essential parameters to evaluate intersections and traffic conditions in traffic engineering. The model can track more than 200 vehicles of different types simultaneously in highly dense traffic on an urban intersection in Hohhot, generating heatmaps based on spatial-temporal traffic flow data and locating traffic conflicts by conducting lane change analysis and surrogate measures. With the diverse data and high accuracy of results, this study aims to advance research and development of UAVs in transportation significantly. UAV data can be obtained by contacting the author.

## Trajectory, Speed, Acceleration, and Direction Extraction
This section provides an overview of the methods used to extract trajectory, speed, acceleration, and directional data from the high-altitude UAV footage. These metrics are crucial for analyzing traffic flow dynamics and understanding vehicular behavior in complex urban environments.

![Video Preview](https://github.com/Qpu523/High-density-Intersection-Dataset/blob/ed9805a5d68c1fba75130c7e56014c3ea489f764/Datashare/11.jpg)

[Watch the Video](https://github.com/Qpu523/High-density-Intersection-Dataset/blob/3e808ab6db80f6a9262a8eb99d99264aee201447/Datashare/1.mp4)



## Dataset Structure

The dataset consists of the following files:
- `video`: Original UAV recorded video.
- `CSV file`: Contains the vehicle data extracted from UAV video.
- `Dataset Sample`

| Frame Num | ID  | Type | Xmin | Ymin | Xmax | Ymax | Speed (km/h) | Direction | Acceleration (m/s²) | UP | RIGHT | DOWN | LEFT |
|-----------|-----|------|------|------|------|------|--------------|-----------|---------------------|----|-------|------|------|
| 5         | 103 | car  | 790  | 709  | 812  | 764  | 27           | DOWN      | -0.08               | 22 | 8     | 25   | 9    |
| 5         | 104 | car  | 1482 | 613  | 1550 | 637  | 18           | RIGHT     | -0.08               | 22 | 9     | 25   | 9    |
| 5         | 105 | car  | 807  | 523  | 827  | 577  | 24           | DOWN      | 0.04                | 22 | 9     | 26   | 9    |





## DownLoad intersection Dataset

<table>
<tr>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/Eh535616YC1DujFzQGgjfoABNAF4UzfXG4xZ9Dk53KslOw?e=5qbybt">A. Zhandong Road</a></th>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/EtxFOZiyGrtMhD-bgD1lem0B7nWK5h_vIb1_k6ii9JxkHQ?e=6wBT99">B. Dongying Road</a></th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/A.%20Zhandong%20Road.jpg" alt="A. Zhandong Road" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/B.%20Dongying%20Road.jpg" alt="B. Dongying Road" /></td>
</tr>
<tr>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/Ekuu_jmamxdIgFZjYTCjLJYBumRynRtFKIAY25wxNd2dVg?e=M3kv38">C. Xing'an South Road‎</a></th>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/EsPlL4srQuRBgodxaZY1CaIBTaZru71udecvcmURbQakvA?e=cwtgNO">D. Ulanqab East Street</a></th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/C.%20Xing'an%20South%20Road%E2%80%8E.jpg" alt="C. Xing'an South Road‎" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/fe391330d81c060d613203e1ad7c5fbab35a0f48/Datashare/D.%20Ulanqab%20East%20Street.jpg" alt="D. Ulanqab East Street" /></td>
</tr>
<tr>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/EhM_t4DUnhhGpx9n88T4TAgBIpx01YCOoIoCZsqG5numpQ?e=loOjEO">E. People's Hall</a></th>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/EjyLu4pVh4pJqxBy0maGVr8BS3S7Ezj8DqdOkkN43kb3fA?e=UGgMPS">F. South intersection</a></th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/E.%20People's%20Hall.jpg" alt="E. People's Hall" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/F.%20South%20intersection.jpg" alt="F. South intersection" /></td>
</tr>
<tr>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/EqRV-9Zsku9MoM6f6HHJ_GMBk4PSVJLdEDWX5ipdiz2ccQ?e=vAxPiY">G. Xinhua Square</a></th>
<th><a href="https://olddominion-my.sharepoint.com/:f:/g/personal/qpu001_odu_edu/ElCvA5YzhH5GvOpq8mJjVU8BKqig1WqahXytJPekT5CVhw?e=EJd7NP">H. Zhongshan Road</a></th>
</tr>
<tr>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/G.%20Xinhua%20Square.jpg" alt="G. Xinhua Square" /></td>
<td align="center"><img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/5bc52ca9acc2b926886e86846faef83c043b1a85/Datashare/H.%20Zhongshan%20Road.jpg" alt="H. Zhongshan Road" /></td>
</tr>
</table>

## Support by

<div style="display: flex; justify-content: space-between; margin-bottom: 20px;">
    <div style="text-align: center;">
        <img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/c70887961a1eb9fca9e903805d3c9a1d4bfbaf0e/Datashare/IMU.png" alt="Inner Mongolia Center for Transportation Research" style="width: 350px; height: auto;">
        <div>
            <strong>Inner Mongolia Center for Transportation Research</strong><br>
            Inner Mongolia Engineering Research Center for Urban Transportation Data Science and Applications,<br>
            Transportation Data Analysis and Visualization Laboratory.
        </div>
    </div>
    
    <div style="text-align: center;">
        <img src="https://github.com/Qpu523/High-density-Intersection-Dataset/blob/df1e43682b1b57ded8a21bf0ef4cca0d87d7ecd4/Datashare/ODU.jpg" alt="Transportation Informatics Lab" style="width: 350px; height: auto;">
        <div>
            <strong>Transportation Informatics Lab, Old Dominion University</strong>
        </div>
    </div>
</div>





## Accessing more Data
If you want to access more data, please contact zhuyuan@imu.edu.cn, qpu001@odu.edu.

## Citation
If you use this dataset and method in your research, please use the following citation:
```bibtex
@article{},
}
