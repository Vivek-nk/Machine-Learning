# Age Prediction from Facial Images 

## Aim: 
To develop a python program that would be able to guess the age of person given his or her photo. 

## Procedure: 
Principal Component Analysis is performed on a very large data set to reduce the dimension of the dataset. Then, a linear regression model is trained on the reduced-dimension dataset to learn their age. 

## Background on PCA:
Problems arise when performing learning in a higher-dimensional space due to the phenomenon known as "Curse of the dimensionality".
Significant improvements can be achieved by first mapping the data into a lower-dimensional space which can be achieved with the help of PCA.
In Image learning paradigm, principal components obtained from the given images are affectionately called the " Eigen Faces". 

Steps to compute Eigen Faces:

Step 1: Obtain the 2D face images, I1, I2, ..., Im (the training faces). All faces must be of the same resolution.

Step 2: Represent every image Ii as a vector Γi

Step 3: Compute the average face vector, Ψ , dimension of which is n2×1 :

Step 4: Subtract the mean face from the original faces. This step is very essential, and is called to centerize the data. Φi=Γi−Ψ , It is also a n2×1 dimensional vector.

Step 5: If the matrix, A is represented as:
A=[Φ1
T
Φ2
T
⋮
Φm T ] , and it is certainly an m×n2 matrix, then compute the covariance matrix, C, which is an m×m matrix.

Step 6: Compute the eigenvectors ui of AT A . The dimension of each of the eigenvector will be n2 . 

Step 7: Keep only K eigenvectors, corresponding to the K largest eigenvalues. This is the  K eigenfaces (a.k.a., principal components). Since each of the K eigenfaces are essentially
n2 dimensional vectors, out of curiosity if you do reshape the eigenfaces to n×n and display them as images, you will be astonished to see the eigenfaces. They may look like
ghosts! Rumor has it: you will be able to recover a human from these ghosts. Just joking! But, I would like to make a note on a property of PCA that makes it one of the most beautiful (and extraordinary)
algorithm. Each of the centered image, Φi in the training dataset can be represented as a linear combination of the best K (ghosts) eigenvectors (i.e., eigenfaces):

Step 8: Project all the original faces (after centering) from the training dataset onto this eigenfaces direction:

Here, we are projecting our original faces onto a subset of K eigenfaces, thus reducing each image from n2 dimensions down to a vector Ω of only K dimensions. Each of the normalized training face Φi is projected onto the eigenfaces by a vector,

The images can then be reconstructed in n2 dimensions from the K dimensional Ω encodings, with some loss in accuracy, using the formula above, or if you need more elaboration, here it is:

Reconstructured image= ^Φi=(Ω1 i u1+Ω2 i u2+⋯+ΩK i uK )

Download wiki_labeled.zip and extract the contents. The wiki_labeled/ directory will contains 60327 facial images kept in
100 folders, naming 00-99. Dimension of each image is 100 pixels by 100 pixels. Also, download the wiki_labeled.mat file, containing meta information of each of the 60327 images:

• ID: identification number of the subject (starting from 2002)

• dob: the date of birth of the subject. (It is Matlab’s datenum value calculated based on total number of days since January 0, 0000.)

• dob_str: the DD-MMM-YYYY format dob value.

• photo_taken: when the photo was taken (only the year value)

• full_path: directory path, including filename of the image

• gender: Gender of the subject (0: female, 1: male, NaN if unknown)

• name: name of the subject

• face_location: location of the face.

• face_score: detector score (the higher the better). Inf implies that no face was found in the image, and the face_location then just returns the entire image.

• second_face_score: detector score of the face with the second highest score. This is useful to ignore images with more than one face. second_face_score is NaN (not a number) if no second face was detected.

• age: age of the person (in years), and was calculated based on the “dob” value and the “photo_taken” values.

To read/extract information from the mat file, the loadmat library from scipy.io in python is used.

2. Randomly split the dataset into 80% training and 20% test sets.

3. Compute the principal components (i.e., eigenfaces) from the training dataset. 

4. Draw a scree-plot to choose a best value for K that denotes how many principal components to retain.

5. Show the top 20 ghosts (i.e., eigenfaces) in a 10x10 grid.

6. Considering the chosen K value above, project the training and test images on to the eigenfaces to reduce the dimensionality.

7. Perform Stochastic gradient descent (SGD) based linear regression on the training dataset to learn “age”.A trial-and-error is done to tune the hyper-parameters of the SGD based linear regression (e.g., number of epochs, learning rate)

8. Predict the test dataset (from step 2) based on the learned model in step 7, and report Root Mean Square Error (RMSE)


### Programming Language used: 
Python 

### Machine learning Algorithm used: 
Stochastic Gradient based Linear Regression

### Libraries and Packages used: 
1) NumPy
2) Matplotlib
3) fnmatch
4) SciPy
5) Sklearn
6) PIL
7) cv2
