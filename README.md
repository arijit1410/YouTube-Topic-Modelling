# YouTube-Topic-Modelling
Topic clustering of audio taken from youtube interviews.

## Requirements
* google-api-python-client==1.6.4
* httplib2==0.10.3
* oauth2client==4.1.2
* pyasn1==0.4.2
* pyasn1-modules==0.2.1
* rsa==3.4.2
* six==1.11.0
* SpeechRecognition==3.8.1
* tqdm==4.19.5
* uritemplate==3.0.0

## Generating audio from youtube videos

Run ``` video2audio.py ``` to generate a .wav file from the youtube video url. Change the url in the code accordingly.

## Converting audio to text 

You will need a google cloud API key. ``` api-key.json ``` contains the credentials. 
Since google cloud API only works for 1 minute videos, the videos are broken down into 30 seconds frames, just to be safe.

Use this command on your terminal.

``` ffmpeg -i source/genevieve.wav -f segment -segment_time 30 -c copy parts/out%09d.wav ```

## Topic clustering

Refer to ``` lda.ipynb ``` for a detailed explanation.