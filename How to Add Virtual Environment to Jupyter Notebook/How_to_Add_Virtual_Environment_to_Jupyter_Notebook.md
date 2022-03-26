# How to Add Virtual Environment to Jupyter Notebook
## Step by step guide to add your virtual environment to jupyter notebook

# 1. Create Conda Virtual Environment
Select appropriate python version for your code and install it using following code:

```
conda create --name venv python=3.8
```

# 2. Activate Virtual Environment Recently Created

```
conda activate venv 
```

# 3. Install Ipykernel Using pip

```
pip install ipykernel
```

# 4. Add Active Virtual Environment to Jupyter Notebook
This piece of code will add active virtual environment to the jupyter. It don't need to be the same with virtual environment's name.

```
ipython kernel install --user --name=venv 
```

From now on virtual environment should be visible on jupyter notebook

# List Conda Virtual Environments

```
conda env list
```

# Delete Virtual Environment

```
conda env remove --name venv
```

# All Together
Here you can see all lines together

```
conda create --name venv python=3.8
conda activate venv 
pip install ipykernel
ipython kernel install --user --name=venv
conda env list
conda env remove --name venv
```


you can find this article also on my medium page:

[https://medium.com/@necocyln/how-to-add-virtual-environment-to-jupyter-notebook-8c338ba11d16](https://medium.com/@necocyln/how-to-add-virtual-environment-to-jupyter-notebook-8c338ba11d16)


and also on my blog:

[https://www.necmettinceylan.com/blog/2022/3/26/how-to-add-virtual-environment-to-jupyter-notebook/](https://www.necmettinceylan.com/blog/2022/3/26/how-to-add-virtual-environment-to-jupyter-notebook/)



<!--- tags: jupyter notebook -->
