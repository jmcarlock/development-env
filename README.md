# Data Science Environment

Creates a VM using for development of data science tools. Installs Zeppelin for
notebooks with Spark/Scala, Jupyter notebooks using pySpark and Python 3.

## Usage

Clone the repo.

Starting the VM:
```bash
$ vagrant up
$ vagrant ssh
```

For Zeppelin notebooks
```
$ zeppelin/bin/zeppelin-daemon.sh start
```

For Jupyter notebooks ([http://localhost:8888/](http://localhost:8888/)):
```
$ jupyter notebook
```

For Jupyter notebooks with Pyspark ([http://localhost:8888/](http://localhost:8888/)):
```bash
$ pyspark
```

Launching TensorBoard ([http://localhost:6006/](http://localhost:6006/)):
```bash
$ tensorboard --logdir path/to/tf_logs/
```

Launching a Bokeh server application ([http://localhost:5006/](http://localhost:6006/)):
```bash
$ bokeh serve path/to/application/
```

## Python libraries

| Package          | Link                                                                     | Usage                       |
|------------------|--------------------------------------------------------------------------|-----------------------------|
| cython           | [cython](http://cython.org/)                                             | Python C extensions         |
| jupyter          | [Jupyter](http://jupyter.org/)                                           | Python/Pyspark Notebooks    |
| numpy            | [NumPy](http://www.numpy.org/)                                           | Data Manipulation           |
| pandas           | [Pandas](http://pandas.pydata.org/)                                      | Data Manipulation           |
| pretty-pandas    | [PrettyPandas](https://github.com/HHammond/PrettyPandas)                 | Data Display                |
| pandas-profiling | [pandas-profiling](https://github.com/pandas-profiling/pandas-profiling) | Data Description            |
| dora             | [Dora](https://github.com/NathanEpstein/Dora)                            | Data Exploration            |
| scikit-learn     | [Scikit-learn](http://scikit-learn.org/)                                 | Machine Learning            |
| annoy            | [annoy](https://github.com/spotify/annoy)                                | Efficient k-NN              |
| imblearn         | [imbalanced-learn](http://contrib.scikit-learn.org/imbalanced-learn/)    | Class Resampling            |
| pomegranate      | [pomegranate](https://pomegranate.readthedocs.io/en/latest/)             | Probabilistic Models        |
| edward           | [Edward](http://edwardlib.org/)                                          | Probabilistic Models        |
| modal            | [modAL](https://cosmic-cortex.github.io/modAL/)                          | Active Learning             |
| snorkel          | [Snorkel](https://hazyresearch.github.io/snorkel/)                       | Data Programming            |
| tdigest          | [tdigest](https://github.com/CamDavidsonPilon/tdigest)                   | Online Quantiles            |
| keras            | [Keras](https://keras.io/)                                               | Deep Learning               |
| tensorflow       | [TensorFlow/TensorBoard](https://www.tensorflow.org/)                    | Deep Learning               |
| darkon           | [DARKON](http://darkon.io/)                                              | Deep Learning Hacking       |
| pytorch          | [pyTorch](http://pytorch.org/)                                           | Deep Learning               |
| dynet            | [dynet](https://github.com/clab/dynet)                                   | Deep Learning               |
| scikit-surprise  | [scikit-surprise](http://surpriselib.com/)                               | Association Learning        |
| bokeh            | [Bokeh/Bokeh Server](http://bokeh.pydata.org/en/latest/)                 | Visualization               |
| matplotlib       | [Matplotlib](https://matplotlib.org/)                                    | Visualization               |
| folium           | [Folium](https://github.com/python-visualization/folium)                 | Visualization               |
| seaborn          | [seaborn](https://seaborn.pydata.org/)                                   | Visualization               |
| colorcet         | [ColorCet](https://bokeh.github.io/colorcet/)                            | Visualization               |
| wordcloud        | [WordCloud](https://github.com/amueller/word_cloud)                      | Visualization (NLP)         |
| gensim           | [gensim](https://radimrehurek.com/gensim/)                               | NLP                         |
| spacy            | [spaCy](https://spacy.io/)                                               | NLP                         |
| textacy          | [textacy](https://github.com/chartbeat-labs/textacy)                     | NLP                         |
| nltk             | [NLTK](http://www.nltk.org/)                                             | NLP                         |
| textblob         | [TextBlob](https://textblob.readthedocs.io/en/dev/)                      | NLP                         |
| stop_words       | [stop_words](https://pypi.python.org/pypi/stop-words)                    | NLP                         |
| langid           | [LangID](https://pypi.python.org/pypi/langid)                            | NLP                         |
| bs4              | [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) | Text Extraction             |
<!-- | textract         | [textract](https://textract.readthedocs.io/en/stable/)                   | Text Extraction             | -->
| statsmodels      | [StatsModels](http://www.statsmodels.org/stable/index.html)              | Statistics                  |
| pymc3            | [PyMC3](http://pymc-devs.github.io/pymc3/)                               | Bayesian Statistics         |
| pystan           | [PyStan](http://pystan.readthedocs.io/)                                  | Bayesian Statistics         |
| prophet          | [Prophet](https://github.com/facebookincubator/prophet)                  | Time Series Prediction      |
| networkx         | [NetworkX](https://networkx.github.io/)                                  | Network Analysis            |
| tweepy           | [tweepy](https://github.com/tweepy/tweepy)                               | Twitter API tool            |
| sympy            | [sympy](http://www.sympy.org/en/index.html)                              | Symbolic Mathematics        |
| autograd         | [autograd](https://github.com/HIPS/autograd)                             | Automatic Differentiation   |
| sacred           | [sacred](https://github.com/IDSIA/sacred)                                | Experimentation             |
| elasticsearch    | [elasticsearch](https://github.com/elastic/elasticsearch-py)             | ES Connector                |
| prospector       | [prospector](https://prospector.landscape.io/en/master/)                 | Static Code Analysis        |
| optml            | [OptML](https://github.com/johannespetrat/OptML)                         | Hyperparameter Optimization |
| ftfy             | [ftfy](https://github.com/LuminosoInsight/python-ftfy)                   | Unicode Cleaning            |
| beautifier       | [beautifier](https://github.com/labtocat/beautifier)                     | Cleans URLs                 |
| scrubadub        | [scrubadub](http://scrubadub.readthedocs.io/en/stable/)                  | Data Anonymization          |
| bandits          | [bandits](https://github.com/bgalbraith/bandits)                         | Multi-Armed Bandits         |
| datasketch       | [datasketch](https://github.com/ekzhu/datasketch)                        | Text Search                 |


## Notes

- If notebooks are not running properly: `sudo chown -R vagrant: ~/.local/share/jupyter`
