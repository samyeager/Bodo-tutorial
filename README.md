# Bodo Tutorial
Welcome to Bodo Tutorials!

First make sure you have Bodo [installed](http://docs.bodo.ai/latest/source/install.html).

To view tutorials with Jupyter Notebook, install `jupyter` and `ipyparallel` in the same enviroment where Bodo is installed:

    # if you followed the above installation instructions, 
    # make sure you are in the same enviroment: source activate Bodo 
    conda install jupyter ipyparallel -c conda-forge

Create an MPI profile for IPython:

    ipython profile create --parallel --profile=mpi

Edit the `~/.ipython/profile_mpi/ipython_config.py` file
and add the following line:

    c.IPClusterEngines.engine_launcher_class = 'MPIEngineSetLauncher'

Now go to `Bodo-tutorial` and start the Jupyter Notebook:

    cd Bodo-tutorial
    jupyter notebook

Then go to *IPython Clusters* tab. Select the
number of engines (i.e., cores) you'd like to use and click *Start* next to the
*mpi* profile. Alternatively, you can use `ipcluster start -n 4 --profile=mpi`
in a terminal to start the engines (this can take several seconds).

Start with [`bodo_getting_started.ipynb`](https://github.com/Bodo-inc/Bodo-tutorial/blob/master/bodo_getting_started.ipynb) 
and then move on to [`bodo_tutorial.ipynb`](https://github.com/Bodo-inc/Bodo-tutorial/blob/master/bodo_tutorial.ipynb).

_________________________
More documentation can be found at http://docs.bodo.ai.

More Jupyter Notebook setup instructions for Bodo can be found [here](http://docs.bodo.ai/latest/source/jupyter.html).
