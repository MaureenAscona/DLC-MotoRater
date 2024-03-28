DLC User Guide for Tracking and Analysis: MotoRater

Video File Organization and Tracking
1.	Prior to analysis, follow this exact video naming schematic. Name the .avi file “animalID_InjuryCondition_#dpi” DO NOT LEAVE SPACES ANYWHERE. 
2.	Open the MR DLC Workflow File. Import Deeplabcut, assuming you have created the environment. Change the config_path to where you have stored the .yaml file in MotoRater2-Maureen-2023-05-02
3.	Scroll to the section that is titled ”Analyze videos, create .csv, create skeleton” and change the file path to where your videos are stored (change ”your file path”). 
4.	Once the path name has been changed, in the top right corner, there is a run all option. Select Run All.
5.	Finally, all videos will be analyzed in the specified folder. Below the ”Analyze videos, create .csv, create skeleton” cell, there will be output confirming the model is being used. Once the analysis is complete, a green checkmark will appear at the end of the cell. 
 
Analysis
1.	DLC above has provided the X, Y coordinates of each limb, now you will have this analyzed using Python and Pandas packages. If you check back to the folder of your data, you should have 8 created files for each analyzed video. DO NOT DISCARD THESE CREATED FILES. 
    a.	You will be using the el_filtered.csv files. NOT THE _el.csv FILES.
3.	In the cell labeled “Locate Data and Collect File Names”, there is a place to add the path, this path is the folder where all of your data is stored. Run this cell to get file paths for all of your files.
5.	Create an environment for this file. It will need to have python 3.7, pandas, scipy, hampel, itertools, matplotlib.
6.	On the next cell named “Consolidate and output”, decide if you want to create figures by silencing/unsliencing this command: walking_fig(cdf).
7.	On This cell, Edit the name of the to_excel file. Run all cells.
8.	If you had multiple runs for the MR, the final cell "Average Columns Based on Names" averages the cells that have overlapping last names. Follow the naming schematic from above. 
