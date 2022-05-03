# Wikipedia QA
Factoid Question Answering Chatbot is a simpler version of question answering system. It answers to the question asked by user in near real time using information retrieval and natural language processing technique. Chatbot is able to answer Factoid and Summarization based question from article of various domains with an accuracy of 70.16% (measured on SQuAD dataset of stanford).


## Methodology
Architecture of this bot closely follow the architecture described in the book. Main modules of the QA System are:

* Question Processing : In this step, bot identifies type of question and type of answer it expects

* Passage Retrieval : It generates question vector and vectors of passage using TF-IDF as feature, it computes cosine similarity between question vector and passage vector returning top 3 closely resembling passage. Furthur improvement to this step has been done by removing Stop Words and using Porter Stemmer

* Sentence Retrieval : After retrieving passage, it tokenize sentences and computes ngram similarity between question and sentence. Thus identifying most relevant sentences.

* Answer Processing : Based on the expected answer type, then it process the answer sentence to identify particular entity using name-entity recognization technique and part of speech tagging technique

* Text summarization : If type of question is definition or bot is unable to identify named-entity from question, it summarize the text using ngram tilting technique

### How to run
* Install all packages in the text document recursively
* Install flask for the front end 
* Run the app by running
```bash
        flask run
```
* Visit the localhost on browser
