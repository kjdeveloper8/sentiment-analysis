## Sentiment Analysis 

#### Dataset

- Imdb: movie review with sentiment (pos, neg)

#### Model

- Model: distilbert-base-uncased

- Why?
  - Smaller and faster with same bert model
  - Automatically generates inputs and labels as from base model (bert)
  - faster inference for downstream task
  - Has proven good results on en language


#### Fine tuning and evaluation

- Load and split dataset
- Tokenized dataset 
- Padd tokenized dataset with datacolltor
- Define eval matrices (acc, pre, recall, f1)
- Initialized seq2se2 model for downstreaming task (sentiment analysis)
- Define training arg:
  - lr: 2e-5
  -  batch_size: 8
  - epochs: 1
  - fp16: True
    

#### Result

Evalutaion result on test set: 

- eval_loss: 0.18838872015476227
- eval_precision: 0.9336
- eval_recal': 0.9336
- eval_f1: 0.9336
- eval_accuracy: 0.9336
- eval_runtime: 59.6147
