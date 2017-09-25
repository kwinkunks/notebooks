# Remote Jupyter

Easily run Jupyter Notebook on an EC2 (say), and connect to a localhost port on your local machine.

## `ssh` into the remote

We will use `localhost:8888` on the local machine, and `8889` on the remote. On your local machine (using your own public DNS):

    ssh -i ~/.ssh/mykey.pem -L localhost:8888:localhost:8889 ubuntu@12-34-56-78.compute-1.amazonaws.com
    
This is going to open port 8888 locally to SSH traffic from port 8889 on the remote.

Note that this won't work if port `8888` on your local is already bound to some other service. If it fails, change it to some other number, eg `8899`.

Adding the flag `-N -f` will provide a non-interactive session that goes into the background. Handy for when you're already connected in a terminal.

## Get ready on the remote machine

- Set up the remote machine, as usual. Install Anaconda (go here and get the link to the latest version):

    wget https://repo.continuum.io/archive/Anaconda3-4.4.0-Linux-x86_64.sh
    bash ./Anaconda3-4.4.0-Linux-x86_64.sh
    
- Create your environment:

    conda create -n myenv anaconda
    source activate myenv

- Install anything else you need.

## Get things ready on the local machine

- Start Jupyter, e.g. on port 8889 (default is 8888, I just changed it to illustrate):

    jupyter notebook --no-browser --port=8889
    
Copy the link and paste it into your browser. You're done.
