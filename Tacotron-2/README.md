# Tacotron-2 for voice acting:
This Repository contains the implementation we used to synthesize voicelines for our game [insert game name]().

This is a modified version of the [Rayhane-mamah tacotron-2 implementation](https://github.com/Rayhane-mamah/Tacotron-2).


# modifications:
I had to change the folder structure to make it easier to train multible voices. I added an argument to be able to give a model directory, which defaults to default.

because of limited training time I implemted transfer learning inside of the tacotron architecture based on the new folderstructure.
at default transfer learning is disabled.

go to [train.py]() to see all arguments


# Datasets:
the datesets used for training the net are the [LJspeech dataset](https://keithito.com/LJ-Speech-Dataset/) and the english parts of the [M-ailabs dataset](https://www.caito.de/2019/01/the-m-ailabs-speech-dataset/).



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
- [double door games blog](https://www.doubledoorgame.com/)
