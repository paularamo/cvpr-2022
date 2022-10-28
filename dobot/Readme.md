## Steps to use these notebooks
Note: The next steps have not had a probe reader, I will come back to this steps Oct 31/2022. I am going to update these notebooks, but this is a big picture of the complet process.

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
14. Save [cubes_config.yaml](https://github.com/paularamo/cvpr-2022/blob/gh-pages/dobot/cubes_config.yaml) the this path '''../../anomalib/models/{MODEL}/cubes_config.yaml'''
15. Verify if this file has this two lines (See the highlights on image). If the asnwer is "Yes", please delete those three lines.
16. Change the inference.py file by this one https://github.com/paularamo/cvpr-2022/blob/gh-pages/dobot/inference.py and modify this line of code with your path result. ![image](https://user-images.githubusercontent.com/10940214/198699965-28330883-f2d6-4692-8452-8b2623f39514.png)
17. Before to run [this notebook](
https://github.com/paularamo/cvpr-2022/blob/gh-pages/dobot/notebooks/001-getting-started-cubics/001-getting-started-Inference-cubics.ipynb), verify your dataset is well-connected with the notebook, verify that the inference is working and you can see the confidence result in the text file.
18. It will take some minutes to run have the mode ready. You don't need a GPU, if you have one the training will be faster.
19. Verify where the model is saved. The model will be saved in the same folder of this notebook ''' ..\results\padim\cubes\weights\model.ckpt '''.
### Inference
20. Come back to [the main notebook](https://github.com/paularamo/cvpr-2022/blob/gh-pages/dobot/notebooks_control/Anomalib_Dobot_cubics_FINAL.ipynb).
21. Verify that you have the proper path for the model you have created. (Cell #2) ![image](https://user-images.githubusercontent.com/10940214/198702126-ee1c5e2b-a598-421a-98a3-743de5353028.png)
21. Verify that you have the inference text file linked properly. Same path than the step #16.
22. In the cell #3 change the flag status to "False"![image](https://user-images.githubusercontent.com/10940214/198696596-459c97be-8789-4878-a038-1fa417a0b4c8.png).
23. Run the notebook.
Have Fun! 😊

