# Day 3
Introduction for Machine Learning and Deep Learning tools in python

Before starting, make sure you have cloned this repository locally and are working from your local copy:

```bash
git clone <repository-url>
cd evolve-python-hybrid-course
```

If you already have it cloned, make sure to pull the latest changes:

```bash
git pull
```

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