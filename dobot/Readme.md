## Steps to use these notebooks
1. Create an environment to run Anomalib + Dobot DLL (Python version 3.8)
2. Install Anomalib. Follow the instructions here: https://github.com/openvinotoolkit/anomalib
3. Install Dobot requirements (See Dobot documentation here: https://en.dobot.cn/products/education/magician.html)
4. Check all connections of the Dobot, verify if it is working using Dobot Studio.
5. Connect the WebCam and verify it is working, using a simple camera application. Close this app after the verification.
6. Install the vent on the dobot and verify if this is working using Dobot Studio.
7. In Dobot Studio, find "Home" hitting "Home" Button. Then, find the Calibration Coordinates (Initial position upper-left corner of cubes array), Place Coordinates (Position where the arm should leave the cubic over the conveyor belt, camera stop will be same positio + 90 point in Z), and Anomaly Coordinates (Where do you want to release the abnormal cube. ![image](https://user-images.githubusercontent.com/10940214/198698536-9a1c403d-c7e3-4186-955b-4ceefb8fb379.png)
8. In the same environment where you have Dobot and Anomalib installed, verify you have jupyter notebooks or Jupyter Lab installed.
9. Open [the main notebook](https://github.com/paularamo/cvpr-2022/blob/gh-pages/dobot/notebooks_control/Anomalib_Dobot_cubics_FINAL.ipynb) ![image](https://user-images.githubusercontent.com/10940214/198696689-1be3583d-0356-4305-a2cd-f51e4ff62409.png)
### Data acquisition
10. Verify the path folder of the dataset.
11. In the cell #3 change the flag status to "True"![image](https://user-images.githubusercontent.com/10940214/198696596-459c97be-8789-4878-a038-1fa417a0b4c8.png)
12. Organize cubes with no abnormalities in the array and run the notebook, verify the notebook is creating the images.
13. Organize cubes with abnormalities in the array and run the notebook again, verify the notebook is creating the images.
### Training
Open the 

