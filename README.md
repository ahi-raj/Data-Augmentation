# Deeplearning
## Data Augmentation To Address Overfitting In Flower Classification CNN
### Data augmentation is a process of generating new training samples from current training dataset using transformations such as zoom, rotations, change in contrast etc

Built a CNN to classify flower images and see how the model overfits and how overfitting can be addressed using data augmentation.

Learn more from tensorflow offical tutorial: https://www.tensorflow.org/tutorials/images/classification

Dataset used: https://www.tensorflow.org/datasets/catalog/tf_flowers

```python
dataset_url = "https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz"
data_dir = tf.keras.utils.get_file('flower_photos', origin=dataset_url,  cache_dir='.', untar=True)
```
Read the images into numpy array and preprocess it.
Train the CNN and evaluate
The evaluation shows the model is overfitting as the test accuracy is significantly low
 
### Improve the accuracy using Data augmentation and Drop out layer technique
The Dropout layer is a mask that nullifies the contribution of some neurons towards the next layer and leaves unmodified all others and prevents overfitting on the training data.

After using the data augmentation and drop out layer the accuracy of test set increased significantly
