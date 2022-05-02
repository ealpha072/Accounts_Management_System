# Wikipedia QA

Wikipedia QA is a question answering system based on Wikipedia. The program utilizes the NLP for natural language processing. The algorithm retrieves relevant articles and paragraphs and displays them based on the **bsm25 similarity score** from gensim. The average_idf is calculated for every elemnt in a split query list. This is then used to generate the most appropriate response based on the score. The system is trained on the <a>SQuAD data set</a>. The front end is built on Flask library that renders html and Vuejs. 

#### Results
Taking a supervised approach, using the cosine similarity (cs_i) of each sentence (s_i) within a document as input feature for a random forest classifier and training it with 66% of our data and evaluating on 33% gave an match rate of 65,01%.Employing a multilayer perceptron network the accuracy ranged from 40%( 15 hidden units, 2 layer) to 64,03%(150 hidden units, 2 layer). Adding more layers did not improve performance, also having more than 80 hidden units per layer does not significantly improve performance anymore. Using eucledian distance, cosine similarity and wordshare for each sentence as input feature we obtained an accuracy of 65,15% for the random forest and ~47% for the multilayer perceptron for various hidden unit sizes between 30 and 300. 


#### Potential errors
The program raises a disambiguition error when it detects ambiguity in the search term. The program also raises error in the usage of en-core-web-sm. Incase an error with en-core-web is encountered, resolve with 

``` python
        python -m spacy download en_core_web_sm
```

## Getting Started
### 1. Install dependencies

```bash
$ pip install -r requirements.txt
```

### 2. Run the application

```bash
$ flask run
```

### 4. Open browser

Go to <http://127.0.0.1:5000>.

