********************************************

# Install gdal and its python interface
Illustrate how to install the python interface of GDAL in Ubuntu os.
##  Download source file
You can download the source package via http://download.osgeo.org/gdal/  
- if you download the *.zip file, use **`unzip *.zip`** to get directory */gdal_x_x_x/  
- if you download the *.tar.gz format, use **`tar -xzvf *.tar.gz`** to get directory */gdal_x_x_x/ 
or you can use `wget` to download the file.

## compile what you download
follow the command to enter the gdal package:  
`cd  gdal-x.x.x`  
`./configure --with-python` --> compile the python interface  
`make`  
`make install`  

## Configuration
 
Add **`export LD_LIBRARY_PATH=$LD_LIBRARY_PATH：/usr/local/lib`** to the `~/.bashrc` and `/etc/profile` 

## build the python package
`cd */gdal-x.x.x/swig/python`  
`sudo python setup.py build`  
`sudo python setup.py install`  


`sudo find / -name gdal.py`
add all path containing gdal.py as *PYTHONPATH* to the `~/.bashrc` and `/etc/profile`  
  
Then reinitiate the `~/.bashrc` and `/etc/profile` by using `source` command

if :  
`>>>import osgeo.gdal` without any error, Congratulations! :)

********************************************
