                                                                                  Data Set E Code
                                                                        By Christopher Strawn and Minh Duc Ong

                                                        #####################################################################
                                                        #   this README file is for understanding the following code:       #
                                                        #                                                                   #
                                                        #   Project_Graphs.ipynb                                            #
                                                        #   Project_codev3.1-Outliers .ipynb                                #
                                                        #   Project_codev3_2-Standard&Normalize.ipynb                       #
                                                        #   Project_codev3_3-Avgtest.ipynb                                  #
                                                        #   Project_codev3_4-Kbest.ipynb                                    #
                                                        #   Project_codev3_4-knnKselect.ipynb                               #
                                                        #   Project_codev3_5-Initial&avg6&prev3.ipynb                       #
                                                        #   Project_codev3_5-Initial&avg6.ipynb                             #
                                                        #   Project_codev3_5-Initial.ipynb                                  #
                                                        #   Project_codev3_5-Poly.ipynb                                     #
                                                        #   Project_codev3_5-avg6.ipynb                                     #
                                                        #   Project_codev3_5-prev3.ipynb                                    #
                                                        #                                                                   #
                                                        #####################################################################




PROJECT SUMMARY 
the purpose of this project was to produce a classification model for Data Set E utilizing the ethylene_methane.txt data set. The data set was used to classify the presence of Methane
concentraition when Methane PPM was greater than 50% of the combined gases with a 1 for Methane concentraition >50% and 0 for Methane concentraition <50%. Inside of each ipynb there should be a 
small summary of each code block. WARNING: the Data Set E file contains over 4.1 million entries so running the some of these files can take a very long time.





BEFORE RUNNING ANY CODE 

    Before running any of these codes please obtain file ethylene_methane.txt for Data Set E and replace the header found in the original file with the following:

        Time(sec) Methane(ppm) Ethylene(ppm) sensor1 sensor2 sensor3 sensor4 sensor5 sensor6 sensor7 sensor8 sensor9 sensor10 sensor11 sensor12 sensor13 sensor14 sensor15 sensor16

    and then place the file with the new header in the DATA folder found within the same location as the ipynb files




PACKAGES NOT USED IN CLASS
        I believe these should already be already included as part of the lastest verion of Python3 but I wanted to note the onese I used that weren't used in any of the homeworks.

        from copy import deepcopy
        import time




CODE SUMMARY

    Project_Graphs.ipynb
        Produces simple graphs for visuallizing the dataset. The first graphs are grouped by sensor type and the data is then grouped by PPM, the second batch of graphs are just
        straight plots of the data and sections of the graphs are colored for each PPM of Methane.

    Project_codev3.1-Outliers .ipynb
        This code was the intial test for comparing the R2 results before and after removing Outliers

    Project_codev3_2-Standard&Normalize.ipynb
        This code tests the R2 value after applying Standardization and Normalization to the dataset

    Project_codev3_3-Avgtest.ipynb
        This code tests and plots the R2 value and Runtime versus the Moving average window size. 

    Project_codev3_4-Kbest.ipynb
        This code tests and plots the R2 value and Runtime versus number of attributes kept, the final result was used to determine which attributes to keep based on its effect on runtime and 
        R2 value.

    Project_codev3_4-knnKselect.ipynb
        This code tests and plots the R2 value and Runtime versus the number of points used in the KNN fit.

    Project_codev3_5-Initial&avg6&prev3.ipynb
        Produces R2 and runtime results for adding a moving average filter of 6 and 3 previous points attribute for each sensor to the data set when fitted to Logistic Regression, LDA, QDA and KNN models

    Project_codev3_5-Initial&avg6.ipynb
        Produces R2 and runtime results for adding a moving average filter of 6 attribute for each sensor to the data set when fitted to Logistic Regression, LDA, QDA and KNN models

    Project_codev3_5-Initial.ipynb
        Produces Reference R2 and runtime results for comparison

    Project_codev3_5-Poly.ipynb
        Produces R2 and runtime results for adding x^2 attribute to the data set for each sensor when fitted to Logistic Regression, LDA, QDA and KNN models

    Project_codev3_5-avg6.ipynb
        Produces R2 and runtime results for replacing the origninal data set with a moving average filter of 6 for each sensor when fitted to Logistic Regression, LDA, QDA and KNN models

    Project_codev3_5-prev3.ipynb
        Produces R2 and runtime results for adding 3 previous points attribute for each sensor to the data set when fitted to Logistic Regression, LDA, QDA and KNN models