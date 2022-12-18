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








# Conclusion



