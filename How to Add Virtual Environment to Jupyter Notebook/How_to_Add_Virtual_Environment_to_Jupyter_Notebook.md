# How to Add Virtual Environment to Jupyter Notebook
## Step by step guide to add your virtual environment to jupyter notebook

# 1. Create Conda Virtual Environment
Select appropriate python version for your code and install it using following code:

    conda create --name venv python=3.8

# 2. Activate Virtual Environment Recently Created

    conda activate venv 

# 3. Install Ipykernel Using pip

    pip install ipykernel

# 4. Add Active Virtual Environment to Jupyter Notebook
This piece of code will add active virtual environment to the jupyter. It don't need to be the same with virtual environment's name.

    ipython kernel install --user --name=venv 

From now on virtual environment should be visible on jupyter notebook

# List Conda Virtual Environments

    conda env list

# Delete Virtual Environment


    conda env remove --name venv

# All Together
Here you can see all lines together


    conda create --name venv python=3.8
    conda activate venv 
    pip install ipykernel
    ipython kernel install --user --name=venv
    conda env list
    conda env remove --name venv


You can find this article on my medium page: <br>
[MEDIUM LINK](https://medium.com/@necocyln/how-to-add-virtual-environment-to-jupyter-notebook-8c338ba11d16)


On my blog: <br>
[BLOG LINK](https://www.necmettinceylan.com/blog/2022/3/27/how-to-add-virtual-environment-to-jupyter-notebook/)


On my github repo: <br>
[GITHUB LINK](https://github.com/NecmettinCeylan/Posts/blob/main/How%20to%20Add%20Virtual%20Environment%20to%20Jupyter%20Notebook/How_to_Add_Virtual_Environment_to_Jupyter_Notebook.md)

<!--- tags: jupyter notebook, conda, python, virtual environment -->
