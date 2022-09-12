Natural Language Tools for Open Source Tools

  
# GitHub Multi-Label Issue Classifier 
## 1  Abstract
  Most open source code development is done on GitHub. When errors occur, the new developer will send a bug and hopefully label it appropriately. However, they are the open source code they classify and wrong wastes more time from an overwhelmed open source maintainer. The goal is to use the data of maintainers with extensive knowledge about the open source code GitHub issues to classify issues correctly. 
## 6 Resources
1. [What is a Neural Network](https://www.youtube.com/watch?v=aircAruvnKk)
3. [# Lecture 1: Deep Learning Fundamentals (Full Stack Deep Learning - Spring 2021)](https://www.youtube.com/watch?v=fGxWfEuUu0w&list=PL1T8fO7ArWlcWg04OgNiJy91PywMKT2lv&index=2)
2. [Lecture 5: ML Projects (Full Stack Deep Learning - Spring 2021)](https://www.youtube.com/watch?v=pxisK6RMn1s&list=PL1T8fO7ArWlcWg04OgNiJy91PywMKT2lv&index=12)
3. Chapter 7 on Natural Language Processing with Transformers
4. [Multi Label Text Classification with Bert and PyTorch Lightning](https://curiousily.com/posts/multi-label-text-classification-with-bert-and-pytorch-lightning/)
## Timeline
1. Create a naive bayes classifier
2. 
# Find Answers to Frequently Asked Questions
## 1 Abstract
 The most common thing that occurs for open source developers is getting asked the same question over and over again. To reduce the strain on the maintainer, you want to give a question about certain open source libraries; you can retrieve relevant answers or supporting documents. Sometimes google gives you a StackOverflow link to a question with no answers.  You can use semantic search to find the relevant answer
## 6 Resources
- Pinecone Documentation
- Haystack documentation
### 6.1 Compute
I need a GPU. Sentence Transformer takes over to train on CPU. 
### 6.3 Times
This should take two weeks
# Find Relevant Open Source Documentation while writing in vs code extension
## 1  Abstract
1. Using open source is looking through the website documentation frequently to give a particular result. Given a quick description with or without code snippets, the user will retrieve applicable documentation , stack overflow, and other to find help code snippets while in VSCode no need to go to your browser and do a quick google search

## 2 Introduction and Prior Work
**Sphere** Where you have a sphere corpus. The goal is to create better search find relevant context. The reason why to choose google. Google is a black box cannot relied to different need for each person. You can instead create a better search engine. 
**GitHub Code Search** This provide use created code snippet base on from the entire github code
## 3 Deliverable
This project will created a simple vscode plugin that return relevant documentation that   has better useful. 
## 4 Based on the idea
[The Web Is Your Oyster - Knowledge-Intensive NLP  
against a Very Large Web Corpus](https://arxiv.org/pdf/2112.09924.pdf)
[CCNEt Extracting High Quality Monolingual Dataset from Web Crawl Data](https://arxiv.org/pdf/1911.00359.pdf)
[How To Create And Deploy A VSCode Extension](https://www.youtube.com/watch?v=q5V4T3o3CXE)
# Make a python code less or more pythonic
## 1  Abstract
The goal of the project is to use code generation to change the code snippet to make it easier. Beginners will receive code that is too pythonic and hard to understand. This will reduce the barrier to entry for new programmers in python using. In this approach, we will be using the current NLP deep learning model. 
## Introduction and Prior Work
**InCoder** This can replace a snippet of the code , with something 
**OpenAi** Have some resource on the codesnippet
## Timeline
1. Try Prompt Engineering using open ai GPT-3 using  [Interactive and Visual Prompt Engineering for Ad-hoc Task Adaptation with Large Language Models](https://prompt.vizhub.ai/)
2. idk
# Make a particular snippet of code more faster in python ( I think this is impossible , but let see)
## 1.  Abstract
Python has interpreted programming language, thus making it slow compared to other programming languages. The only way to improve the user performance of the programming is to use libraries to increase performance. For example, a simple for loop has to be vectorized in NumPy to be the fastest approach. To make high-performance code requires lots of technical knowledge, while the average person using python wants to get stuff done quickly., however unable to make the program faster sometimes can break a project. In this project, you will be using the In-Filling approach using a Deep Learning model to change the code in the in-filling to increase performance and not create more errors. 


# Resource 
1. Join some good Discord
	1. Hugging Face
	2. Carper AI
	3. Learn AI Together 
	4. [Learn Machine Learnign](https://discord.gg/uFmNWCfhCm)