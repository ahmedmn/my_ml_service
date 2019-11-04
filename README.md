# Deploy Machine Learning Models with Django

This is a source code from the tutorial available at [deploymachinelearning.com](https://deploymachinelearning.com)

This web service makes Machine Learning models available with REST API. It is different from the most of the tutorials available in the internet:

- it allows to keep information about many ML models in the web service. There can be several ML models available at the same endpoint with different versions. What is more, there can be many endpoint addresses defined.
- it stores information about requests send to the ML models, this can be used later for models testing and audit.
- it has tests for ML code and server code,
- it allows to run A/B tests between diferent versions of ML models.

## The code structure

In the `research` directory there are:

- code for training machine learning models on Adult-Income dataset [link](https://github.com/pplonski/my_ml_service/blob/master/research/train_income_classifier.ipynb)
- code for simulating A/B tests [link](https://github.com/pplonski/my_ml_service/blob/master/research/ab_test.ipynb)

In the `backend` directory there is Django application that:

- can handle several ML algorithms and make the available as web service with user defined REST API endpoints,
- store information about requests which are send to the ML models,
- allow to run A/B tests between algorithms.

In the `docker` directory there are dockerfiles for running the service in the container.

