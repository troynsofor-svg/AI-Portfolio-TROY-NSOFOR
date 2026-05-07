Problem Statement: This project solves the problem of "noisy," raw, and incompatible unprocessed text data, changing it to a clean, 
structured data fitted for Machine Learning (ML) and Natural Language Processing (NLP) models. 
It removes unrelated details, decreases data dimensionality, and confirms compatible input for higher model accuracy and effectiveness.

Approaches: 
In the lab and project, I addressed the problem of 'noisy,' raw, and 
incompatible unstructured text data by using a sequence of text preprocessing techniques and algorithms, mainly powering the NLTK and spaCy libraries:

- Tokenization: I applied NLTK's word_tokenize and sent_tokenize and spaCy's tokenizer (along with nlp(text) and token.text)
to separate unstructured text into single words or sentences, making them adjustable units for extra processing.

- Stop Words Removal: I used NLTK's stopwords.words('english') and spaCy's nlp.Defaults.stop_words to break down common,
fewer detailed words (e.g., 'the', 'is', 'a'), consequently decreasing sound and concentrating on more relevant material.

- Morphological Normalization (Lemmatization & Stemming):
In stemming, I used NLTK's PorterStemmer to decrease words to their base form (e.g., 'running' -> 'run').
For lemmatization, I applied spaCy's token.lemma_ attribute, which gives the root form of a word, thinking of the context and grammatical form (e.g., 'was' -> 'be', 'better' -> 'good').

- Text Cleaning and Normalization (Regular Expressions & String Operations): I created custom functions (basic_clean_text and advanced_clean_text)
that used some cleaning algorithms,
frequently utlizing Python's re module (regular expressions) and the text preprocessing pipeline:

1. Case Normalization: Changing every text to lowercase.
2. Punctuation Removal: Deleting punctuation marks.
3. Number Handling: Getting rid of numerical digits.
4. Special Character Handling: Particularly, the advanced cleaner earmarked and deleted URLs, email addresses, and reminders (@username),
when changing the hashtags (e.g., #coffee to coffee) and eliminating emojis.
5. Whitespace Normalization: Decreasing tons of spaces to an individual surface and stripping leading/trailing a blank surface.

Results: 
- Tokenization Comparison: I examined that spaCy gave a richer language marking (POS tags, lemmas) and 
dealed with 'messy' social messages (emojis, hashtags) with data analysis than NLTK, 
making it more strong for sophisticated real-world data.

- Stop Word Removal: spaCy's stop word list was more spacious (326 words) matched with NLTK's (198 words). 
This caused a higher vocabulary decrease with spaCy 
(e.g., 50.0% in decrease for simple text with spaCy vs. 28.6% with NLTK), particularly while even deleting punctuation.

- Stemming vs. Lemmatization: Lemmatization (spaCy) compatibly created the correct base forms 
(e.g., 'was' -> 'be', 'better' -> 'good'), maintaining semantic meaning. 
Stemming (NLTK's PorterStemmer) was quicker, unfortunately it frequently resulted in non-words ('flying' -> 'fli', 'was' -> 'wa') 
and ocassionally had the failure of grouping the relevant words ('better', 'good', 'best'). 
Lemmatization illustrated the best 'performance' in preserving linguistic accuracy.

- Text Cleaning: Custom cleaning functions efficiently decreased the amount of text and complexity. 
Basic cleaning of a pattern accomplished a 26.2% length decrease by deleting case, punctuation, digits, and more spaces. 
Advanced cleaning for social media texts showed diverse decreases
(e.g., 7.2% decrease for the social media sample), successfully dealing with URLs, reminders, and preparing hashtags and emojis.

- Pipeline Configurations: Over opposite text types, a 'data engineering' pipeline (basic cleaning, stop word removal, lemmatization) 
consistently accomplished crucial token increases, ranking from 50.0% for simple text to 61.7% for product reviews. 
This illustrated the 'performance' of this pipeline in conciseness for data analysis.

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


