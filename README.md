# IndianFoodImageClassification
Classify indian food images into 12 categories.<br>
### Abstract
  -  The Indian cuisine consists of possibly hundreds of varieties of regional and traditional foods, due to which <br>
food image recognition becomes an essential task. <br>
  -  In this repo we explore a custom-built CNN model and a transfer learning based MobileNetV2 <br>
model for the purpose of food recognition and classification. <br>
  -  A **calorie estimation** algorithm based on image features and nutritional information is proposed, to estimate calories of <br>
the recognized food image. <br>

### DATASET
  - The dataset consists of 12 classes of indian food images. 
  - Each class consists of 70-80 images for training and 30 images for validation.
  - *The dataset is based on the original food20(indian) from kaggle.* <br>
  *The Train and Test folder consists of  the training and test dataset* <br>
  ![image](https://user-images.githubusercontent.com/55789244/159164755-abd10cd4-7aa7-40de-ae90-69cd07b2bda0.png)

### Custom CNN
  - The data was trained on custom CNN model consisting of Convolution, MaxPool, Conv2D Layer, Dropout, Fully Connected layer and ReLu Function. <br>
  - The network is configured to output 12 values, one for each class in the classification task, and the softmax function is used to normalize the outputs. <br>
  - Adam optimization algorithm was used and the learning rate is configured as 0.0001. <br>
  **Results** - The model acheived an overall accuracy of 88.42% for the train dataset and 73% for the test dataset.<br>
  
### Transfer Learning - MobileNetV2
  - The dataset was trained on  pretrained MobileNetV2 model. <br>
   ![image](https://user-images.githubusercontent.com/55789244/159165235-0a3bf5c8-0263-462f-aef7-e51b574403fe.png) <br>

  - The input images are preprocessed to 256x256 size. <br>
  - Learning rate is kept at a minimum value to improve training at 0.0001. Dropout of 0.2 is used. <br>
  - The activation function used is softmax. The optimizer used is Adam optimizer. SparseCategoricalCrossEntropy is used as a parameter for loss values. <br>
  
### Calorie Estimation
  - The algorithm uses the concept of indexed images which is a direct mapping of pixel values to colormap values. The calories range of each food class is obtained from nutrition websites and then used along with the HSV method to estimate the calories of the food image. <br>

### RESULTS
 - *A GUI WAS DEVELOPED USING TKINTER* <br>
  ![image](https://user-images.githubusercontent.com/55789244/159165409-bd167e22-2375-4389-99f8-4213f3b89272.png) <br>
  ![image](https://user-images.githubusercontent.com/55789244/159165457-ac77cff7-a13c-46dc-952c-ecd44950e76e.png)
  ![image](https://user-images.githubusercontent.com/55789244/159165469-4e38f07c-eb6e-4100-9ca2-59549311170f.png) <br>
 **TRAINING AND ACCURACY GRAPHS FOR MOBILENETV2 MODEL**
  ![image](https://user-images.githubusercontent.com/55789244/159165529-6ad9ec80-f5e5-4c2c-9593-58f322b2fd1d.png) <br>
  ![image](https://user-images.githubusercontent.com/55789244/159165542-c6ce2a62-f0ab-4f70-bbe9-ceeb4284a019.png) <br>
 - **The MobileNetV2 model outperformed the CNN model and achieved an accuracy of 79.44%.** <br>
 
 *How To RUN* <br>
  - The UI was developed using Tkinter.
  - To run the front-end : Run the cnn-ui/ui-edited.py file. <br>
  *Note- The Ui was developed for the custom CNN model. For the Transfer learning model please view the indianfoodclassification.ipynb file*
 
 **PUBLICATION** - The research was published at the IRJET Journal. For more detailed information : [IndianFoodClassification](https://www.irjet.net/archives/V8/i8/IRJET-V8I8102.pdf).



