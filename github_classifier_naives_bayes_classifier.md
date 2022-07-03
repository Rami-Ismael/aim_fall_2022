#naive_bayes #classifier
![[Pasted image 20220523110506.png]]
https://colab.research.google.com/drive/1ud8MZVs1EoykuTvyZaq2b3dzgmWEKfE7

```Python
def get_all_label():
    number_of_labels = set()
    for repository_owner in os.listdir(os.getcwd()):
        if os.path.isdir(os.path.join(os.getcwd() , repository_owner)) and repository_owner !=".git":
            ## print the the file name in the directory
            for repository in os.listdir(os.path.join(os.getcwd() , repository_owner)):
                for issues in os.listdir(os.path.join(os.path.join(os.getcwd() , repository_owner) ,repository) ):
                    f = open(os.path.join(os.getcwd() , repository_owner , repository , issues))
                    data = json.load(f)
                    try:
                        for node in data["data"]["repository"]["issue"]["labels"]["edges"]:
                            number_of_labels.add(node["node"]["name"])
                    except TypeError:
                        pass
                    f.close()
    return number_of_labels
```

"Whenever you start a new NLP project, it’s always a good idea to implement a set of strong baselines. There are two main reasons for this":

1. A baseline based on regular expressions, handcrafted rules, or a very simple model might already work really well to solve the problem. In these cases, there is no reason to bring out big guns like transformers, which are generally more complex to deploy and maintain in production environments.
   
2. The baselines provide quick checks as you explore more complex models. For example, suppose you train BERT-large and get an accuracy of 80% on your validation set. You might write it off as a hard dataset and call it a day. But what if you knew that a simple classifier like logistic regression gets 95% accuracy? That would raise your suspicions and prompt you to debug your model.
Quotes from Hugging Transformer Book


So let’s start our analysis by training a baseline model. For text classification, a great baseline is a Naive Bayes classifier as it is very simple, quick to train, and fairly robust to perturbations in the inputs. The Scikit-learn implementation of Naive Bayes does not support multilabel classification out of the box, but fortunately we can again use the Scikit-multilearn library to cast the problem as a one-versus-rest classification task where we train L binary classifiers for L labels. First, let’s use a multilabel binarizer to create a new label_ids column in our training sets. We can use the map() function to take care of all the processing in one go:
1. What is Naives Bayes Great YouTube Video
	1. [Naive Bayes, Clearly Explained!!!](https://www.youtube.com/watch?v=O2L2Uv9pdDA)
	2. [Naive Bayes classifier: A friendly approach](https://www.youtube.com/watch?v=Q8l0Vip5YUw)
-  [Create a new Notebook](https://colab.research.google.com/drive/1ud8MZVs1EoykuTvyZaq2b3dzgmWEKfE7)
- Install Python Library
	```Python
		!pip install scikit-multilearn
		!pip install rich
		!pip install pandas #**pandas** is a Python package that provides fast, flexible, and expressive data structures designed to make working with "relational" or "labeled" data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, **real world** data analysis in Python. Additionally, it has the broader goal of becoming **the most powerful and flexible open source data analysis / manipulation tool available in any language**. It is already well on its way towards this goal.
		!pip install numpy
		!pip install seaborn
		!pip install nltk
		!pip install tqdm #tqdm derives from the Arabic word taqaddum (تقدّم) which can mean “progress,” and is an abbreviation for “I love you so much” in Spanish (te quiero demasiado).
	```
- Preprocess the dataset 
	- Make Sure the dataset is store on the cloud
	- if you are using google colab get access to the dataset
		```Python
			from google.colab import drive
			drive.mount('/content/drive/', force_remount=True)
			p = Path("/content/drive/MyDrive")
		``
	- get all the labels in the dataset
	- create a pandas dataframe on the datasets
	- Import MultiLabelBinarizer from sklearn preprocess
	- fit the the MultiLabelBinarizer
	- quick example of MultiLabel Binarizer
	- add a new column in the dataset pandas frame called  multi_label_binarizer
	- create a method of iterative train test split
		- create the trai/test splits iteratively to achieve balanced labels. We wrap it in a function that we can apply to DataFrame
		- To create the splits we can use the iterative_train_test_split() function from Scikit-multilearn, which creates the train/test splits iteratively to achieve balanced labels. We wrap it in a function that we can apply to DataFrames. Since the function expects a two-dimensional feature matrix, we need to add a dimension to the possible indices before making the split:
- Setup the macro and micro scores
- Train and Test the Naives Bayes Model
- [Get the number of True Positive, True negative and false positive](https://androidkt.com/micro-macro-averages-for-imbalance-multiclass-classification/)
- Covert the table to a pandas DataFrame and named the coloumns ( True Positive , False Positive , False Negative , False Positive  , Precision , Recall )
- Get the Recall macro and micro value

End ( First Technical Blog)`
