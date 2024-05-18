# mixing_quantification
Allows quantification of mixing of a fluorophore in microfluidic channels

### Author Information

Name: Yael Suárez

Institution: Uppsala University

Email: yael.suarez@farmaci.uu.se


You can download mixing_quantification.ipynb as a jupyter notebook and run it with python 3.10

## Requirements 

- numpy
- datetime
- os
- matplotlib.pyplot 
- PIL 
- pandas

## Usage

The input of the script is a local folder that contains PNG files. The script will graph a concentration plot of all the PNG files contained in the folder specified in path and calculate the Relative Mixing Index according to (Hashmi & Xu, 2014, DOI: 10.1177/2211068214540156). 

1. Before running the script, fill in the second cell with the following information:
    - path = # The folder path where the images to be processed are contained. Images must be .png
    - save_path = r'' # The folder path where the results are to be saved
    - conc = 2 #set concentration of fluorophore
    - font_size = 14 # Font size of the graphs
    - save_status = "save" #"save" to save the PNG files, otherwise leave empty
    - reference = 0 #"No" if no reference image to normalize the rest of the images shall be taken, otherwise, index
    - title_graph = ""
    - line_or_square = "s" #"l" to plot a line and "s" to plot a square of w width in pixels
    - w = 20 #Width of pixels to use for line
    - px_to_nm = 2.09 # pixel resolution


2. After running cell [5], a yaml configuration cell containing information for each of the images contained in the folder path, will appear:
    - filename: r"ROI 4.png" #This will be the name of the image contained in the folder
    - filepath: r" " #This will be the path of the image contained in the folder
    - orientation: 1 # 0 = horizontal, 1 = vertical, orientation of the line to take the concentration profile
    - line_pos_x: 1250 # For vertical lines, this position must be adjusted so that the profile line is in the ROI
    - line_pos_y: 300 # For horizontal lines, this position must be adjusted so that the profile line is in the ROI

3. After running cell [8] the processed images will appear, and the line_pos_x or line_pos_y can be adjusted to match the ROI.

4. Once all the ROI are adjusted, the rest of the script can be ran.
