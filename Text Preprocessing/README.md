Problem Statement: This project solves the problem of "noisy," unstructured, and inconsistent raw text data, transforming it into a clean, 
standardized format suitable for Machine Learning (ML) and Natural Language Processing (NLP) models. 
It eliminates irrelevant information, reduces data dimensionality, and ensures consistent input for higher model accuracy and efficiency.

Approaches: 
In this lab, you addressed the challenge of 'noisy,' unstructured, and 
inconsistent raw text data by applying a series of text preprocessing methods and algorithms, primarily leveraging the NLTK and spaCy libraries:

- Tokenization: You used NLTK's word_tokenize and sent_tokenize and spaCy's tokenizer (via nlp(text) and token.text)
to break down raw text into individual words or sentences, making them manageable units for further processing.

- Stop Words Removal: You employed NLTK's stopwords.words('english') and spaCy's nlp.Defaults.stop_words to filter out common,
less informative words (e.g., 'the', 'is', 'a'), thereby reducing noise and focusing on more meaningful content.

- Morphological Normalization (Lemmatization & Stemming):

For stemming, you utilized NLTK's PorterStemmer to reduce words to their root form (e.g., 'running' -> 'run').
For lemmatization, you used spaCy's token.lemma_ attribute, which provides the base form of a word, 
considering its context and part of speech (e.g., 'was' -> 'be', 'better' -> 'good').

- Text Cleaning and Normalization (Regular Expressions & String Operations): You developed custom functions (basic_clean_text and advanced_clean_text)
that applied several cleaning algorithms,
often using Python's re module (regular expressions) and the string module:

1. Case Normalization: Converting all text to lowercase.
2. Punctuation Removal: Eliminating punctuation marks.
3. Number Handling: Removing numerical digits.
4.  Special Character Handling: Specifically, the advanced cleaner targeted and removed URLs, email addresses, and mentions (@username),
 while converting hashtags (e.g., #coffee to coffee) and removing emojis.
5. Whitespace Normalization: Reducing multiple spaces to a single space and stripping leading/trailing whitespace.

Results: 
- Tokenization Comparison: You observed that spaCy provided richer linguistic annotations (POS tags, lemmas) and 
handled 'messy' social media text (emojis, hashtags) with finer granularity than NLTK, 
making it more robust for complex real-world data.

- Stop Word Removal: spaCy's stop word list was more extensive (326 words) compared to NLTK's (198 words). 
This led to a higher vocabulary reduction with spaCy 
(e.g., 50.0% reduction for simple text with spaCy vs. 28.6% with NLTK), especially when also removing punctuation.

- Stemming vs. Lemmatization: Lemmatization (spaCy) consistently produced valid base forms 
(e.g., 'was' -> 'be', 'better' -> 'good'), preserving semantic meaning. 
Stemming (NLTK's PorterStemmer) was faster but often resulted in non-words ('flying' -> 'fli', 'was' -> 'wa') 
and sometimes failed to group related words ('better', 'good', 'best'). 
Lemmatization showed better 'performance' in maintaining linguistic accuracy.

- Text Cleaning: Custom cleaning functions effectively reduced text length and complexity. 
Basic cleaning of a test string achieved a 26.2% length reduction by removing case, punctuation, numbers, and extra spaces. 
Advanced cleaning for social media texts showed varied reductions 
(e.g., 7.2% reduction for the social media sample), successfully handling URLs, mentions, and processing hashtags and emojis.

- Pipeline Configurations: Across different text types, a 'Standard processing' pipeline (basic cleaning, stop word removal, lemmatization) 
consistently achieved significant token reductions, ranging from 50.0% for simple text to 61.7% for product reviews. 
This demonstrated the 'performance' of the pipeline in streamlining text for analytical tasks.

Key Findings (The things I've learned):
- Tokenization
- Stemming
- Lemmatization
- Stop Word Removal

Technologies Used:
Libraries (NLTK, Collections, spaCy, String, Re, Random, etc.)
Tools (Counter, Word_Tokenize, Stop_Words, Re, Sent_Tokenize, Nltk.Tokenize, Nltk.Corpus, etc.)

How to Run:
- Open Google Colab
- Click on Open notebook
- Click on L02_Troy_Nsofor_ITAI_2373-1.ipynb
- Run the cells from top to bottom


