# Accessing-jupyter-notebook-

Scenario : Suppose you have large amount of  data (may be TB) is in your working cluster and you want to access and interactively play with your data in your home computer.  xwin is one of the way to open your Jupyter notebook on remote host. However, this kind of connection is quite slow.

Please follow the instructions below to use faster connection.

First of all, you should  install Jupyter notebook in both machines  remote (working station in your Lab) and local (your home computer)


Make sure you are connected with UH network or try to connect with VPN with your cougarnet credentials 

open the terminal in your remote machine and just type:

jupyter notebook --no-browser --port=8889

# you should leave the this open

In your local computer, open MS-DOS cmd (if using Windows) or Unix terminal, then type:

ssh -N -f -L localhost:8888:localhost:8889 cougar_username@your_remote_host_name

# make sure to change `cougar_username` to your real username in remote host
# change `your_remote_host_name` to your address of your working station
# Example: ssh -N -f -L localhost:8888:localhost:8889 aawasth3@csip_address



Now open web browser (google chrome, firefox, ...) and type:

localhost:8888
# you will see your notebooks in your given directory
Snapshot on your home computer


Try to open notebook

 Your data (may be TB) is in your working cluster. You want to access and interactively play with your datayour home computer. You can use xwin to open your Jupyter notebook on remote host. However, this kind of connection is quite slow.
