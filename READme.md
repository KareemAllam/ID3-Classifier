# Decision Tree using Python
python implementation of [id3 classification trees](https://en.wikipedia.org/wiki/ID3_algorithm). id3 is a machine learning algorithm for building classification trees developed by Ross Quinlan in/around 1986.

The algorithm is a greedy, recursive algorithm that partitions a data set on the attribute that maximizes information gain. The information gain of attribute A is defined as the difference between the entropy of a data set S and the size weighted average entropy for sub datasets S' of S when split on attribute A. 

This implementation was informed by [Dr. Lutz Hamel's](http://homepage.cs.uri.edu/faculty/hamel/) notes [here](http://homepage.cs.uri.edu/faculty/hamel/courses/2016/spring2016/csc581/lecture-notes/32-decision-trees.pdf). A widely cited text on decision trees is [Machine Learning, by Tim Mitchell](https://www.amazon.com/Machine-Learning-Tom-M-Mitchell/dp/0070428077), you can find pages relevant to id3 [here](http://www.cs.princeton.edu/courses/archive/spr07/cos424/papers/mitchell-dectrees.pdf).

There are also some readable notes on information gain from University of Washington [here](https://courses.cs.washington.edu/courses/cse455/10au/notes/InfoGain.pdf).

## Running the code
Run the code with the python interpreter: 

```python id3.py ./resources/<config.cfg>```

Where config.cfg is a plain text configuration file. The format of the config file is a python abstract syntax tree representing a dict with the following fields:

``
{
   'data_file' : '\\resources\\tennis.csv',
   'data_project_columns' : ['Outlook', 'Temperature', 'Humidity', 'Windy', 'PlayTennis'],
   'target_attribute' : 'PlayTennis'
}
``

You have to specify:
 + relative path to the csv data_file
 + which columns to project from the file (useful if you have a large input file, and are only interested in a subset of columns)
 + the target attribute, that you want to predict.


