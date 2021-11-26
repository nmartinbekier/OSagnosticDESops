# Sage installation in MacOS Big Sur (11.6.1), on a MacBook Air (2017)

## First installation: SageMath 9.4 with MacOS binaries
he first time I just downloaded the .dmg binaries for SageMath-9.4 (https://github.com/3-manifolds/Sage_macOS/releases), as I didn't find a 9.1 installer. I used this one for a while, while I got the grip on sage.

## Second installation: SageMath 9.1 with conda, in its own environment
For using conda, I initially installed Anaconda Navigator (https://docs.anaconda.com/anaconda/navigator/index.html) to be able to manage more easily different environments and conda packages. I installed it through the Graphical Installer (https://www.anaconda.com/products/individual#macos , 515MB). It was useful at first specially to explore recommended applications and IDEs (JupyterLab and Spyder specially), and to see and create different test environments. Shortly after the GUI stopped being useful, as it is very slow, and when there where problems testing packages (which was frequently), it didn't show the errors or warnings.

After this, I started using directly conda from the terminal.

In particular, I installed sage from the conda-forge channel, as shown in https://doc.sagemath.org/html/en/installation/conda.html , through the sequence:
* conda config --add channels conda-forge ## Adding the channel
* conda config --set channel_priority strict ## Changing the channel priority
* conda create -n sage sage=9.1

From what I remember, I think I had to specify python 3.7 for it to work:
* conda create -n sage sage=9.1 python=3.7

Having it in its own environment was useful to continue playing with other packages without affecting the sage installation. Specially after starting the course of Statistical Machine Learning, where we also work with jupyter notebooks, and with packages such as scikit-learn, pandas, scipy, seaborn, and others.

## Third installation: SageMath 9.2 with conda
To play with some IDEs, such as the latest versions of Spyder and Jupyterlab, they required python 3.8. Since sage 9.1 doesn't support python 3.7 but sage 9.2 does, I installed sage 9.2.

Now I use sage mainly through Jupyterlab, in the sage environment
* conda activate sage
* sage -n jupyterlab

Although the integrated debugger and variable explorer doesn't work with the sage kernel, I find it nicer to work there than in jupyter notebooks, among others because of easier contextual documentation, short description of methods and method parameters, and for using a dark theme (so much white burns my eyes ;) .

I also installed scikit-learn and other packages in this environment without problem
* conda install scikit-learn
* conda install scipy
* conda install pandas
* ...etc...
 

# OSagnosticDESops

This is a repository for instructions on how to do Operating System Agnostic Data Engineering Science Operations

## Problem 0, Individual Assignment 3

Please do the following STEPS to document your installation of SageMath on your laptop's and/or desktop's operating system(s):

1. STEP 0: Get a Github Account at https:/github.com if you do not already have one and install git on your laptop by following this [Quickstart](https://docs.github.com/en/get-started/quickstart) with these two minimal steps:
    - [Hello World](https://docs.github.com/en/get-started/quickstart/hello-world)
    - [Set up Git](https://docs.github.com/en/get-started/quickstart/set-up-git)
2. STEP 1: fork **this** GitHub repository: [https://github.com/datascience-intro/OSagnosticDESops](https://github.com/datascience-intro/OSagnosticDESops) 
    - the easiest way is to login to your GitHUb account and go to the above URL, 
    - click the 'fork' button from the web browser [as shown here](images/fork00.png),
    - choose your GitHub username where you want the fork of OSagnosticDESops repository to go to [as shown here](images/fork01.png),
    - now you should be able to see your fork of the repository at `https://github.com/yourGitHubUsername/OSagnosticDESops/` [as shown here](images/fork02.png),
    - go to `Code` and chose one of the methods (SSH is recommended; HTTPS or CLI are also ok; see [connect with SSH](https://docs.github.com/en/enterprise-server@3.0/authentication/connecting-to-github-with-ssh) for the setup instructions) [as shown here](images/fork03.png),
    - finally you can go into the appropriate directory in your local machine (laptop/desktop) and clone your fork of the repository [as shown here](images/fork04_cloneYourForkLocally.png),
    - you can stay up to date with the upstream [https://github.com/datascience-intro/OSagnosticDESops](https://github.com/datascience-intro/OSagnosticDESops) [as showh here](images/fork05_fetchAndMetgeUpstream.png) and commit and push your own changes by taking a brief tour of [git](https://en.wikipedia.org/wiki/Git) and completing other steps in [Quickstart](https://docs.github.com/en/get-started/quickstart).
3. STEP 2: You main task is to document the steps you took to install SageMath the easy way from binaries or the harder way from source on your local machine, by following the guidelines in:
    - [https://github.com/datascience-intro/how2_MacOSX_2SageMath-2021](https://github.com/datascience-intro/how2_MacOSX_2SageMath-2021)
    - [https://github.com/datascience-intro/how2_WindowsOS10-\_2SageMath-2021](https://github.com/datascience-intro/how2_WindowsOS10-_2SageMath-2021)
    - You may either document using markdown by editing this `README.md` file in your fork of this repository by simply writing down the steps you took to install SageMath
    - Or give a URL to another repository that documents your installation steps in detail
    - The main expectation is that you should be able to install SageMath on your local machine a lot faster by following the instructions you have given
 
Further instructions, if needed, will follow shortly after the computer labs in Angstrom are tested. Please discuss in threads at the course instructure page so you can learn from one another.
