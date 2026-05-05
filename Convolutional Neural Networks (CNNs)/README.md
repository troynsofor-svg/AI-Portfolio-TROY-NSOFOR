Problem Statement: The problem that this project solves is by efficiently analyzing, classifying, and interpreting spatial data—such as images and videos—by automatically 
learning hierarchical features without manual feature engineering.

Approaches: 
Convolutional Neural Networks (CNNs): This was the core algorithm. You built a custom CNN from scratch, which is inherently designed for image processing. 
CNNs efficiently analyze spatial data by:

- Preserving spatial relationships: They understand that pixels close to each other are related.
Parameter sharing: Filters are applied across the entire image, reducing the number of parameters and making them efficient.
Hierarchical feature learning: They learn simple features like edges and textures in early layers, and progressively combine them into 
more complex features (e.g., fur patterns, round shapes) in deeper layers.

- Data Augmentation: To improve the model's ability to generalize and prevent overfitting, you used techniques 
like rotation, shifting, shearing, zooming, and horizontal flipping. This effectively increased the diversity of your training data by creating variations of existing images.

- Transfer Learning: You leveraged pre-trained CNN models (specifically ResNet50 and optionally MobileNetV2) that were already trained on vast image datasets (like ImageNet). 
This method is highly efficient for spatial data tasks, especially with smaller datasets, because:
The pre-trained models already learned robust, general-purpose features from millions of images.
You only needed to train a small, new classification 'head' on top of the frozen pre-trained layers.

- Fine-tuning: To further adapt the transfer learning model to your specific dataset, you unfroze some of the later layers of the pre-trained base model and continued training with a very low learning rate. 
This allowed the model to slightly adjust its high-level feature detectors to be more relevant to distinguishing puppies from bagels.

- Image Preprocessing with ImageDataGenerator: This utility efficiently loads, resizes, and batches image data, and applies the specified data augmentation transformations on-the-fly.

Results: Custom CNN: Your custom-built CNN achieved a 50.00% Test Accuracy with a Test Loss of 0.7231 after 8 epochs of training. 
This model learned from scratch to distinguish between puppies and bagels.

Transfer Learning (ResNet50): Using a pre-trained ResNet50 model, you also achieved a 50.00% Test Accuracy with a slightly lower Test Loss of 0.7132 after 5 epochs. 
This demonstrates that even with fewer epochs, transfer learning can match or slightly outperform a custom model on a small dataset, 
as it leverages features learned from a much larger dataset.

Fine-tuning: Your attempt to fine-tune the transfer learning model by unfreezing some of its layers and 
continuing training for 5 additional epochs did not improve performance, remaining at 50.00% accuracy. 
You correctly identified several potential reasons for this, including the small dataset size, the possibility of the chosen learning rate not being optimal, and 
the fact that the pre-trained features might already be sufficient for this relatively simple binary classification task on limited data.

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
1. Visit: kaggle.com/datasets/returnofsputnik/puppy-or-bagelLinks to an external site.
2. Click "Download" (requires free Kaggle account)
3. In Colab: Click the 📁 folder icon → Upload the zip file
4. Uncomment the manual extraction cell in the notebook

The name of the dataset is Puppy or Bagel
Link to where the dataset is downloaded: kaggle.com/datasets/returnofsputnik/puppy-or-bagelLinks
