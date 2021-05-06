[![Image](https://isdasoil.s3.amazonaws.com/iSDAsoil_logo.jpg)](https://www.isda-africa.com/isdasoil)

# Introduction

This repository contains iPython notebook tutorials that explain how to access the iSDAsoil data. For more information about isdasoil, visit https://www.isda-africa.com/isdasoil.



# Setup

There are a few different ways to get an iPython notebook up and running. We have created configs for as many options as feasible. You have 2 main options - running a Jupyter Notebook with a cloud provider (e.g. Google or AWS), or running the tutorial locally. 

## Running on a cloud provider
### Option 1: Google colab
Google colab is, a free service operated by Google to host iPython notebooks. The only requirements is a Google account. The advantage of this approach is that all requirements are automatically installed, so you can just open the notebook and get started straight away. Note that because this is a cloud service, any data that is downloaded in code will then need to be downloaded locally, should you wish to access the data on your machine.

To open this tutorial in colab, visit: https://colab.research.google.com/github/iSDA-Africa/isdasoil-tutorial/blob/main/iSDAsoil-tutorial.ipynb. Be sure to run the first cell that installs the `requirements-googlecolab.txt` file.

### Option 2: AWS Sagemaker

Equally as easy to set up, the only requirement is an AWS accout. Follow the link below to set up a hosted Jupyter Notebook on AWS Sagemaker, with all requirements preinstalled. Setup can take a few minutes. Once the notebook is set up, be sure to select the `isdasoil-tutorial` Python kernel. 

https://eu-west-2.console.aws.amazon.com/cloudformation/home?region=eu-west-2#/stacks/quickcreate?templateUrl=https%3A%2F%2Fisdasoil.s3-us-west-2.amazonaws.com%2Fsagemaker-config.yml&stackName=isdasoil-tutorial

## Running locally
### Option 3: conda package manager
- For those needing to run the iPython locally, the easiest way is to use the environment manager [conda](https://docs.conda.io/en/latest/). We've created a conda `environment.yml` config file, with all the requirements already specified. Once conda is installed, it's as simple as running the  command `conda env create -f environment.yml` in the directory where the `environment.yml` file is located.

### Option 4: pip + virtualenv
- The final option is to use pip with a virtual environment. This is the most error prone approach - it requires Python and a number of Python packages to be installed on the system, and also relies on external dependencies such as the correct version of the GDAL library. Run the following commands in the folder where you've downloaded the repo to set up the virtual environment:

```
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```
