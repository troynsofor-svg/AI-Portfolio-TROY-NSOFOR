Problem Statement: The problem that this project solves is by changing messy, 
incompatible, or unstructured data into a clean, 
structured, and regularized format fit for model fitting.

Approach: For Image Data, I concentrated on formalizing input with changing the size 
and regularization, and improving diversity through rotation (data augmentation). 
I used the cv2 for image processing and skimage for formalization.

In Text Data preprocessing, I cleaned unstructured text by word-splitting, 
deleting stop words and punctuation, and decreasing words to their root by using lemmatization. This was mainly accomplished using the NLTK library.

For Time Series Data, my work had something to do with handling missing values using 
backfilling and standardization to a compatible range with min-max normalization. 
I used Numpy as the key library for this part.

In the Video Data section, I processed single photos by changing the size and 
transforming them to grayscale, again still depending on cv2.

Lastly, for Audio Data, I extracted crucial components such as MFCCs to show 
sound characteristics and then formalized these components. I used Librosa for this task, 
matched with Numpy for formalization. 
I even created a dummy audio file by using scipy.io.wavfile to confirm reproducibility.

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
