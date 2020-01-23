## A Deep Multi-task Contextual Attention Framework for Multi-modal Affect Analysis

For the evaluation of our proposed multi-task CIM framerwork, we use benchmark multi-modal dataset i.e, MOSEI which has both sentiment and emotion labels.

### Dataset

* You can download datasets from [here](https://drive.google.com/open?id=1vavqHJshjwhKnt_hUqgXr8ZsHkt7u16I).

* Download the dataset from given link and set the path in the code accordingly make two folder (i) results and (ii) weights.

-------------------------------------------------------
### For multi-task sentiment and emotion classification
#### For MOSEI Dataset:
For trimodal-->>  python trimodal_sentiment_class_emotion_class.py  

#### Emotion Results Extractor

Follow these steps to extract the threshold based results for emotion:

* Open the text file i.e., multiTask_emotion_results_extractor.txt
* Copy and paste on the terminal

###### For preference F1 score:

If the result file name is trimodal_emo.txt then run the following command 

* cat trimodal_emo.txt |  grep "average" | grep -P "Threshold:" | sort -k 6,6  | tail -1 | cut -d$'\t' -f'5' >> Emotion-Multi-task.txt

So based on threshold, desired output will be stored in Emotion-Multi-task.txt (preference is F1-score)

###### For preference W-Acc:

If the result file name is trimodal_emo.txt then run the following command 

* cat trimodal_emo.txt |  grep "average" | grep -P "Threshold:" | sort -k 7,7  | tail -1 | cut -d$'\t' -f'6' >> Emotion-Multi-task.txt

So based on threshold, desired output will be stored in Emotion-Multi-task.txt (preference is W-Acc)

-------------------------------------------------------

### --versions--

python: 2.7

keras: 2.2.2

tensorflow: 1.9.0
