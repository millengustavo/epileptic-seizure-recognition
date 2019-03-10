# Epileptic seizure end-to-end classification with Deep Learning techniques
Repository with Machine Learning techniques to identify Epileptic Seizure from EEG data. 

---

# Abstract. 
Epilepsy is a chronic disorder of the brain that affects people of all ages. Approximately 50 million people currently live with epilepsy worldwide with close to 80% living in developing countries. Experienced professionals are able to detect epilepsy by analyzing patterns of the electroencephalogram (EEG). However, in the absence of experts, an automated system is desirable. Many current automatic detection systems use classifiers on top of handengineered features. Deep learning methods are capable of learning from raw data, using a general-purpose procedure, bypassing the feature extraction step. Applying state of the art deep learning techniques to raw EEG data, this work presents an alternative to conventional pattern-recognition systems without the need to extract features from the EEG signals. This technique achieves 100% accuracy in binary classification between epileptic seizure and seizure-free intervals and avoids false negatives in seizure detection on multiclass problems. The tools used in this work are open-source, so this method can be applied to useful assistance applications by anyone.


---

# Dataset
The original dataset from the reference consists of 5 different folders, each with 100 files, with each file representing a single subject/person. Each file is a recording of brain activity for 23.6 seconds.

The corresponding time-series is sampled into 4097 data points. Each data point is the value of the EEG recording at a different point in time. So we have total 500 individuals with each has 4097 data points for 23.5 seconds.

We divided and shuffled every 4097 data points into 23 chunks, each chunk contains 178 data points for 1 second, and each data point is the value of the EEG recording at a different point in time.

So now we have 23 x 500 = 11500 pieces of information(row), each information contains 178 data points for 1 second(column), the last column represents the label y {1,2,3,4,5}.

The response variable is y in column 179, the Explanatory variables X1, X2, ..., X178

The column y contains the category of the 178-dimensional input vector.
Specifically y in {1, 2, 3, 4, 5}:
Recording of seizure activity

They recorded the EEG from the area where the tumor was located

Yes they identify where the region of the tumor was in the brain and recording the EEG activity from the healthy brain area

eyes closed, means when they were recording the EEG signal the patient had their eyes closed

eyes open, means when they were recording the EEG signal of the brain the patient had their eyes open

All subjects falling in classes 2, 3, 4, and 5 are subjects who did not have epileptic seizure. Only subjects in class 1 have epileptic seizure.

Our motivation for creating this version of the data was to simplify access to the data via the creation of a .csv version of it.

Although there are 5 classes most authors have done binary classification, namely class 1 (Epileptic seizure) against the rest.

## Citation Request:
Andrzejak RG, Lehnertz K, Rieke C, Mormann F, David P, Elger CE (2001) Indications of nonlinear deterministic and finite dimensional structures in time series of brain electrical activity: Dependence on recording region and brain state, Phys. Rev. E, 64, 061907
