# Accessing-jupyter-notebook-Remotely-

## Why ?????? : 

Sometimes, It is important to execute each line or block of code from large amount of code to visualize the output from each line. But consider your dataset is very large or each line or block of code is highly computationally expensive. Then, running jupyter notebook on the cluster having Multiple processors or GPU will be a good idea.

or 

Suppose you have large amount of  data (may be TB) is in your working cluster and you want to access and interactively play with your data in your home computer.  xwin is one of the way to open your Jupyter notebook on remote host. However, this kind of connection is quite slow.

Please follow the instructions below to use faster connection.

First of all, you should  install Jupyter notebook in both machines  remote (working station in your Lab) and local (your home computer)


Make sure you are connected with UH network or try to connect with VPN with your cougarnet credentials 

You need to ssh to your remote machine using the below command 

ssh courgarnet_username@ip_address_of_your_workstation

Once you are loggen in, Please try to type the below command in the ssh terminal of your remote machine.

jupyter notebook --no-browser --port=8889

## you should leave this window open

# Let's Play with local machine now!!

In your local computer, open MS-DOS cmd (if using Windows) or Unix terminal, then type:

ssh -N -f -L localhost:8888:localhost:8889 cougar_username@your_remote_host_name

## make sure to change `cougar_username` to your real username in remote host
## change `your_remote_host_name` to your ip address of your working station
## Example: ssh -N -f -L localhost:8888:localhost:8889 aawasth3@csip_address


![Screenshot (267)](https://user-images.githubusercontent.com/30754423/140812004-138e48f4-001e-423f-b900-fbe78892838e.png)

Now open web browser (google chrome, firefox, ...) and type:

localhost:8888
## you will see your notebooks in your given directory
Snapshot on your home computer

![Screenshot (268)](https://user-images.githubusercontent.com/30754423/140812101-ab752442-4c3e-43d6-9ace-6207e51887a3.png)

Try to open notebook

 Your data (may be TB) is in your working cluster. You want to access and interactively play with your data in your home computer. You can use xwin to open your Jupyter notebook on remote host. However, this kind of connection is quite slow.
