# DS_UA-301-Final-Project

Multi-class Classification of book covers to predict the categories of the books.  
This project imports image data and trains sequential model through tensorflow to classify the book covers directly.  
And it converts the titles to vectors and use RNN, LSTM, and GRU model to predict the categories.  
It also uses python-tesseract, which is an optical character recognition (OCR) tool for Python, to detect the letters of the title in the book cover and use them to predict their categories with RNN model.

# Link
Kaggle dataset: https://www.kaggle.com/datasets/sjorts/book-covers-and-their-properties

# Repository

DS_UA_301_Final_Project_Frank_Fan.ipynb: The main file   
kaggle.json: Used to be chose when import the dataset from kaggle   
main_dataset.csv: contains all meta information for each book in the dataset, provided paths to each image  

# Results
The training and validation accuracy of classifying the book covers directly:  
![image](https://user-images.githubusercontent.com/98332987/208316443-d4c295ba-6da8-427c-bc69-5ff64888b0ab.png)

The training and validation loss of classifying the book covers directly:  
![image](https://user-images.githubusercontent.com/98332987/208316432-8dd1de37-244e-43a1-9e88-c4b69dae2be1.png)

The training and validation accuracy of classifying the book covers directly after using data augmentation, dropout, and checkpoints:  
![image](https://user-images.githubusercontent.com/98332987/208316477-b350270d-c470-4bea-8c7c-74ec0c723708.png)

The training and validation loss of classifying the book covers directly after using data augmentation, dropout, and checkpoints:  
![image](https://user-images.githubusercontent.com/98332987/208316485-d6b755b0-ff25-45f4-98be-97990ed2cf72.png)

The result of RNN model using titles in the dataset:  
Test loss: 3.26  
Test accuracy: 0.27  
Top 5 categorical accuracy: 0.60  
![image](https://user-images.githubusercontent.com/98332987/208316744-7c0d82d3-194e-471c-8d9c-60069032838f.png)
![image](https://user-images.githubusercontent.com/98332987/208316749-8a904b5e-9113-4446-9b66-62fef6858c1e.png)  

The result of LSTM model using titles in the dataset:    
Test loss: 3.10  
Test accuracy: 0.27  
Top 5 categorical accuracy: 0.61  
![image](https://user-images.githubusercontent.com/98332987/208316770-b482c407-4c37-4ae0-af37-17bd681f54d6.png)
![image](https://user-images.githubusercontent.com/98332987/208316775-d9cdbb89-2d92-4c66-9b88-2d838c977081.png)

The result of GRU model using titles in the dataset:    
Test loss: 3.10  
Test accuracy: 0.28  
Top 5 categorical accuracy: 0.60  
![image](https://user-images.githubusercontent.com/98332987/208316781-c94d24f2-e0f3-44f2-b44d-3b012cd9b9fd.png)
![image](https://user-images.githubusercontent.com/98332987/208316784-2ca987be-89e6-4736-9b5f-6a6f255d7475.png)

The result of RNN model using titles gained by python-tesseract:   
Test loss: 4.15  
Test accuracy: 0.03  
Top 5 categorical accuracy: 0.26  
![image](https://user-images.githubusercontent.com/98332987/208317279-459f4f1f-4531-46bb-a89a-627940efaa93.png)
![image](https://user-images.githubusercontent.com/98332987/208317280-7881edf9-adb2-4d24-9457-f3aa00f3496e.png)

The result of RNN model using a part of the titles in the dataset which only contains 10 classes:    
Test loss: 2.11    
Test accuracy: 0.51  
Top 5 categorical accuracy: 0.87  
![image](https://user-images.githubusercontent.com/98332987/208317328-d743eaa1-639e-49f5-871e-9d9fe909ac98.png)
![image](https://user-images.githubusercontent.com/98332987/208317336-e640d542-9e1e-4583-82a1-b3ea0437c207.png)

# Conclusion
The accuracy of classifying the image of book covers directly is quite low. And both the accuracy and loss doesn't improve much after the training.  
One possible reasons is that the categories of the books in the dataset are too much (33).    
And another reason is that unlike common dataset we use, such has cifar10 which contains images pictured in reality, the book covers in this datset have high diversity even they are in the same category.

The accuracy of classifying the titles is acceptable but has large space for improvement.  
The results of RNN, LSTM, GRU models are very similar, having test accuracy as 0.27 and top 5 categorical accuracy as 0.60, which is the acccuracy that the target is in the top 5 predictions instead of one.
All the training models contain dropout and L2 regularization to prevent overfitting.  
After decrease the number of categories in the dataset to 10, we get the test accuracy of 0.51 and top 5 categorical accuracy of 0.87, meaning that the number of classes does influence the efficiency of improving accuracy.  

The accuracy of classifying the letters gained through python-tesseract is horrible. The main reason is that this method has bad performance on recognizing stylish characters in a colorful image. And since it cannot tell which part of the letters is the title, the test accuracy is extremely low.

Potential solutions and improvement:   
-Better models, more epochs, cycling learning rate schedules.   
-Better character recognition method to increase the success rate of recognizing the letters in the cover.   
-A method to distinguish the title from other words in the book cover(author, comments, etc.)   
-Find other elements rather than titles that are more representative of the categories of the books.  

Future possible development:
Automatically create a book cover after inputting the title, author, and the category.
