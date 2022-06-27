# Deep Fake Video generator

This repository implements Deep fake video generation of a celebrity, from a textual input. The user should provide a textual input, source, target languages and choose the celebrity.
The input text will be translated to the target language, the audio will be generated and lipsynced with the chosen celebrity.
< To be filled >
  
## Introduction
Generating the Deep Fake videos consist of 5 steps. 
![image](https://user-images.githubusercontent.com/97409925/175902151-cf53dbfe-7925-4506-b99b-36ca7b70f514.png)

# 1. Text to Text
   About the Model used:
- It is a Convolutional Neural Network
- It falls under the FairSeqMachineTranslation (FSMT) Models
- It was Trained on Facebook Posts and Messages
- Found on Huggingface under “facebook/wmt19-de-en”

# 2. Text to Speech

# 3. Voice Cloning
# 4. Lip Sync

## Steps to run
Open the file **DeepFake_Generator_GradioUI.ipynb** in Google colab and execute. The gradio interface can be used to input a German text and choose a celebrity. The video will be displayed after execution.
< To be filled >

## Reference projects Used
< To be filled >
