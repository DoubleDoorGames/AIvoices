# Tacotron-2 for voice acting:
This Repository contains the implementation we used to synthesize voicelines for our game [Captain Starshot](https://www.doubledoorgame.com/captain-starshot/).  
Made by team [double door games](https://www.doubledoorgame.com/team/).
We are a team studying at the Breda University of Applied Sciences.

![](Logo_Buas.svg)

This is a modified version of the [Rayhane-mamah tacotron-2 implementation](https://github.com/Rayhane-mamah/Tacotron-2).  
The changes and have been made purely for educational purposes.  
all rights reserved to the respective owners.

# modifications:
I had to change the folder structure to make it easier to train multible voices. I added an argument to be able to give a model directory, which defaults to default.
This had to do with the requirement of easily synthesizing voicelines with diffrent voices.

because of limited training time I implemted transfer learning inside of the tacotron architecture based on the new folderstructure.
at default transfer learning is disabled.

# Datasets:
the datesets used for training the net are the [LJspeech dataset](https://keithito.com/LJ-Speech-Dataset/) and the english parts of the [M-ailabs dataset](https://www.caito.de/2019/01/the-m-ailabs-speech-dataset/).

# Setup:

for intructions for setting up the net please follow [Rayhane-mamah`s explanation](https://github.com/Rayhane-mamah/Tacotron-2/blob/master/README.md)

For additional information on the training arguments please check ([train.py](https://github.com/DoubleDoorGames/AIvoices/blob/master/train.py) & [synthesize.py](https://github.com/DoubleDoorGames/AIvoices/blob/master/synthesize.py))

# Repository Structure:
```
Tacotron-2  
    ├── datasets  
    ├── LJSpeech-1.1    
    │   └── wavs  
    ├── default ────logs-Tacotron   
    │  ├ name1 ─.. ├── eval_-dir  
    │  ├ name2 ─.. │   ├── plots  
    │  ├ name3 ─.. │   └── wavs  
    │  ├ name4 ─.. ├── mel-spectrograms  
    │  └ name5 ─.. ├── plots  
    │              ├── pretrained  
    │              └── wavs  
    ├── default ────logs-Wavenet     
    │  ├ name1 ─.. ├── eval-dir  
    │  ├ name2 ─.. │   ├── plots  
    │  ├ name3 ─.. │   └── wavs  
    │  └ name4 ─.. ├── plots  
    │              ├── pretrained  
    │              └── wavs  
    ├── default ────logs-Tacotron-2	  
    │  ├ name1 ─.. ├── eval-dir  
    │  ├ name2 ─.. │   ├── plots  
    │  ├ name3 ─.. │   └── wavs  
    │  ├ name4 ─.. ├── plots  
    │  └ name5 ─.. ├── taco_pretrained  
    │              ├── wave_pretrained  
    │              ├── metas  
    │              └── wavs  
    │  
    ├── tacotron  
    │   ├── models  
    │   └── utils  
    ├── tacotron_output   
    │   ├── eval  
    │   ├── gta  
    │   ├── logs-eval  
    │   │   ├── plots  
    │   │   └── wavs  
    │   └── natural  
    ├── wavenet_output    
    │   ├── plots  
    │   └── wavs  
    ├── training_data     
    │   ├── audio  
    │   ├── linear  
    │   └── mels  
    └── wavenet_vocoder  
        └── models  
```


# References and Resources:
- [Rayhane-mamah Tacotron-2](https://github.com/Rayhane-mamah/Tacotron-2)
- [double door games website](https://www.doubledoorgame.com/)
- [Original Tacotron paper](https://arxiv.org/pdf/1703.10135.pdf)
- [Breda University of Applied Sciences](https://www.buas.nl/)
  
