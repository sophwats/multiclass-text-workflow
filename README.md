#### Multi-class classification of text data

The notebooks in this repo step through stages of the machine learning workflow in order to create a muli-class classification model. The data used is the [Usenet 20 Newsgroups data](https://kdd.ics.uci.edu/databases/20newsgroups/20newsgroups.html), which contains 20,000 articles, each of which was posted to one (or, in a small number of cases, more than one) NewsGroup. 


These notebooks aren't intended to produce the optimal classification model. Instead, we hope you learn some approaches and considerations for dealing with multi-class data and for handling text data. 


Notebook [00-eda.ipynb](00-eda.ipynb) explores the raw data. You will only be able to execute the cells in this notebook if you download the data set directly yourself. It is possible to run through the other notebook in this repo without running [00-eda.ipynb](00-eda.ipynb). 


Notebook [01-feature-engineering.ipynb](01-feature-engineering.ipynb) transforms the data into feature vectors, using a Hashing Vectoriser and tf-idf transformation. 


Notebooks [02-naive-bayes-model.ipynb](02-naive-bayes-model.ipynb), [02-random-forest-model.ipynb](02-random-forest-model.ipynb), [02-svc-model.ipynb](02-svc-model.ipynb) and [02-xgboost-model.ipynb](02-xgboost-model.ipynb) each train a model. These notebooks require you to have run notebook [01-feature-engineering.ipynb](01-feature-engineering.ipynb) fully, since the model notebooks load in the feature engineering pipeline stage, and use that to transform the data prior to training a model. You can try out as many of these models as you wish, but note that when training multiple models, the model file is overwritten, meaning you only save the latest model you trained.


Notebook [03-parameter-tuning.ipynb](03-parameter-tuning.ipynb) loads in the feature engineering pipeline stage and model training pipeline stage from the previous notebooks, and carries out a hyper-parameter sweep to identify a model which gives 'the best' results, for some metric. 


Some of the notebooks contain tick symbols like this one ✅. We use this symbol to indicate that you have reached a part of the notebook where you should play around or answer some questions. We will make suggestions, such as tuning variables or testing different methods as they arise. 

