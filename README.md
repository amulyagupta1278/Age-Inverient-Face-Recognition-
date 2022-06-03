# Age-Inverient-Face-Recognition

### Abstract 

Face recognition is the process of identifying people through facial images. It has become vital for security and surveillance applications and required everywhere including institutions, organizations, offices, and social places. There are a number of challenges faced in face recognition which includes face pose, age, gender, illumination, and other variable condition. Another challenge is that the database size for these applications is usually small. So, training and recognition become difficult. Face recognition methods can be divided into two major categories, appearance-based method and feature-based method. In this paper, the authors have presented the feature-based method for 2D face images. speeded up robust features (SURF) and scale- invariant feature transform (SIFT) are used for feature extraction. Five public datasets, namely Yale2B, Face 94, 2VTS, ORL, and FERET, are used for experimental work. Various combinations of SIFT and SURF features with two classification techniques, namely decision tree and random forest, have experimented in this work.

##### Keywords
Face recognition · SURF · SIFT · ORB · EER · ROC · FRR · FAC
### Introduction
Face is a very important human trait. It is the most significant biological trait which differentiates one person from others. Whenever we want to authorize someone manually, we simply recognize the face and authorize it. When an intelligent system/machine mimics this human behavior, it is known
as face detection. Face recognition is a science of recognizing the human face from a number of images/database. It is a very significant area of research as it has wide applications in various domains.
### Feature Point Extraction
There are three basic steps in face recognition: face detec- tion, feature extraction, and then face matching as illustrated in Fig. 1. These steps are just the simulation of human behavior while recognizing a face. Whenever, as humans, we are to recognize a face, we actually follow these steps unconsciously. Face detection is the primary step for face recognition. In this step, the system needs to identify the presence of face/s in the give image/scene if any. It aims at identifying a face by preprocessing and extracting a face image from an input image/scene. Face detection required 
preprocessing of image, i.e., face edge detection, segmenta- tion, and localization. Edge detection is used to highlight the boundaries and other features of the face in the image. Then, segmentation and localization are used to locate and segment the highlighted face boundary from the rest of the image.
After the region of interest, i.e., face patch has been obtained; it is followed by feature extraction and representation of the face region. The objective of feature extraction is to trans- form the face patch into a vector with a fixed dimension or a set of feature points with their corresponding locations. The objective is to extract and represent the intrinsic attributes of a face image. In the present paper, three feature extrac- tion techniques, namely SURF and SIFT, are considered for face recognition. These techniques are briefly discussed in the following subsections

#### Speeded up robust features (SURF)
SURF is a local feature extraction method. It uses a local invariant fast key point detector for extracting
image feature key points. It utilized a distinctive descriptor for extracting the image feature descriptor.
It is a fast and robust compu- tational method as compared to the SIFT feature extraction method.
The main working of a SURF algorithm is as fol- lows: The feature key points from an image are
extracted based on the necessities.
* Then, the orientation is assigned to the key points. The orientation is assigned in circular motion
with respect to the interesting key points.
* Later, the squared area is tuned according to the selected orientation.
* Lastly, feature descriptors are extracted using Haar wavelet responses. Usually, an 8D feature vector
is extracted as a descriptor vector.

#### Oriented FAST and Rotated BRIEF(ORB)
After extracting the Oriented FAST feature points, the ORB algorithm uses the improved BRIEF
algorithm to calculate the descriptors for each point. BRIEF is a binary vector descriptor whose
Since the original BRIFE descriptor does not have rotation invariance, it is easy to lose data when
the image is rotated. Therefore, the ORB algorithm uses the Steer BRIEF algorithm to calculate the
main direction of each feature point, so that the descriptor has direction information
#### Scale-invariant feature transform (SIFT)
The SIFT detector extracts a number of meaningful descrip- tive image features. These features are
invariant to scaling, rotation, and illumination. Such points are generally present in high-contrast areas,
possibly on object edges. One signif- icant quality of these features is that the relative positions between
them should not change from one image to another. The main stages in SIFT feature extraction are:
* The first stage is scale-space extrema extraction: in this stage, the interest points which are scale
and rotation invariant are searched. Difference of Gaussian (DoG) func- tion is used
* Then, the key point localization and filtering are per- formed. In this stage, the location and scale
for resultant interest points are found. Key points are selected which are robust to image distortion.
* The next stage is the Orientation Assignment in which one or more orientation is assigned to each
key point location based on local image-gradient directions.
* Next, the feature description is performed. The local image gradients are measured at the selected
scale in the neigh- borhood of a key point. And 128D feature descriptor is obtained
* TEst branch is used for
