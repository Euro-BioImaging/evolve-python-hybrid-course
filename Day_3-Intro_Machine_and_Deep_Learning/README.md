# Day 3
Introduction for Machine Learning and Deep Learning tools in python

## Before starting

Make sure you have the course files on your computer:

1. Open the course page in your browser.
2. Click the green **Code** button.
3. Select **Download ZIP**.
4. Unzip the downloaded file.
5. Open the unzipped course folder on your computer.

You also need Miniconda installed before running the notebooks. To check whether it is already installed, open a terminal and run:

```bash
conda --version
```

If this command shows a conda version, you can continue with the course instructions below.

If `conda` is not found, install Miniconda using the guide for your operating system in the `installation/` folder:

- [Windows Miniconda installation guide](installation/anaconda_miniconda_windows_install.md)
- [macOS Miniconda installation guide](installation/anaconda_miniconda_macos_install.md)
- [Linux Miniconda installation guide](installation/anaconda_miniconda_linux_install.md)

After installing Miniconda, close and reopen your terminal, then run `conda --version` again to confirm it works.

## Intro to Machine Learning

### Instructions

1. Open a terminal and navigate to the Day 3 folder:

```bash
cd Day_3-Intro_Machine_and_Deep_Learning
```

2. Activate the course conda environment:

```bash
conda activate pythoncourse
```

If you do not have the environment yet, create it first:

```bash
conda create -n pythoncourse python=3.12
conda activate pythoncourse
```

3. Install JupyterLab and the required packages:

```bash
pip install jupyterlab numpy scipy scikit-image scikit-learn matplotlib pandas
```

4. Launch JupyterLab from the Day 3 folder:

```bash
jupyter lab
```

5. In JupyterLab, open the `notebooks/` folder and run the notebooks in order:

- `1_sklearn_introduction.ipynb`
- `2_sklearn_classification.ipynb`
- `3_OPTIONAL_sklearn_segmentation_filtering.ipynb`

The completed versions are available in `notebooks/solutions/` if you want to compare your work.

## Intro to Deep Learning

### Instructions

> **Data upload to Google Drive**

1. Go to Google Drive. 
2. Log in with your Google account.
3. Click `+ Add` (top-left corner)
4. Select `Folder upload`
5. Pick the folder `training_example` within `data/cellpose_example`
6. Confirm upload

---
> **Run tools/notebooks**

1. Open a terminal and navigate to the Day 3 folder:

```bash
cd Day_3-Intro_Machine_and_Deep_Learning
```

2. Activate the course conda environment:

```bash
conda activate pythoncourse
```

3. Launch JupyterLab from the Day 3 folder:

```bash
jupyter lab
```

4. Follow instructions in notebooks:

- `4_cellpose_deep_learning.ipynb`
- `5_napari_empanada.ipynb`
- `6_bioimage_model_zoo.ipynb`

---

> **Install separate environment if necessary**

1. Create a new environment:

```bash
conda create -y -n dl_tools -c conda-forge python=3.10
```

2. Activate the environment:

```bash
conda activate dl_tools
```

3. Install required packages with pip:

```bash
python -m pip install "napari[all]"==0.6.6 cellpose[gui]==3.1.1.1 empanada-napari
```
