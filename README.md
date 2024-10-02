This is the most interesting (in my opinion) of all the individual projects I developed while studying for my degree.

The project uses the dataset found [here](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset), last downloaded on 14/12/2022

The notebook explains (in Catalan) and executes each part of the process I followed. This includes:
- Data Analysis & Cleansing: In this part the dataset is analyzed, deciding which columns are relevant, which could cause a bias in the classification, and, going further, checking for bias sources within each news article's text.
- Classification Models:
  - Random forest with TF-IDF
  - Naive Bayes with [spaCy](https://spacy.io/) and its large CPU English pipeline
  - Neural Network with [GloVe](https://nlp.stanford.edu/projects/glove/)'s pre-trained word embeddings (specifically the 100d vectors found [here](https://nlp.stanford.edu/data/glove.6B.zip))


The final results were:

<table>
  <tr>
    <th rowspan="2" style="text-align:center;">RESULTS</th>
    <th colspan="3" style="text-align:center;">MODELS</th>
  </tr>
  <tr>
    <th style="text-align:center;">Random Forest</th>
    <th style="text-align:center;">Naive Bayes</th>
    <th style="text-align:center;">Neural Network</th>
  </tr>
  <tr>
    <td style="text-align:center;">Accuracy</td>
    <td style="text-align:center;">0.995</td>
    <td style="text-align:center;">0.868</td>
    <td style="text-align:center;">0.913</td>
  </tr>
  <tr>
    <td style="text-align:center;">Time</td>
    <td style="text-align:center;">7 minutes</td>
    <td style="text-align:center;">42 minutes</td>
    <td style="text-align:center;">41 minutes</td>
  </tr>
</table>

Looking back on it, the project could have been more interesting if instead of checking different models I had performed a hyperparameter optimization for the first model, nevertheless, I learned a lot while developing this so I'm happy with the results.