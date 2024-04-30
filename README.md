### Hugging Face Model
Link to hugging face model : [airbnb-reviews-helpfulness-classifier-roberta-base](https://huggingface.co/lihuicham/airbnb-reviews-helpfulness-classifier-roberta-base)

### Team Members (S001 - Synthetic Expert Team E) :

Li Hui Cham, Isaac Sparrow, Christopher Arraya, Nicholas Wong, Lei Zhang, Leonard Yang

### Description
This model is an AirBnB reviews helpfulness classifier. It can predict the helpfulness, from most helpful (A) to least helpful (C) of the reviews on AirBnB website.

### Pre-trained LLM
Our project fine-tuned [FacebookAI/roberta-base](https://huggingface.co/FacebookAI/roberta-base) for multi-class text (sequence) classification. 

### Dataset
5000 samples are scraped from AirBnB website based on `listing_id` from this [Kaggle AirBnB Listings & Reviews dataset](https://www.kaggle.com/datasets/mysarahmadbhat/airbnb-listings-reviews). Samples were translated from French to English language.  

Training Set : 4560 samples synthetically labelled by GPT-4 Turbo. Cost was approximately $60.

Test/Evaluation Set : 500 samples labelled manually by two groups (each group labelled 250 samples), majority votes applies. A scoring rubrics (shown below) is used for labelling. 

### Training Details
```
hyperparameters =  {'learning_rate': 3e-05,
                    'per_device_train_batch_size': 16,
                    'weight_decay': 1e-04,
                    'num_train_epochs': 4,
                    'warmup_steps': 500}
```

We trained our model on Colab Pro which costed us approximately 56 computing units. 

This fine-tuned roberta-based model is a text classifier to predict the helpfulness of AirBnB reviews. 

### Slides

<img width="839" alt="image" src="https://github.com/lihuicham/airbnb-helpfulness-classifier/assets/99931775/3241d000-1b2c-4fc2-8ff7-d08e2914255e">
<img width="833" alt="image" src="https://github.com/lihuicham/airbnb-helpfulness-classifier/assets/99931775/875343ea-e9c5-46f0-8332-d545b87d0fa4">
<img width="835" alt="image" src="https://github.com/lihuicham/airbnb-helpfulness-classifier/assets/99931775/dc423b32-77c6-43f7-9de5-58ed6e95bffd">
<img width="838" alt="image" src="https://github.com/lihuicham/airbnb-helpfulness-classifier/assets/99931775/5e7bf728-04ec-4bbd-a3a8-cdd6442407d3">
<img width="609" alt="image" src="https://github.com/lihuicham/airbnb-helpfulness-classifier/assets/99931775/939819f6-2693-44b0-828e-82affc72ae3d">




