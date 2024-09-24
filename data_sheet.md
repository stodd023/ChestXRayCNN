# Datasheet 
This datasheet contains the accessible information on the dataset used and its sources.

## Motivation

- For what purpose was the dataset created? 
The Kaggle dataset was created to help with the "early diagnosis of COVID-19", as "X-ray machines are widely available" (https://www.kaggle.com/datasets/prashant268/chest-xray-covid19-pneumonia).
The dataset is suitable for research rather than industry models that can make official clinical diagnoses. 
- Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)? Who funded the creation of the dataset?
Prashant Patel created the Kaggle dataset.
The dataset is sourced from three places, each formed by a different research group and institution:
Source 1: Joseph Paul Cohen, Paul Morrison and Lan Dao [University of Montreal]
(https://github.com/ieee8023/covid-chestxray-dataset)
Source 2: Daniel Kermany, Kang Zhang, Michael Goldbaum [Guangzhou Women and Children's Medical Centre]
(https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
Source 3: Linda Wang, Alexander Wong, Zhong Qiu Lin, Paul McInnis, Audrey Chung, Hayden Gunraj [University of Waterloo, Canada]
(https://github.com/agchung/Figure1-COVID-chestxray-dataset)
 
## Composition

- What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? 
Images of patient chest X-rays that either have COVID-19, pneumonia or neither.
- How many instances of each type are there? 
           |   Train   |  Test  |  Total 

 Covid     |   460     |   116  |  576
 
 Normal    |   1266    |   317  |  1583
 
 Pneumonia |   3418    |   855  |  4273
- Is there any missing data?
No.
- Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by    doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?
Yes, as they are the X-rays of real life patients. The patients however are not identifiable through the X-rays.

## Collection process

- How was the data acquired? 
The dataset was collected from three publicly available data sources.
First source: From publicly available sources and "indirectly from hospitals and physicians"
Second source: During "patients’ routine clinical care". "Low quality or unreadable scans" were removed.
Third source: With the help of Figure 1. 
- If the data is a sample of a larger subset, what was the sampling strategy? 
Not specified.
- Over what time frame was the data collected?
Not specified.

## Preprocessing/cleaning/labelling

- Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? 
If so, please provide a description. If not, you may skip the remaining questions in this section. 
Unknown.
- Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? 
N/A.
 
## Uses

- What other tasks could the dataset be used for? 
Detecting pneumonia in patients.
- Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups 
(e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer 
could do to mitigate these risks or harms? 
Not in terms of the formatting of the X-rays. However, there are biases of the groups of people collected for the X-rays (for example one study was women and children only). This should be considered 
when using the dataset in the future. There are also unknown biases for the other data sources because the demographics of the X-rays are not evidently specified. The lack of 
labelling would also impact future usage, by reducing the quality of the descriptions of the data.
- Are there tasks for which the dataset should not be used? If so, please provide a description.
Detecting any diseases other than COVID-19 or pneuomonia. 

## Distribution

- How has the dataset already been distributed? 
The dataset is available to download as a zip file on Kaggle.
- Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?  
For the first source: licenses are provided for each image in a csv file but include Apache 2.0, CC BY-NC-SA 4.0, CC BY 4.0. Scripts are distributed under a  CC BY-NC-SA 4.0 license.
                      The research team must be contacted if companies intend to do anything other than carry out research using the data.
For the second source: The project is licensed under CC BY 4.0
For the third source: The project is licensed under GNU Affero General Public License 3.0

## Maintenance

- Who maintains the dataset?
The corresponding research groups stated above. However, the datasets have not been updated for several years (at minimum 2, at maximum 7, depending on the source).

