# PoetryGeneration-RomanUrdu
This repository contains code for generating poetry in Roman Urdu using n-gram language modeling. The code utilizes the spaCy pipeline for text processing and can be used to generate a ghazal consisting of seven stanzas, with each stanza containing two verses.

# Introduction
In this assignment, the goal is to generate poetry using n-gram language models trained on a poetry corpus containing poems from Faiz, Ghalib, and Iqbal. The generated poetry will follow the structure of a ghazal, with each stanza consisting of two verses containing 6-8 words. The assignment also involves scraping online sources to augment the poetry corpus for better representation of Urdu poetry.

# Task
The task involves the following steps:

1. Load the Poetry Corpus: The poetry corpus containing poems from Faiz, Ghalib, and Iqbal is loaded for training the n-gram language models.

2. Tokenize the Corpus: The corpus is tokenized to split it into a list of words.

3. Generate n-gram Models: Bigram and trigram models are trained using the tokenized corpus.

4. Generate Ghazal: For each stanza, a random number between 6 and 8 is generated to determine the length of the verse. The first word of the verse is selected intelligently, and subsequent words are selected based on the most probable next word according to the n-gram models. The last words of the stanzas are attempted to be rhymed with the last word of the first stanza.

# Implementation Challenges
The assignment presents several challenges, including the selection of subsequent words based on the already selected word, and the task of rhyming the verses. To select the most probable next word, a Conditional Frequency Distribution (CFD) is used. Rhyming the generated verses can be achieved by building a dictionary for rhyming.

# n-gram Models
The implementation includes the development of standard n-gram models using the Conditional Frequency Distribution method. Both bigram and trigram models are developed, and the first word of each line is randomly selected from the starting words in the vocabulary. The bigram model is used to generate the next word until the verse is complete. The same steps are followed for the trigram model, and the results of both models are compared.

# Backward Bigram Model
In addition to the standard n-gram models, a backward bigram model is also implemented. The backward bigram model models the generation of a sentence from right to left. This model can be compared with the previous implementations to evaluate its effectiveness.

# Bidirectional Bigram Model
A bidirectional bigram model is built by combining the forward and backward models. This model takes the same input and produces the same style of output as the bigram model. The output of the bidirectional bigram model can be compared to evaluate its performance.

# Code
The code for the implementation is provided in the repository. The implementation utilizes the spaCy library for text processing and includes functions for loading the poetry corpus, tokenizing the corpus, generating n-gram models, and generating the ghazal.

Please refer to the code for more details and instructions on how to run it.

# Acknowledgments
The code in this repository is based on the assignment and instructions provided by the course instructor. It builds upon the concepts learned in the previous assignment on Urdu sentence structure and processing.

Note: The code provided here is a simplified example and may require modifications and enhancements for more accurate and creative poetry generation.
