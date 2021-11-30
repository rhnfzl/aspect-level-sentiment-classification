# Aspect-level Sentiment Classification

## Objective

Build a aspect-level classification model based on document-level and aspect-level data as proposed in [Exploiting document knowledge for aspect-level sentiment classification](/reading/exploiting_document_knowledge_for_aspect-level_sentiment_classification.pdf). Build an attention-based aspect-level sentiment classification model with Bidirectional Long Short Term Memory networks (BiLSTM). Your model shall include:

* BiLSTM network that learns sentence representations from input sequences (Recommend to use Bidirectional provided by Keras to define the BiLSTM network).
* Attention network that predicts sentiment label, given the representation weighted by the attention score.
* Fully connected network that predicts sentiment label, given the representation weighted by the attention score

Requirements:

* You shall train your model based on transferring learning. That is, you need first train your doc-level model on document-level examples. Then the learned weights will be used to initialize aspect-level model and fine tune it on aspect-level examples.
* You shall use the alignment score function in attention network as same as the recommended
![equation](https://latex.codecogs.com/gif.latex?f_{score}(h,&space;t)=tanh(h^{T}W_{a}t))
* You shall evaluate trained model on the provided test set and show the accuracy on test set.

### Data Description

Document-level and aspect-level data sets can be [downloaded from](https://surfdrive.surf.nl/files/index.php/s/AytwhaLUbIGRsCt). The raw data set contains two domains: 

1. Restaurant reviews; and 

2. Electronics reviews, use ```lt_14``` as experimental data.