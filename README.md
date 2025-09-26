# Rice Classification Project

## Introduction
This project focuses on the classification of five rice varieties: Arborio, Basmati, Ipsala, Jasmine, and Karacadag. Initially, a Convolutional Neural Network (CNN) was implemented as a baseline model. While the CNN showed promising results for some classes, it struggled significantly with distinguishing between Basmati and Karacadag, leading to poor performance on these categories. To address this issue, Transfer Learning was later applied using MobileNetV2 as the base model, which resulted in a substantial improvement in classification accuracy.

## Metrics

### CNN Model Results
The CNN achieved an overall accuracy of approximately 74%. It performed well on Arborio and Ipsala, but struggled heavily with Karacadag, which was almost never recognized correctly. Most Karacadag samples were misclassified as Basmati, which explains the high recall but low precision for the Basmati class. Jasmine was classified with moderate success, showing that the CNN could not fully capture the differences between similar classes.

### Transfer Learning Results
After applying Transfer Learning with MobileNetV2, the model achieved an accuracy of 95.6%. Performance improved drastically across all classes, with both precision and recall values being consistently high. Arborio, Ipsala, and Basmati reached near-perfect classification. Jasmine and Karacadag also showed strong improvements, with recall values significantly better than those of the CNN model. Overall, the use of Transfer Learning solved the major misclassification issues seen in the baseline model.

## Additional Work
Beyond building and evaluating the models, interpretability methods were applied. Grad-CAM and Eigen-CAM visualizations were generated to better understand which regions of the rice images influenced the model’s predictions. This provided transparency and helped validate that the model was focusing on relevant image features for classification.

## Conclusion and Future Work
In conclusion, while the CNN baseline struggled with specific rice varieties, the Transfer Learning approach using MobileNetV2 proved highly effective, resulting in strong overall performance and balanced class metrics. Future improvements could include experimenting with fine-tuning additional layers of the pre-trained model, testing other advanced architectures, or deploying the model with a simple user interface for practical use cases. Expanding the dataset with more diverse samples could also enhance robustness. This project demonstrates the effectiveness of Transfer Learning in image classification tasks where baseline models face difficulties in distinguishing between visually similar classes.

## Kaggle Notebook

You can also check the project on Kaggle:  
https://www.kaggle.com/code/pelinkoz/rice-classification-cnn
