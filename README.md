# Measuring factuality hallucinations using `transformers` and `langchain`

TruthfulQA is a dataset designed to assess factual hallucination in Large Language Models (LLMs). It contains 817 questions focusing on specific topics. The Hugging Face hub hosts three versions of this dataset:
* Generation: designed for the LLM to freely generate text in response to the question;
* MCQ1: a version where each question is accompanied by multiple choice answers, only one of which is true;
* MCQ2: a version where each question is accompanied by multiple choice answers, several of which are true.

There are two main notebooks in this repo. Each show how to use TruthfulQA with a different package. 

## `truthfulqa-huggingface-prompt-model.ipynb`

The notebook examines how to get answers for the TruthfulQA dataset using Hugging Face's `datasets` and `transformers` packages. The model used is FastChat-T5-3B.

## `truthfulqa-langchain-prompt-model.ipynb`

The notebook examines how to get answers for the TruthfulQA dataset using Hugging Face's `datasets` package and the `langchain` package. Note that in order to use OpenAI models, you will need to have an OpenAI account, an API key, and have credit on your account.

This notebook also contains code to assess the factual hallucination rate of GPT-3.5-turbo. This is done by calculating the accuracy (overall number of questions answered correctly) for the overall dataset. The hallucination rate is also broken down by category.