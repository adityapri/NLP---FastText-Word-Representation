# NLP---FastText-Word-Representation
FastText represents each word as a bag of character n-grams, and its vector representation as the sum of the representations of each of
the individual character n-grams. Have Implemented the FastText word representation learning in
two parts:

1. The n-gram generator should add word boundary symbols and convert words into a
bag containing character n-grams of lengths 3 to 5, and a special sequence: the word
with boundary symbols. Punctuation symbols should be separated by whitespace
before processing the words. The n-grams should be processed as follows:

• All distinct n-grams present in the input should be mapped to unique integer
indices.
• Assign indices to the n-grams and special sequences lexicographically in ascending
order.

2. The trainer should implement the word2vec skipgram model with negative sampling
and subsampling of frequent words. Optionally, Also use the negative
sampling strategy and context window sampling specified.

Have Used the corpus wmt-news-crawl.txt file. The implementation allows the following operations:

1. Accept an input file of the same format, and output a text file containing the space
separated bags for each input line. Each bag must contain the comma-separated IDs
of the constituent n-grams of the corresponding word, sorted in increasing order of ID.

2. Save the word representations and perform the following experiments:
   i. Demonstrated how FastText allows representing words that would be OOV for a
      word2vec model without subword segmentation.
   ii.Conducted the analysis and reported whether the most important
      n-grams roughly correspond to morphemes
