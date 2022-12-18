# DS_UA-301-Final-Project

Multi-class Classification of book covers to predict the categories of the books.  
This project imports image data and trians sequential model through tensorflow to classify the book covers directly.  
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




![image](https://user-images.githubusercontent.com/98332987/208316744-7c0d82d3-194e-471c-8d9c-60069032838f.png)
![image](https://user-images.githubusercontent.com/98332987/208316749-8a904b5e-9113-4446-9b66-62fef6858c1e.png)  


Test loss: 3.103273868560791  
Test accuracy: 0.2738436460494995  
Top 5 categorical accuracy: 0.607859194278717  
![image](https://user-images.githubusercontent.com/98332987/208316770-b482c407-4c37-4ae0-af37-17bd681f54d6.png)
![image](https://user-images.githubusercontent.com/98332987/208316775-d9cdbb89-2d92-4c66-9b88-2d838c977081.png)


Test loss: 3.1028494834899902  
Test accuracy: 0.2771182954311371  
Top 5 categorical accuracy: 0.6002865433692932  
![image](https://user-images.githubusercontent.com/98332987/208316781-c94d24f2-e0f3-44f2-b44d-3b012cd9b9fd.png)
![image](https://user-images.githubusercontent.com/98332987/208316784-2ca987be-89e6-4736-9b5f-6a6f255d7475.png)





# Conclusion



