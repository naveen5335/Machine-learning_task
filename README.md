# Machine-learning_task
       import numpy as np 
       import matplotlib.pyplot as plt 
       import pandas as pd
       # Importing the dataset 
       data = pd.read_csv('train.csv') 
       Y = data.fetal_health
       X = data.drop('fetal_health',axis=1)
       
              from sklearn.model_selection import train_test_split 
       X_train, X_test, Y_train, test_Y = train_test_split(X, Y, test_size = 0.2, random_state = 101)
       from sklearn.naive_bayes import GaussianNB
       gnb = GaussianNB()   #Create a Gaussian Classifier
       gnb.fit(X_train, Y_train)   #Train the model using the training sets
       y_pred = gnb.predict(X_test)   #Predict the response for test dataset
       y_pred = model.predict(X_test)
       y_pred
       
               array([1., 3., 1., 1., 1., 2., 2., 3., 1., 1., 1., 1., 2., 1., 1., 1., 1.,
       1., 1., 2., 2., 1., 1., 1., 2., 1., 1., 1., 1., 1., 1., 1., 2., 1.,
       1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 2., 1., 1., 1., 1., 1., 3.,
       1., 1., 1., 1., 1., 1., 3., 1., 1., 1., 2., 2., 2., 1., 1., 1., 1.,
       1., 1., 1., 1., 2., 1., 1., 1., 2., 1., 2., 1., 1., 1., 2., 1., 1.,
       1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 2., 1.,
       3., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1.,
       2., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 3., 3., 3., 1., 1.,
       1., 1., 1., 1., 3., 1., 1., 1., 1., 1., 2., 1., 2., 2., 2., 1., 1.,
       1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 2., 1., 1.,
       1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 3., 2., 1., 1., 2.,
       1., 3., 3., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 2., 1.,
       2., 1., 3., 2., 1., 1., 2., 1., 1., 1., 2., 1., 1., 1., 3., 1., 1.,
       1., 1., 1., 1., 1., 1., 1., 1., 1., 3., 2., 2., 1., 1., 1., 1., 3.,
       1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2.,
       2., 2., 1., 1., 1., 3., 2., 1., 1., 1., 1., 3., 3., 1., 1., 1., 1.,
       1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1.,
       1., 1., 1., 1., 1., 3., 1., 1., 1., 3., 1., 1., 1., 3., 1., 1., 1.,
       1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1.,
       1., 1., 2., 1., 1., 1., 1., 1., 3., 1., 1., 1., 1., 1., 1., 1., 1.])


      #Import scikit-learn metrics module for accuracy_score
      from sklearn import metrics
      print("Accuracy:",metrics.accuracy_score(test_Y, y_pred))
  
            Accuracy : 0.9294117647058824

      Validation_test = pd.read_csv('test.csv') 
      val_pred =model.predict(Validation_test)
      val_pred

                    array([1., 1., 2., 1., 2., 2., 1., 1., 1., 1., 1., 1.,               1., 1., 1., 1., 2.,
            3., 1., 2., 1., 3., 2., 1., 2., 1., 1., 1., 1., 3., 2., 2., 1.,               2.,
            3., 1., 1., 1., 1., 2., 2., 1., 1., 1., 1., 1., 1., 3., 1., 1.,               1.,
            1., 1., 1., 1., 1., 1., 1., 2., 2., 1., 1., 1., 1., 1., 2., 1.,               1.,
            1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 3., 1., 1.,               1.,
            1., 1., 1., 1., 1., 3., 1., 1., 2., 1., 2., 1., 1., 1., 1., 3.,               1.,
            1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1., 1., 1.,               1.,
            1., 1., 1., 1., 3., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1.,               1.,
            1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 3.,               1.,
            2., 2., 3., 2., 1., 1., 1., 1., 3., 1., 2., 1., 1., 2., 1., 1.,               1.,
            3., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 2.,               1.,
            1., 1., 3., 2., 1., 2., 1., 1., 1., 2., 1., 1., 3., 1., 1., 1.,               1.,
            1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 3., 1., 1.,               1.,
            1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1., 1., 1.,               1.,
            1., 1., 1., 3., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1.,               1.,
            3., 1., 3., 1., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 3.,               1.,
            1., 1., 1., 1., 2., 1., 1., 1., 3., 1., 1., 1., 1., 3., 3., 1.,               2.,
            1., 1., 1., 1., 1., 1., 3., 1., 1., 1., 1., 3., 1., 1., 1., 3.,               1.,
            1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1.,               1.,
            1., 1., 3., 1., 1., 1., 1., 1., 2., 1., 1., 2., 2., 1., 1., 1.,               1.,
            1., 1., 1., 2., 1., 1., 2., 1., 2., 1., 2., 1., 1., 1., 1., 1.,               2.,
            1., 3., 3., 1., 2., 1., 1., 1., 1., 1., 1., 1., 1., 1., 1., 2.,               1.,
            2., 1., 1., 2., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1., 1.,               2.,
            1., 1., 2., 1., 1., 1., 1., 1., 1., 1., 2., 1., 1., 1., 1., 1.,               1.,
            1., 1., 1., 1., 1., 1., 1., 2., 2., 1., 1., 1., 3., 1., 1., 1.,               1.,
            1.]

       output=[val_pred]
       df=pd.DataFrame(output)
       new=df.to_csv(r'output.csv',index=None,header=True)
       print(df)  

                   0    1    2    3    4    5    6    7    8    9    ...  416                   417  418  419  \
                   0 1.0 1.0 2.0 1.0 2.0 2.0 1.0 1.0 1.0 1.0 ... 2.0 1.0 1.0                    1.0
         
                   420 421 422 423 424 425
                   0 3.0 1.0 1.0 1.0 1.0 1.0

                               [1 rows x 426 columns]
