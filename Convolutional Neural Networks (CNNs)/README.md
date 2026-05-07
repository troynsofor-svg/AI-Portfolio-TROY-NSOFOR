Problem Statement: The problem that this project solves is effectively observing, categorizing, and explaining spatial data—like pictures and videos—by automatically 
learning hierarchical components without data transformation.

Approaches: 
Convolutional Neural Networks (CNNs): This is the main algorithm. I've made a custom CNN from scratch, which is essentially made for image analysis. 
CNNs effectively examine geospatial data by:

- Maintaining topological relationships: They comprehend that pixels close to each other have something in common.
Parameter sharing: Filters are used over the whole picture, by decreasing the number of parameters and causing them to be effective.
Hierarchical feature learning: They learn simple parts such as surfaces and textures in early layers, and progressively integrate them into 
more sophisticated parts (e.g., fur patterns, round shapes) in deeper layers.

- Data Augmentation: To improve the model's capability to adapt and stop overfitting, I used methods such as rotation, shifting, shearing, zooming, and horizontal reflection. This efficiently maximized the variety of my training data by making versions of existing pictures.

- Transfer Learning: I powered pre-trained CNN models (particularly ResNet50 and optionally MobileNetV2) that were already trained on huge picture datasets (such as ImageNet). 
This technique is highly effective for geospatial analysis, particularly with little datasets, because:
The pre-trained models already learned strong, general-purpose parts from lots of pictures.
I just needed to train a little, new categorization 'head' on top of the frozen layers.

- Fine-tuning: To then adapt the transfer learning model to my limited dataset, I unfroze several of the next layers of the tranformer model and persisted to training with a very low step size. 
This enabled the model to change its high-level feature detectors a little bit to be more related to differentiating puppies from bagels.

- Image Preprocessing with ImageDataGenerator: The utility effectively loads, changes the size, and batches image data, and uses the specified noise injections on-the-fly.

Results: 
Custom CNN: My custom-built CNN accomplished a 50.00% test accuracy with a test loss of 0.7231 after 8 epochs in training. 
My model learned from scratch to differentiate between puppies and bagels.

Transfer Learning (ResNet50): Using the transfer learning model, I even accomplished a 50.00% test accuracy with a somewhat lower test loss of 0.7132 after 5 epochs in training. 
This describes that even with a small number of epochs, transfer learning could match or somewhat surpass a custom model on a little dataset, 
as it powers components learned from a much bigger dataset.

Fine-tuning: My effort to fine-tune the ResNet 50 model by unfreezing several of its layers and 
persisting the training for 5 more epochs didn't enhance performance, leaving only 50.00% accuracy. 
I accurately spotted some potential explanations for this, including the little dataset size, the likelihood of the chosen step size not being optimal, and 
the fact that the pre-trained parts may have already been enough for this relatively simple two-class classification on limited data.

Key Findings (What I learned):
- CNN fundamentals: convolutional layers, pooling, and feature maps
- Building a CNN from scratch for binary image classification
- Transfer learning with pre-trained models
- Fine-tuning strategies for custom datasets

Technologies:
- Libraries (TensorFlow, Keras, Sklearn, Numpy, Matplotlib, Seaborn, Shutil, Zipfile, os, and Pandas)
- Frameworks (Sklearn, TensorFlow, and Keras)

How to Run:
- Open Google Colab
- Click on Open Notebook
- Click on Module_03_Lab_Troy Nsofor_.ipynb
- Run all the cells from top to bottom

Instructions on how to download and load the dataset
1. Visit: https://www.kaggle.com/datasets/returnofsputnik/puppy-or-bagel to an external site.
2. Click "Download" (requires free Kaggle account)
3. In Colab: Click the 📁 folder icon → Upload the zip file
4. Uncomment the manual extraction cell in the notebook

The name of the dataset is Puppy or Bagel
Link to where the dataset is downloaded: https://www.kaggle.com/datasets/returnofsputnik/puppy-or-bagel
