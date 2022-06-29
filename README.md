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

- Voice cloning is the process of generating the speech of real individual using computer. 
- applying AI algorithms to replicate their unique voice in a similar manner.
- In this project we are using Tacatron from google
- Tacatron is a Generative Adversarial Network(GAN)
- Three componets are improtant for Voice cloning
   1. Encoder - The task of an encoder network is to take audio from a specific speaker as input and turn it into a low-dimensional vector embedding that captures the features of that speaker's speech. It is just concerned with the speaker's manner of speaking; it gives little thought to what they are saying.
   2. Synthesizer -  is the fundamental model of text-to-speech. It creates a spectrogram of the relevant text input after receiving the phoneme sequence as input.       Phonemes are individual components of a word's sound. Each phrase is broken down into these phonemes, and the model's input sequence is created.
   3. Vocoder -  is a type of audio processor that records the distinctive features of an audio stream and then applies those elements to other audio signals.
   
   
   ![image](https://user-images.githubusercontent.com/97409925/176412003-35d83d8c-7428-4fa0-b580-d8903e662d49.png)



# 4. Lip Sync
- Model Used “Wav2Lip”
- Lip-synching a video to any audio containing speech with high level of accuracy.
- It uses Generative Adversarial Networks(GANs)
- In this step we are taking the output of voice cloning and combining with the video and we will get the result of Lip Syncing video

## Steps to run
- Open the file **DeepFake_Generator_GradioUI.ipynb** in Google colab and execute.
- Before executing the project make sure that colab runtime is GPU runtime.
- The gradio interface can be used to input a German text and choose a celebrity. The video will be displayed after execution.


- Input text to the gradio UI

![image](https://user-images.githubusercontent.com/97409925/176398857-68eb8da4-7739-4109-8913-1708c976a7a9.png)

- Selecting the celebrity

![image](https://user-images.githubusercontent.com/97409925/176399018-9dea8648-54ad-4337-806a-67163d1a097f.png)

- Final output video of the selected celebrity
 
![image](https://user-images.githubusercontent.com/97409925/176399681-e8627116-4440-4c00-be60-6c1ea98f76d8.png)


## Reference projects Used

- [Transfer Learning from Speaker Verification to Multispeaker Text-To-Speech Synthesis](https://arxiv.org/abs/1806.04558)
- [Real_time_Voice_Cloning](https://github.com/CorentinJ/Real-Time-Voice-Cloning)
- [Lip Sync](https://github.com/Rudrabha/Wav2Lip)


