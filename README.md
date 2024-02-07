# Python Virtual Envirnments

To set up Python in your local development. There are primarily two ways - 

- https://www.python.org/
- https://www.anaconda.com/download


Recommendation is for each application/project that is being done. a new Virtual Env be made.

Example - 

![List of Environments](https://drive.google.com/file/d/1CYLtdb2TKuUuJUAEL3eZXYr-qhTamZwf/view?usp=sharing "List of Environments")


To manage environments - 

Python has a environment manager called - virtual environemnts and a package manager called "pip" (https://pypi.org/)

Anaconda is a popular distribution along with Conda Environments and a package manager called "conda" (https://anaconda.org/anaconda/repo)

If you are starting with Data Analysis/Data Science Experimentation. Anaconda is the goto distribution.



## Installation Instructions


### Vanilla Python Installation

##### Mac

Note : Mac comes with a default installation of Python. It is advisable to install fresh so that you can manage different envs easily
1. Download and Install - https://www.python.org/downloads/macos/
2. Launch Python - 
```python3```

3. Install pip
```python get-pip.py```

##### Ubuntu

1. Execute the following commands for download an install- 
```
sudo apt-get update
sudo apt-get install python3.x
```

2. Launch Python - 
```python3```

3. Install pip
```python get-pip.py```

##### Windows 

1. Download and Install - https://www.python.org/downloads/macos/
2. Add Python to PATH
    * Navigate: Control Panel -> User Accounts -> Change my Environment Variables
    * Inside the top window labeled 'System Variables' select 'Path' and edit it
    * Select 'Browse' and navigate to C:\python311 and select 'ok'
    * Select 'Move Down' and repeat step 3 for C:\python311\Scripts
3. Launch Python from command line - 
```python```

### Anaconda Installation

For anaconda, we have two options - Full anaconda instllation with all most used packages and miniconda, which is a minimal installation with just python and conda package manager. Depending upon your requirement you can start with either.

When installing anaconda a new environment (base) will be created for you that can be used to get started

##### Mac

Note : Mac comes with a default installation of Python. It is advisable to install fresh so that you can manage different envs easily
1. Download and Install - https://www.anaconda.com/download
2. After Instllation. You should be able to see default conda env
(base)
confirm by executing ```conda``` command

##### Ubuntu

1. Download - https://www.anaconda.com/download/
2. ```bash <conda-installer-name>-latest-Linux-x86_64.sh```
3. Next time you launch terminal (base) env will be activated

##### Windows 

1. Download and Install - https://www.anaconda.com/download
2. Add Python to PATH
    * Navigate: Control Panel -> User Accounts -> Change my Environment Variables
    * Inside the top window labeled 'System Variables' select 'Path' and edit it
    * Following entries need to be set -

            C:\Users<>\Anaconda3\Scripts\
            C:\Users<>\Anaconda3\Library\
            C:\Users<>\Anaconda3\Lib\site-packages\

        
3. Base env can be activated with - ```activate base```


## Commands for Creating and Managing Virtual Environments

While we can create empty environments.

To enable re-usabiulity of code.

It is advisable to create an evironment file to install packages from.

For Python Virtual Env. This file is called - "requirements.txt"

For Conda Env. This file is called - "environment.yml"

In python requirements.txt the packages can only be installed from pip

In conda environment.yml the packages can be installed from both conda and pip package manager. Example of both will be included in the Example Directory

environment.yml generally includes the name of the environment as well.


### Conda Envs

All conda Envs are created in the main conda directory as folder. you can browse the same anytime.

#### Create a new empty environment

To Create a new environment with all anaconda default packages.

```conda create -n test_env python=3.x.y```

#### Create a new empty environment

```conda create -n test_env python=3.x.y anaconda```

#### Activate an Environment

```conda activate test_env```

#### Deactivate an Environment

```conda deactivate```

#### Create a new environment from file 

```conda env create -f environment.yml```

#### Update an existing environment from file after changes in the file

```conda env update -f environment.yml --prune```

Note: sometimes pip installed packages are not pruned. Please check when doing this.

#### install packages
 ```conda install [PACKAGE_NAME]```

#### get list of environments 

```conda info -e```

#### Get a list of all the packages installed in your current active environment	
 ```conda list```

#### Export your current active environment to a YAML file called environment 
```conda env export > environment.yaml```


## Virtual Env

Each Virtual Env is created in the folder where the command is executed.

##### To create a virtual environment in the virtual_env folder:

```python -m venv virtual_env```

##### To activate the virtual environment

```source virtual_env/bin/activate```

##### To deactivate the virtual environment just type

```deactivate```

##### Installing packages
```pip install [PACKAGE_NAME]```

##### Export package list

```pip freeze > requirements.txt```