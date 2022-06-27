# Deep Fake Video generator

This repository implements Deep fake video generation of a celebrity, from a textual input. The user should provide a textual input, source, target languages and choose the celebrity.
The input text will be translated to the target language, the audio will be generated and lipsynced with the chosen celebrity.
  
## Introduction
Generating the Deep Fake videos consist of 5 steps.  
- The pipeline of the Generating Deep Fake Video is shown in below image:-
 ![image](https://user-images.githubusercontent.com/97409925/175902151-cf53dbfe-7925-4506-b99b-36ca7b70f514.png)

# 1. Text to Text
   About the Model used:
- It is a Convolutional Neural Network
- It falls under the FairSeqMachineTranslation (FSMT) Models
- It was Trained on Facebook Posts and Messages
- Found on Huggingface under “facebook/wmt19-de-en”

# 2. Text to Speech
- In this step we are generating speech from text.
- For this we are using TACATRON from Google.
- It is a GAN(Generative Adversarial Network)
 
# 3. Voice Cloning



# 4. Lip Sync
- Model Used “Wav2Lip”
- Lip-synching a video to any audio containing speech with high level of accuracy.
-It uses Generative Adversarial Networks(GANs)
-In this step we are taking the output of voice cloning and combining with the video and we will get the result of Lip Syncing video

## Steps to run
Open the file **DeepFake_Generator_GradioUI.ipynb** in Google colab and execute. The gradio interface can be used to input a German text and choose a celebrity. The video will be displayed after execution.

## Reference projects Used


