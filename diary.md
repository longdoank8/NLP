
**Start Date:** March 2023
<br/>
**Goal:** Create webapp for ai based dubbing 
<br/>
*For customers*: provide dubbed video


## March

* research and study paper about video dubbing, lip syncing
* install and run open source repositories (Google Dubber, wav2lip)

## 1.week
* Google Dubber: uses 3 google cloud APIs (translation, TTS, STT)
* convert mp4 in wav-file, diarize, punctuation recognizer and time recognizer
* puts sentences with timestamp in json-file and translates it and saves it into multiple mp3-files
* call TTS API, different voices can be chosen
* mp3-file combined with mp4-file
* problems: translation incorrect, adaptive speaking rate too fast, umlaute pronounced incorrectly, can't reconize brands

## 2.week
* wav2lip needs muted video and audio with the same length
* face has to be always visible, no black or blurry frames
* most models trained for detecting english

## 3.week
* run various tests on different videos
* established a working pipeline using python scripts, Google APIs and wav2lip


## April

* ocotillo works → transcription saved in tsv.file
* openNMT (New! v3 English-German - Transformer Large) (https://opennmt.net/Models-py/)
* transformer doesn’t work well, needs training 
* use audio → transcribe → synthesize voice with tortoise 
* tortoise too slow → use coqui.ai (TTS) 
* --model_name "tts_models/en/ljspeech/glow-tts" --vocoder_name "vocoder_models/en/ljspeech/univnet"
* TTS needs a TTSmodel and a vocoder because tts is comprehensive system including a vocoder 
* problem: TTS can't take txt.files as input only terminal inline text 
* solution: export SAMPLE=`cat sample.txt` and use $SAMPLE as input variable 

## 13. April

* TODO: further test coqui.ai (voice synthesizer), install and test unsupervised generative video dubbing (alternative to wav2lip lip syncing)


