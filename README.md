Unified Multimodal Product Classification for Rakuten’s E-Commerce Catalog
==============================

Table of Contents
==================
1. Project Overview
2. Folder Structure
3. Getting Started
4. Prerequisites
5. How to Use
6. Contributing
7. License

Project Overview
================
Rakuten's e-commerce catalog features millions of products that need to be categorized accurately and efficiently. This project aims to build a robust classification system that leverages both textual and visual data for enhanced accuracy.

Key Features:

- Text Model: A DistilBERT-based transformer model for processing product descriptions.
- Image Model: A VGG16-based CNN for extracting visual features from product images.
- Late Fusion Approach: Combines text and image features for final classification.
- Modular Design: Flexible structure for adapting and extending the project.

Folder Structure
=================
The repository follows a modular structure inspired by the cookiecutter data science project template. Below is a brief overview:

------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data               <- Should be in your computer but not on Github (only in .gitignore)
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── RAW DATASET    <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │   ├── Image model    <- contains saved model and labelencoder
    │   └── Text model     <- contains txt file with link for saved model and labelencoder
    │
    ├── notebooks          <- contains Jupyter notebooks for EDA, feature engineering, preprocessing and model file
    │
    ├── references         <- Data dictionaries, manuals, links, and all other explanatory materials.
    │
    ├── reports            <- The reports that you'll make during this project as PDF
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── Image processing.ipynb
    │   │   └── Text_translation.ipynb
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── late_fusion_model.ipynb (predict model)
    │   │   └── DistilBERT_base _uncased_model.ipynb (train_text_model)
    │   │   └── Vgg16_image_model.ipynb (train_image_model)
    │   │
    │   ├── visualization  <- Scripts to create exploratory and results oriented visualizations
    │   │   └── Exploratory analysis.ipynb

--------

Getting Started
===============
1. Clone the repository
2. Create Virtual Environment
3. Install Dependencies

Prerequistes
============
Ensure the following are installed on your machine:

1. Python 3.8 or later
2. Jupyter Notebook or JupyterLab
3. GPU support for training models (optional but recommended)

How to Use
==========
Prepare Data:
Place the raw dataset in the data/RAW DATASET folder.
Use scripts in src/features/ for preprocessing.

Train Models:
Run src/models/DistilBERT_base_uncased_model.ipynb for text-based classification.
Run src/models/Vgg16_image_model.ipynb for image-based classification.

Combine Models:
Use the late fusion approach in src/models/late_fusion_model.ipynb.

Visualize Results:
Explore insights and results using src/visualization/Exploratory analysis.ipynb.

Contributing
============
Contributions are welcome! Please open an issue or submit a pull request if you'd like to suggest improvements or report bugs.

License
=======
This project is licensed under the MIT License. You are free to use, modify, and distribute this project with proper attribution.


<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
