# mixing_quantification
Allows quantification of mixing of a fluorophore in microfluidic channels

### Author Information

Name: Yael Suárez

Institution: Uppsala University

Email: yael.suarez@farmaci.uu.se


You can download mixing_quantification.ipynb as a jupyter notebook and run it with python 3.10

## Requirements 

- numpy
- os
- matplotlib.pyplot 
- PIL 
- pandas

## Usage

The input of the script is a local folder that contains PNG files. The script will graph a concentration plot of all the PNG files contained in the folder specified in path and calculate the Relative Mixing Index according to (Hashmi & Xu, 2014, DOI: 10.1177/2211068214540156). Before running the script, fill in the second cell with the following information:

path = r'path to files'

save_path = r'path where files are to be saved'

conc = concentration of fluorophore to be used in mg/mL

font_size = Desired font size for output graphs

save_status = Write "save" to save the PNG files, otherwise, leave blank 

reference = Write "No" if no reference shall be taken, otherwise, index of image to be used as a reference

title_graph = Title of the output graphs
