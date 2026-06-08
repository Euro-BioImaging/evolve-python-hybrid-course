# Preparation for "Intro to bioimaging analysis with Python for life scientists" workshop

## Installing conda

1. Install Miniconda by following the installation instructions for your operating system at [this page](https://www.anaconda.com/docs/getting-started/miniconda/install). Choosing the "Graphical installer" option should make it easier, if you're not familiar with using the terminal. 
2. [Windows users only] When prompted, make sure to select "Register Miniconda3 as my default Python 3.13", if not already selected.

   ![Miniconda Webpage](./anaconda_win.jpeg)
   
3. Please check that the installation worked properly by opening the Terminal (MacOS) or Anaconda PowerShell Prompt (Windows) and typing `conda list`. If conda has been installed correctly, a list of installed packages appears.

FAQ: "What should I do if I already have `conda` installed on my machine?"

Please make sure that your `conda` installation is up to date. To do so, run the following command:
```
conda --version
```
If this returns a version older than `23.10.0`, please update your `conda` by running:
```
conda update -n base conda
```
