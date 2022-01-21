# Usual Way of Accessing Jupyter Notebooks
* Access ‘Anaconda Navigator’
* Find the ‘Jupyter’ icon
* Click ‘launch’

However this might not work, and you find the following errors on your terminal and browser respectively:

![Anaconda] (/home/nduta/Documents/My Projects/Jupyter_Notebook_Cheatsheet/Anaconda.png)


Why is this happening?
You are most likely using a browser installed using snap, like Chromium. 
Since Chromium is installed using snap, it cannot open the HTML file used by Jupyter on the browser, as it is a hidden file. 
In recent snap versions, applications installed with snap cannot by default open files in hidden folders (which is the case with the .jupyter folder)
Here is what to do:
Create a Jupyter folder and notebook configuration file
jupyter notebook --generate-config

[Created hidden folder] = /home/nduta/.jupyter
[File in folder] = (a default config file)

If we run ls -a while at /home/<your username on your computer>, we’ll find the hidden Jupyter folder, .jupyter

cd .jupyter
ls -a

We find the following files and hidden folders
.  ..  jupyter_notebook_config.json  
jupyter_notebook_config.py  
migrated  
nbconfig

Access the Jupyter Notebook Server from the Chromium Browser
You’ll need to set up a password. 
To do this, type jupyter notebook password on the terminal and enter. (you can also use this to reset a lost password or change your password)


Create a password and enter.
Retype the same password to verify it and enter.
You should see the following:

Go to http:127.0.0.1:8888
The following window should open:


Enter the password you just created on your terminal and click ‘login’.
If the 8888 port is in use, you will not have access to jupyter notebooks

To check the URLs of running servers, run jupyter notebook on the terminal.
If the 8888 port is in use, you will be notified that jupyter notebook is trying another port.

You will also see any other ports currently in use.

You will also see the current port jupyter notebooks is running on, for example, http://localhost:8891/
Click on the current port’s link or go to the current server, http:127.0.0.1:8891/
You can then enter your password and login.
You should now have access to your Jupyter Notebooks.
