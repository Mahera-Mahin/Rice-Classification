# Rice-Classification
Rice is one of the most widely cultivated grain crops globally, with numerous genetic varieties. These varieties are typically distinguished based on characteristics such as texture, shape, and color. Such features allow for the classification and quality assessment of rice seeds. In this study, five rice varieties commonly cultivated in Turkey—Arborio, Basmati, Ipsala, Jasmine, and Karacadag—were analyzed. The dataset consists of 75,000 grain images, with 15,000 images per variety.

Two different approaches were tested:

Dimensionality reduction using PCA, reducing 250x250 pixel images to 20 principal components, followed by classification using algorithms like Decision Trees, Logistic Regression, Gradient Boosting, etc.

Classical computer vision methods, including a basic convolutional neural network and MobileNet with transfer learning.

Results:

The XGBoost classifier achieved the best performance, with an accuracy of 97.8% using the 20 PCA features. It also had a very fast inference time of 0.01 seconds for 12,500 samples. Similar performance was observed with LightGBM and SVM.

In contrast, convolutional networks required over 30 seconds for inference and achieved a lower accuracy of around 91%.

Other methods like Logistic Regression, Decision Trees, and Random Forests showed comparatively lower accuracy.

Conclusion:
The XGBoost classifier is the most suitable model for this task, offering both high accuracy and low computational demand, making it ideal for edge device deployment in industrial applications.

Potential improvements include:

Increasing the number of PCA components beyond 20;

Applying ensemble learning methods;

Performing detailed hyperparameter tuning.

This is the link of the demo video of the project: https://www.loom.com/share/2eed4c829eda4ca7bad3e34ede391d29?sid=d7f294c5-c756-495f-aa18-9d53552ba0b2
