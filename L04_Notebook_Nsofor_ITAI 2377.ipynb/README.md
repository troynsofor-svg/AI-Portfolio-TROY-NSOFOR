Problem Statement: The problem that this project solves is by transforming messy, 
inconsistent, or raw data into a clean, 
structured, and normalized format suitable for model training.

Approach: For Image Data, you focused on standardizing input with resizing 
and normalization, and enhancing diversity through rotation (data augmentation). 
You utilized cv2 for image manipulation and skimage for normalization.

In Text Data preprocessing, you cleaned raw text by tokenizing, 
removing stop words and punctuation, and reducing words to their base form via lemmatization. 
This was primarily achieved using the nltk library.

For Time Series Data, your work involved handling missing values using 
backward fill and scaling data to a consistent range with min-max normalization. 
Pandas and Numpy were key tools here.

In the Video Data section, you processed individual frames by resizing them and 
converting them to grayscale, again relying on cv2.

Finally, for Audio Data, you extracted significant features like MFCCs to represent 
sound characteristics and then normalized these features. The librosa library was central to this task, 
complemented by numpy for normalization. 
You also generated a dummy audio file using scipy.io.wavfile to ensure reproducibility.

Results: The MFCCs shape was (20, 216) and Normalized MFCCs was shape: (20, 216) of the 
dummy audio file. The video file was not available, a warning was shown, and a 
black placeholder picture was shown instead of the video too. There were 5 images that were showing. 
One of them was rotated and four of them were not. When the picture was rotating, black parts were showing. 
Four of the images were green and blue and one of them was gray. 

Key Findings: The things I learned from this project are the errors and corrections that I made when 
coding cells and real-world applications.

Technologies
- Libraries (Numpy, Matplotlib, NLTK, Librosa, and SciPy)
- Tools (WordNet Lemmatizer, Stopwords, and Word Tokenizer)

How to Run
1. Open Google Colab
2. Click on Open notebook
3. Click on L04_Notebook_Nsofor_ITAI 2377.ipynb
4. Run the cells from top to bottom
