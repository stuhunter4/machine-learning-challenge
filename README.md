# machine_learning_exoplanets:
Create machine learning models capable of classifying candidate exoplanets from data collected by the NASA Kepler space telescope over a period of nine years.

Each model is in its own Jupyter notebook.  The model with the best accuracy is saved in the 'models' folder, for the Neural Network model from TensorFlow.  Preprocessing included scaling with scikit-learn's MinMaxScaler, and their LabelEncoder with to_categorical from TensorFlow for the neural network and deep learning dependent variable.  Feature selection was done with a Random Forest Classifier, and hyperparameters tuned with GridSearch; both from scikit-learn.  In total, eight different models were tested and compared.  Additional notebooks test various feature selections and parameters for three of the eight models, attempting to find a model with a higher accuracy.

Among the models used, the scores for the neural network and deep learning models from TensorFlow had the highest scores.  After many different experiments with parameter tuning, the best score was for the saved neural network model

    loss: 0.2906 - accuracy: 0.8867

This score comes from using Random Forest Classifier numerous times to find the optimal features to select for model training.  The feature selection narrowed our total features to these twelve: 

    koi_fpflag_nt
    koi_fpflag_ss
    koi_fpflag_co
    koi_fpflag_ec
    koi_duration_err1
    koi_duration_err2
    koi_prad
    koi_prad_err1
    koi_prad_err2
    koi_model_snr
    koi_steff_err1
    koi_steff_err2

At 88.67% accuracy, I believe this model would be a useful tool for classifying candidate exoplanets from raw data.  Some things that might improve the model include researching other classification models, researching hyperparameter tuning and feature selection further, or perhaps using larger datasets to train our models.