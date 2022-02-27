In the present scenario, various technologies are facing issues in detecting spectacles. Due to which the identification of a person through those technologies becomes harder and not efficient. This makes the CCTV cameras; iPhone face unlocks to mislead the person identity by wearing glasses. This real-life problem is still facing problems in many technologies, but it is efficient and easier to identify persons with glasses using deep learning techniques. Here I have implemented both image classification (for checking if a person is wearing eyewear or not) and object detection (locating the eyewear in an image).

For Image classification, data for this process is extracted from the Kaggle website. This data which is available consists of 3060 images and each of these consists of different people wearing eyewear and the people without eyewear. This extracted data contains people having eyewear with a count of 1689. Alongside, 1371 images consist of people who are not wearing eyewear. These images that are not wearing eyewear can be mixed with other data and train the model which makes the model robust and have better accuracy when the new data comes in. Furthermore, the data with eyewear is taken for labelling as the system needs the data with labelling to identify which specific part of the image to be analysed for object detection i.e., eyewear detection.  In object detection for labelling the data we have used Computer Vision Annotation Tool (CVAT). CVAT is an open-source interactive online tool used for annotating images for computer vision algorithms. It is being used to annotate 1689 of images with people who are wearing eyewear.

I opted CNN (Convolutional neural networks) is used to predict a person wearing eyewear or not. In this model, we have used 3 layers: Convolutional layer, Activation layer, Max pooling layer to identify the feature of the image and split it in extracting the status of eyewear.

## Image Classification:

<p align="center">
<img src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Glasses_Detection/Image/1.png"
  alt=""width="500" height="350">
  
<p align="center">
<img src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Glasses_Detection/Image/2.png"
  alt=""width="500" height="350">

## Object Detection:
- **Precision:**  
<p align="center">
<img src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Glasses_Detection/Image/3.jpg"
  alt=""width="500" height="350">
  
- **Recall:** 
<p align="center">
<img src="https://github.com/PrudhviRaj-Numburi/Data_Science_Portfolio/blob/main/Projects/Glasses_Detection/Image/4.jpg"
  alt=""width="500" height="350">
