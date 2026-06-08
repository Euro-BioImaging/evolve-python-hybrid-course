# Day 2: Intro to BioImage Analysis with Python for Life Scientists - A distributed in-person training course

## Relevant links:

Course [materials website](https://iah-public.pages.pasteur.fr/20241008_remote_python_bioimage_analysis_course_day2).

Course [materials repository](https://gitlab.pasteur.fr/iah-public/20241008_remote_python_bioimage_analysis_course_day2).

Euro-BioImaging course [website](https://www.eurobioimaging.eu/events/intro-to-bioimage-analysis-with-python-for-life-scientists-a-distributed-in-person-training-course/)

## Course structure

- Day 1 - June 23rd: Intro to Jupyter notebooks and python, introduction to loading images and microscopy metadata, basics of visualisation
- **Day 2 - June 24th: Practical image processing with Python: segmentation, denoising, morphology and automation of analysis pipelines.**
- Day 3 - June 24th: Novel strategies for segmentation: Machine learning + use of pre-trained models from the Bioimage Model Zoo.

### Day 2
Classical (as opposed to AI fueled) image processing and image analysis. Use it to motivate the edition of a complete analysis script. Base afternoon on a biological application.

Morning (10:00-13:00 CET, 9-12 UK time)

- Image basics
- data types
- 2d/3d
- Image normalisation

Segmentation
- Difference between semantic and instance segmentation
- Connected components, watershed
- Spot detection
- Filtering
- Basic things to do with a segmentation
- Cell boundaries
- Find cell neighbours
- E.g. manipulating masks to extract neighbourhoods to extract ratios

Afternoon (14:00-17:00 CET, 13:00-16:00 UK time)

- Feature extraction
- Regionprops
- Explain different features / when they're useful

Building a workflow / pipeline
- Assembling steps into functions
- Batch processing / loops
- Exporting features in tables
- Visualising analysis results
- seaborn plots


## This repository

This repository contains the teaching materials for Day 2 of the course: [Intro to BioImage Analysis with Python for Life Scientists - A distributed in-person training course](https://www.eurobioimaging.eu/events/intro-to-bioimage-analysis-with-python-for-life-scientists-a-distributed-in-person-training-course/).

This repository contains a set of Jupyter notebooks to learn how to do basic image processing using Python and the scientific packages Numpy, scikit-image, Matplotlib and Pandas.

## Installation instructions for practical

Follow the instructions provided [here](https://iah-public.pages.pasteur.fr/20241008_remote_python_bioimage_analysis_course_day2/README.html) to [download](book/download_repo.md) the course material, [set up](book/setup_environment.md) a python environment and [launch](book/launch_notebooks.md) the notebooks provided in this repository.

## Acknowledgements / Copyright

A large part of the material for this course has been taken and adapted from
[this](https://github.com/guiwitz/PyImageCourse_beginner) [![DOI](https://zenodo.org/badge/173477371.svg)](https://zenodo.org/badge/latestdoi/173477371)  (notebooks), created by [Guillaume Witz](https://twitter.com/guiwitz). 
Some images and material are taken from [this](https://bioimagebook.github.io/index.html) nice introduction to bioimage analysis course. Some topics were also inspired by [this](https://haesleinhuepf.github.io/BioImageAnalysisNotebooks/intro.html) nice repository where you can also find more advanced material.

Thank you for making this teaching material available to the community!

Installation instructions have been taken and adapted from the [Open Image Data Handbook](https://kevinyamauchi.github.io/open-image-data/intro.html) by [Kevin Yamauchi](https://kevinyamauchi.github.io/). Thanks!


## Data

In this course, we are trying to reproduce a workflow used in other contexts, in particular Fiji, so that you can compare different approaches. For example you can check the excellent introduction to Fiji Macro programming by Anna Klemm [here](https://github.com/ahklemm/ImageJMacro_Introduction). We use images from the [Cell Atlas](https://www.proteinatlas.org/humanproteome/cell) of the Human Protein Atlas (HPA) project where a large collection of proteins have been tagged and imaged to determine their cellular location. Specifically, we downloaded a series of [images](images) from the Atlas, with some cells showing nucleoplasm localization and some nuclear membrane localization. The idea of the workflow is to compare the signal within the nucleus with that on its edge to determine for each image whether the protein is membrane bound or not.

The images in the [images](images) folder all come from the [Cell Atlas](https://www.proteinatlas.org/humanproteome/cell). For more information see the publication of Thul PJ et al., A subcellular map of the human proteome. **Science**. (2017) DOI: [10.1126/science.aal3321](https://doi.org/10.1126/science.aal3321). All images are covered by a [Creative Commons Attribution-ShareAlike 3.0 International License](https://creativecommons.org/licenses/by-sa/3.0/).

All images were downloaded directly from the HPA website using the same link construction and saved as tif files. For example the image [8346_22_C1_1.tif](images/8346_22_C1_1.tif) was downloaded using the link
https://images.proteinatlas.org/8346/22_C1_1_blue_red_green.jpg.
