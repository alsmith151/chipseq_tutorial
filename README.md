# ChIP-seq Tutorial

Very quick ChIP-seq processing tutorial.

## Running the tutorial

### Install conda

In order to standardise the enviroment I've made a conda enviroment. First install conda in your /t1-data directory:

```
cd /t1-data/user/USERNAME/
mkdir software/
cd software/
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
```

*Note* You will need to log in and out again for conda to work correctly

### (Optional) Install Mamba to speed up creating conda environments
```
conda install mamba -y
```


Follow the installation instructions.

### Clone the repo

```
# Clone
git clone https://github.com/alsmith151/chipseq_tutorial.git

# Enter
cd chipseq_tutorial/
```

### Create conda enviroment

Re-create the conda enviroment that I've generated.

```
# Create env
mamba env create -f chip.yml

# Activate the enviroment
conda activate chip
```

### Load the tutorial notebook

##### If running the above commands connected by RDP to the cluser:

```
jupyter lab

```

A browser window should open up with the notebook.


#### If using SSH from a terminal: 

```
#Connect to server with port forwarding
ssh USERNAME@cbrglogin1.molbiol.ox.ac.uk -L 8002:127.0.0.1:PORT_NUMBER

# Navigate to the cloned repo
cd PATH_TO_REPO

# Start the notebook server on the cluster
echo 'Set jl port to 8002'; jupyter lab --port PORT_NUMBER --no-browser
```

To connect to the notebook and run the tutorial, in your browser go to:
localhost:8002

You will also need the token to access the notebook. You can find this in the terminal window where you activated the notebook server. It looks something like this:
a0c23c3a7fbd0f90ca5cf6500df6c1f01129b0739de60453

Find it at the end of the url, e.g.
http://localhost:8889/lab?token=a0c23c3a7fbd0f90ca5cf6500df6c1f01129b0739de60453








