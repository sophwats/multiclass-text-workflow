# Multi-class classification of text data

The notebooks in this repo come together to create a multi-class classification model. The data used is the [Usenet 20 Newsgroups data](https://kdd.ics.uci.edu/databases/20newsgroups/20newsgroups.html), which contains 20,000 articles, each posted to one (or, in a small number of cases, more than one) newsgroup. 


These notebooks aren't intended to produce the optimal classification model. Instead, we hope you learn some approaches and techniques which can be used when dealing with multi-class data and for handling text data.


Notebook [00-eda.ipynb](00-eda.ipynb) explores the raw data. You will only be able to execute the cells in this notebook if you download the data set directly yourself. (It is possible to run through the other notebooks in this repo without running [00-eda.ipynb](00-eda.ipynb).)


Notebook [01-feature-engineering.ipynb](01-feature-engineering.ipynb) transforms the data into feature vectors, using a Hashing Vectoriser and tf-idf transformation. 


Notebooks [02-naive-bayes-model.ipynb](02-naive-bayes-model.ipynb), [02-random-forest-model.ipynb](02-random-forest-model.ipynb), [02-svc-model.ipynb](02-svc-model.ipynb) and [02-xgboost-model.ipynb](02-xgboost-model.ipynb) each train a model. These notebooks will only run if you have run notebook [01-feature-engineering.ipynb](01-feature-engineering.ipynb) fully, since these model notebooks load in the feature engineering pipeline stage. You can try out training as many of these models as you wish, but each model will overwrite the previously trained model - you will only save the last model you trained.


Notebook [03-parameter-tuning.ipynb](03-parameter-tuning.ipynb) loads in the feature engineering pipeline stage and model training pipeline stage from the previous notebooks, and carries out a hyper-parameter sweep to identify a model which gives the _best_ results, for some metric. 


Some of the notebooks contain tick symbols like this one ✅. We use this symbol to indicate that you have reached a part of the notebook where you could play around with the notebook or answer some questions.

### Getting Started

1. Make sure you have Python 3.7 installed, installing it if necessary
    - If you have a favorite package manager, use that 
    - if not, [python.org](https://www.python.org/downloads/) has binaries for many platforms
2. Make sure you have `git` installed, installing it if necessary
    - If you have a favorite package manager, use that
    - if not, [git-scm.com](https://git-scm.com/downloads) has binaries for many platforms (you won't need a GUI)
3. Install [pipenv](https://docs.pipenv.org/en/latest/)
    - on a Mac, the easiest way is probably `brew install pipenv`
    - on a Fedora Linux machine, the easiest way is probably `dnf install pipenv`
    - on Windows, if you have Python installed already, the easiest way is probably [to use `pip`](https://docs.pipenv.org/en/latest/install/#pragmatic-installation-of-pipenv)  
    
#### Install the notebooks and dependencies

1.  Clone this repository:  `git clone https://github.com/sophwats/multiclass-text-workflow/`
    - tip:  if you don't have `git` installed, you can also [download an archive of this repository](https://github.com/sophwats/multiclass-text-workflow/archive/master.zip)
2.  Change to this repository's directory:  `cd multiclass-text-workflow`
3.  Install the dependencies:  `pipenv install`
4.  Run the notebooks:  `pipenv run jupyter notebook`

### Alternative approach

You can run nearly all of the notebooks on [Binder](https://mybinder.org/v2/gh/sophwats/multiclass-text-workflow/master), without needing to download anything. However, notebook 03-parameter-tuning.ipynb may not have enough resources to run for certain models. 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sophwats/multiclass-text-workflow/master)
