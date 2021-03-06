# EAE3532 Physics of the Solid Earth - Practicals Project

This is the source repository for the EAE3532 practicals project.
A Docker container that holds a semester of Jupyter Notebooks used by 3rd year Monash University Earth Science students.  
The notebooks in the container aim to introduce students to the basics of programming and Python and
the various libraries and techniques needed for Earth Science. I built this container with assistance from the Earth Science
department to replace the previous MatLab tutorials.

### Running from Kitematic  
Search 'eae3532' and click create container.  
Add local content into the __practicals__ folder via the Kitematic Volume Settings.  
Click on the 'Open Browser' button in the Web Preview Pane.  

### Running from Docker Terminal

__docker run -it -p 8888:8888 -v path/to/local:/workspace/practicals eae3532/practicals__  
  
This will pull the image from Docker Hub when run for the first time.  
You can then open a browser at  
  
__http://dockervirtualhostIP:8888__
  
where the docker virtualhostIP appears at the top of the docker terminal.  
  
eg. __http://192.168.99.100:8888__  

### Conda Environment  
  
To set-up the project environment locally from the _environment.yml_ file,  
  
__conda env create -n eae3532 -f environment.yml__  
__conda activate eae3532__  

Then install Jupyter and extensions into the activated environment with,  

__conda install jupyter__  
__conda install -c conda-forge jupyter_contrib_nbextensions__  


#### Enabling Extensions

The nbextensions below are used in the notebooks and can be enabled from the dashboard interface or at the command line,  
  
__jupyter nbextension enable snippets_menu/main__  
__jupyter nbextension enable hide_input/main__  
__jupyter nbextension enable equation-numbering/main__      
__jupyter nbextension enable init_cell/main__  

### custom.js file

Add this file locally to (from root or User)    

__/.jupyter/custom/__ 

<a href="http://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/JavaScript%20Notebook%20Extensions.html">Custom Docs</a>  
