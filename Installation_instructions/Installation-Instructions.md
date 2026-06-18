# Preparation for "Intro to bioimaging analysis with Python for life scientists" workshop

## Minimal installation to get started

Before starting the course, you need to install **Miniforge** and create a Python environment with Jupyter Lab.

This is a minimal setup to get us started. Later in the course, we will include a more detailed section explaining installations, environments, kernels, and package management.

### 1. Download and install Miniforge

Download **Miniforge** from the official conda-forge download page:

[Download Miniforge](https://conda-forge.org/download/)

Choose the installer for your operating system:

- Windows
- macOS
- Linux

Run the installer and follow the installation instructions.

After installation, open the **Miniforge Prompt**.

On Windows, you can search for **Miniforge Prompt** in the Start menu.

On macOS or Linux, open a terminal.

### 2. Create a new environment

In the Miniforge Prompt or terminal, create a new environment called `my-env` with Python 3.10 and the basic Jupyter packages:

```bash
conda create -n my-env python=3.10 jupyterlab ipykernel ipython
```

When asked to proceed, type:

```bash
y
```

and press Enter.

### 3. Activate the environment

Activate the environment with:

```bash
conda activate my-env
```

You should now see the environment name at the beginning of your prompt, for example:

```bash
(my-env)
```

### 4. Start Jupyter Lab

Start Jupyter Lab by running:

```bash
jupyter lab
```

A new window or tab should open in your web browser showing the Jupyter Lab interface.

You are now ready to start working with notebooks.

## Alternative option: Installing Miniconda instead of Miniforge

The instructions above use **Miniforge**, which is the recommended option for this workshop. The section below provides an alternative way to install `conda` using **Miniconda**.

You only need to install **one** of these options: either **Miniforge** or **Miniconda**. After you have a working `conda` installation, you can create and activate the `my-env` environment using the commands above.

## Installing conda

1. Install Miniconda by following the installation instructions for your operating system at [this page](https://www.anaconda.com/docs/getting-started/miniconda/install). Choosing the "Graphical installer" option should make it easier, if you're not familiar with using the terminal. 
2. [Windows users only] When prompted, make sure to select "Register Miniconda3 as my default Python 3.13", if not already selected.

   Note: the Python version shown by the installer may differ from the one used in this course. For the workshop, we will create a separate environment with `python=3.10` using the commands above.

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