## Reading Text in the Wild with CNN

end-to-end text recognition using non-deeplearning methods to select adjacent bounding boxes and cnn to revise bounding boxes and classify.

#### key points

* Extract - Proposal - Bounding box regression - Recognition - Threshold
* Edge boxes + Aggregate Channel Feature Detector for Extraction
* random forest classfier for Proposal
* CNN for bounding box regression
* CNN for recognition of words

#### thoughts

* End-to-end is an awesome feature
* Unable to train bounding box detection
* Maybe attention algorithm can be used to detect text from an image