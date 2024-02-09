
Report on Language Models

Overview:
In this project, we implemented four language models to analyze and generate sentences based on different approaches. The models include:

Unigram Model: A basic model relying on unigram probabilities.
Smoothed Unigram Model: Unigram model with Laplace (add-one) smoothing.
Bigram Model: Model considering the probabilities of word pairs (bigrams).
Smoothed Bigram Model with Linear Interpolation (SmoothedBigramModelLI): Bigram model smoothed using Linear Interpolation.

Model Implementation:
Unigram Model:
The Unigram Model is a simple language model that calculates the probability of each word independently. The implementation includes methods for generating sentences and calculating sentence probabilities.

Smoothed Unigram Model:
This model extends the Unigram Model by incorporating Laplace smoothing to handle unseen words. The smoothing helps avoid zero probabilities for unseen words and improves the model's performance.

Bigram Model:
The Bigram Model considers the conditional probabilities of a word given its preceding word. The implementation includes methods for generating sentences, calculating bigram probabilities, and assessing sentence probabilities.

Smoothed Bigram Model with Linear Interpolation:
The Smoothed Bigram ModelLI incorporates Linear Interpolation for smoothing. This technique blends the probabilities from unigrams and bigrams, providing a balance between local and global information. The model includes methods for generating sentences, calculating bigram probabilities, and computing sentence probabilities.

Model Training:
All models are trained on a given corpus, with sentences appropriately preprocessed by adding start and end markers.

Unigram and Smoothed Unigram Models:
Unigram probabilities are calculated directly from the frequencies of each word.
Laplace smoothing is applied to the Smoothed Unigram Model to handle unseen words.

Bigram and Smoothed Bigram ModelLI:
Bigram probabilities are calculated from the observed frequencies of word pairs.
Linear Interpolation is used for smoothing in the Smoothed Bigram ModelLI.

Sentence Generation:
All models can generate sentences based on their learned probabilities. The generation process starts with the beginning-of-sentence marker and continues until the end-of-sentence marker is generated.

Model Evaluation:
Perplexity values are computed for each model on different test corpora. Perplexity measures how well the models predict the test sentences, with lower values indicating better performance.

Perplexity Results:
Unigram Model:
Test Corpus 1: 1899.06
Test Corpus 2: 789.02
Smoothed Unigram Model:
Test Corpus 1: 1964.72
Test Corpus 2: 828.06
Bigram Model:
Test Corpus 1: 0.0
Test Corpus 2: 52.21
Smoothed Bigram ModelLI:
Test Corpus 1: 81.50
Test Corpus 2: 49.50

Observations:
Unigram and Smoothed Unigram Models have high perplexity values, indicating lower predictive performance.
Bigram Model achieves perplexity of 0 on Test Corpus 1, suggesting overfitting or data leakage.
Smoothed Bigram ModelLI performs well on both test corpora, demonstrating the effectiveness of Linear Interpolation smoothing.

Conclusion:
The choice of language model depends on the specific task and data characteristics. While unigram models are straightforward, bigram models with appropriate smoothing techniques, such as Linear Interpolation, can capture more complex patterns in the data. The evaluation results provide insights into the strengths and weaknesses of each model, aiding in model selection based on the specific requirements of the natural language processing task at hand.




