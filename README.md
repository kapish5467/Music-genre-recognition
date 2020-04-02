# Music-genre-recognition
Packages

    Python 3.6.5
    Tensorflow - 1.7.0
    Keras - 2.2.4
    Numpy, Pandas, Matplotlib
    Librosa - 0.6.2

Raw data:

Download FMA Small from: https://github.com/mdeff/fma Raw data is 8GB and consists of audio from 8000 songs + fma_metadata


To run code in any of these notebooks, first please download raw data from FMA Github link above

    load_fma_dataset: Loads fma_dataset and explores it.
    Plot_Spectograms: Plots spectograms for the 8 different genres
    convert_to_npz: Loads the raw audio, converts each file to a spectogram and pickles the results to make it easy for training models

Building models

To run the code below, please download the processed data from the drive

    baseline_model_fma: This model uses the metadata in tracks.csv to load MFCC features and builds a SVC classifier.

    CRNN_model: This notebook uses the compressed spectograms to build a CRNN model in Keras

    CNN_RNN_Parallel: This notebook uses the compressed spectograms to build a a parallel CNN-RNN model.

Activation Visualization and Embedding Clustering

    Activation_Visualization: This notebook loads the weights for Parallel CNN-RNN model and uses the keras_vis package to draw activation visualizations for the filters in convolution block 1 and convolution block 5

    Embedding_Clustering_CRNN: This notebook extracts the features from the first dense layer of CRNN model and performs clustering on them. It then compares the outputs of the clustering with the true labels
