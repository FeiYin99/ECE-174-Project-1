# ECE-174-Project-1
Least squares classfier and K-means clustering

This project was created and run on Python 3.6.9.

Dependencies:
    numpy
    matplotlib
    scipy
    sys
    time
    tqdm
    multiprocessing 

least_squares_classifier.ipynb contains the 1st part of the project
    whereas kmeans_clustering.ipynb contains the 2nd part of the project.

least_squares_classifier.ipynb can be run directly.

However, before running kmeans_clustering.ipynb, run the following line in Terminal:
    jupyter notebook --NotebookApp.max_buffer_size=8589934592

This will re-open Jupyter Notebook and set the memory limit of Jupyter Notebook to 8GB
    such that memory leak does not happen if running the kmeans function with 8 
    multiprocessing pools. 

Important Notes: 
    1) If a system's usable memory is less than 8GB, potential freeze could happen
       when running kmeans with multiple pools. In that case, try reducing the pool count
       by changing the `multiprocessing_pool_count` variable located in the first code cell
       to a smaller number.  

    2) This project makes use of the istarmap function from: 
        https://stackoverflow.com/questions/57354700/starmap-combined-with-tqdm
       This function is written differently for Python version < 3.8 and >= 3.8. 
       This project is created and run on Python 3.6.9.
       If running this project with Python 3.8+, please make changes accordingly.
