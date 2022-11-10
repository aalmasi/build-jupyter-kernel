# build-jupyter-kernel
Instructions to build a new Jupyter notebook kernel based on a conda environment


## Manipulating existing kernels
To list all existing Jupyter kernels do the following in the Anaconda CLI.
```
jupyter kernelspec list
```

To remove an existing Jupyter kernel <kernel_name> type in the following in the Anaconda CLI.
```
jupyter kernelspec remove <kernel_name>
```

## Manipulating conda environments
To get a list of all existing conda environments, type in the following into the Anaconda CLI.
```
conda env list
```

To get information about an existing conda package, type in the following into the Anaconda CLI.
```
conda search <package_name> --info
```

To create a new conda environment, type in the following in the Anaconda CLI.
```
conda create --name <env_name> 
```

To remove an existing conda environment, type in the following into the Anaconda CLI.
```
conda env remove --name <env_name>
```

## Instructions to create a python kernel to use in Jupyter notebook using a new conda environments:
1. Create a new conda environment (e.g. `new-env`) to host your kernel.
1. Install ipykernel, if you have not done so already:
```
(new-env)$ conda install ipykernel
```
1. Register the new kernel spec with Jupyter 
```
(new-env)$ ipython kernel install --user --name=new-env
```
