#  BIS-Analytics_FinalProject

#  Dataset: CSE-CIC-IDS2018 on AWS
## collaborative project between the Communications Security Establishment (CSE) & the Canadian Institute for Cybersecurity (CIC)
## url: https://www.unb.ca/cic/datasets/ids-2018.html 
## Kaggle url: https://www.kaggle.com/datasets/dhoogla/csecicids2018 

#  Rationale: 
## The CSE-CIC-IDS2018 dataset was published by the Canadian Institute for Cybersecurity and is the successor to CIC-IDS2017. 
##  The biggest difference is the move away from on-premise infrastructure to AWS to generate the dataset, while also vastly increases the representation of 'Infiltration' traffic compared to CIC-IDS2017.
##  CICIDS-2018 was generated from a much larger network, resulting in 16,233,002 instances gathered over 10 days of network traffic compared to the 2017 dataset.
##  CICIDS-2018 is generally the better choice for modern intrusion detection research due to its larger size and corrections for flaws in the original dataset
##  The CICIDS-2018 dataset is a recommended alternative to CIC-IDS-2017 because it was prepared from a larger network, has more instances, and corrects several issues found in the earlier dataset, such as a bug in the TCP       flag count and inconsistencies in attack labels. 
##  It's an improved version that better serves intrusion detection research and machine learning evaluations.
##  Studies show that the improved quality of the CICIDS-2018 dataset can lead to better performance in detecting attacks compared to the older dataset. 

#  File Structure:
##  Data is divided into various files based on date. 
##  Parquet files -> need to search/determine how to use
##  Data is divided into various files based on date. Each individual file has imbalanced labels -> need to search which dates/labels to use (decide if to combine imbalanced labels in one “malicious” label).

#   Column Structure of Dataset:
##  In total, there are eighty columns within this dataset, each of which corresponds to an entry in the IDS logging system that the University of New Brunswick has in place. 
##  The most important columns within this dataset are listed below:
##  -	Dst Port (Destination port)
##  -	Protocol
##  -	Flow Duration
##  -	Tot Fwd Pkts (Total forward packets)
##  -	Tot Bwd Pkts (Total backward packets)
##  -	Label (Label) -- determines if the packets sent are malicious or not

#  Task:
##  classification (malicious / benign)
##  --maybe multiclass ??
##  --maybe check for additional analysis (port, protocol, multi-label) ??

#   Algorithms to use (proposal):
##  -Supervised: DT, RF, NB, k-NN, SVM (?), ANN (?), CNN (?)
##  -Unsupervised: K-MEANS (+ PCA), EM (?), SOM (?), CNN (?), SVM (?)

