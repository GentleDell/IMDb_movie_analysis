# How to Invest in Movies
**Authors:** [Shengzhao Xia](https://github.com/SXiaZr), [Yinan Zhang](https://github.com/yinanzhangepfl), [Yu-Ting Huang](https://github.com/yuyuvalerie), [Zhantao Deng](https://github.com/GentleDell) 

**Report**: [How to Invest in Movies]()

## Abstract


## 1. Prerequisites
This project is based on [Python](https://www.python.org/) and we use [Spyder](https://www.spyder-ide.org/) as our python programming environment. We also provide `.ipynb` files for [Jupyter notebook](https://jupyter.org/). These softwares can be installed together with [Anaconda](https://www.anaconda.com/). In addition, We install all packages through the Anaconda Prompt. These packages have been tested in **Window 10 Home** and **macOS Mojave**, but it should be easy to implement in other platforms. 

### Anaconda
This project is based on anaconda and jupiter notebook. Download and install instructions can be found at: https://www.anaconda.com/download/. After installing Anaconda, `pip` and `conda` can be used to install Python packages. Spyder will also be installed together with 

### Scipy
We use the scientific computing and visualization functionalities of [scipy](https://www.scipy.org/install.html), especially the numpy, pandas and matplotlib package. These packages can be installed by typing the following command in your Anaconda Prompt.
```
python -m pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose
```

### Networkx
We use [networkx](http://networkx.github.io) to visualize signals and graph structure. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install networkx
```

### NLTK
We use [NLTK](https://www.nltk.org/) to analyze the keywords of each movie. The package can be installed by typing the following command in your Anaconda Prompt.
```
pip install -U nltk
```

## 2. Research questions
In this project we have figured out:
- What factors are important for the ROI (Return on Investment) of a specific genre?
- How to predict the ROI of a new movie with some prior features, e.g. budget and production companies ?

## 3. Dataset
### Original Dataset:
We use the dataset on [Kaggle](https://www.kaggle.com/tmdb/tmdb-movie-metadata). It contains two csv files: 
- `tmdb_5000_credits.csv` (~ 38.1MB): 

The dataset contains the cast and crew data of 4803 movies. The cast feature mainly depicts what actors appear in the movie and what characters they star. So as the crew data, which descibles the names and jobs of specific crews. 
- `tmdb_5000_movies.csv` (~ 5.43MB): 

The dataset contains 4803 movies data with 20 distinct features. The important features that we are interested: budget, genres ,keywords, title, popularity, production_companies, revenue, vote_average.



## 4. What we have done
### Auxiliary modules:
- `Lib_gradientdecent.py`: Contain gradient decent algorithms of ridge regression and lasso regression.
- `Lib_graph.py`: Contain functions of constructing all subgraphs.
- `Lib_keywords.py`: Contain fuctions grouping keywords by word roots and synonym and training a word2vec model.
- `Lib_prediction.py`: Contain functions to predict return of investment according movie network.
- `Lib_vis.py`: Contain all kinds of visualization functions. 

### Working modules:
- `Project_IMDb.py`: Python interface. A pipeline to run whole codes of our project from data exploration, feature preprocessing to movie network construction and prediction.  
- `Project_IMDb.jpynb`: Jupyter notebook interface to run our project.


## 5. Contributions of group members
**Shengzhao Xia:**
- Actor/ress social network analysis
- Genre and keyword subgraphs
- Reports

**Yinan Zhang:**
- NLTK based keywords analysis and processing 
- Actor/ress and director subgraphs
- Reports

**Yu-Ting Huang:**
- Budget and popularity subgraphs
- ROI (Return on Investment) signal
- Gradient descent and reports

**Zhantao Deng:**
- Ridge regression, LASSO and their gradient decent
- Average vote and production companies subgraphs
- Reports
