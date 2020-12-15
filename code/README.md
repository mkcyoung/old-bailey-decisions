I did all of my work for this project via Jupyter notebooks in Google's Colaboratory environment. In accordance with the following post by a TA on the discussion board:

*For Jupyter Notebooks, we would like the following:*

1. *the ipynb file*
2. *a pdf/html export of the file with the outputs as they see it (for confirmation)*
3. *The report as usual*
4.  *You can't use libraries that are not on CADE , and you can't use any ML library (like sklearn).*

I’ve submitted my code as a series of Jupyter notebooks w/ pdfs showing their outputs. They are located in folders named to correspond with which algorithms they implement. 

To run the notebooks locally with data, one would need to change the PATH variables located at the top of the notebooks to correspond with where the data is in the local system. The current PATH variables are set to where the data was located in my google drive. For each notebook, I create either a data loading function or class which takes this PATH variable as input and loads the data that the PATH points to. I've indicated in each notebook where I'm loading the data, so make sure that the PATH variable that's being loaded corresponds to where your data is. 

All algorithms but the ones located in 'gradient boosting' and 'neural net and random forest' were implemented without the use of any external ML libraries. 

