
**Start Date:** March 2023
<br/>
**Goal:** Create webapp for ai based dubbing 
<br/>
*For customers*: provide dubbed video


## First week 

* 
* 
* 

## Second week

* 
* 

## Third week

* 
* 

## April

* ocotillo works → transcription saved in tsv.file
* openNMT (New! v3 English-German - Transformer Large) (https://opennmt.net/Models-py/)
* transformer doesn’t work well, needs training 
* test with google APIs
* use translated audio → transcribe → synthesize voice with tortoise 
* tortoise too slow → use coqui.ai TTS 
* --model_name "tts_models/en/ljspeech/glow-tts" --vocoder_name "vocoder_models/en/ljspeech/univnet"
* TTS needs a TTSmodel and a vocoder because tts is comprehensive system including a vocoder 
* The best sounding in my opinion is tts_models/en/ljspeech/fast_pitch and vocoder_models/en/ljspeech/hifigan_v2
* They are specified in the corpus which has a speaker_ids file, but in coqui they got scrambled, see #2258
* At least as of three months ago in January when I ran a script to generate all the voices, these were American accents in Coqui's VCTK-VITS:  256 M, 257 F, 270 F, 287 M, 293 F, 317 M, 360 F (may not be all) 