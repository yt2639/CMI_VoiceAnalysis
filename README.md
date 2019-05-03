# CMI_VoiceAnalysis

Updated on April 26, 2019

1. The speaker diarization has been already realized using VB-Diarization on docker.

2. Changed the function to real-time recording and transcribing speech to text using 'speech_recognize' package.

==================================================================================================================
Posted on Mar 15, 2019

Currently, there are two parts.

1. Batch feature extraction of voice features on Python using OpenSMILE. These features were then used for SVM to classify Hyperfun_dysfunction patients (70 people) and healthy people (56 people) (just a very simple demo so the accuracy is not high yet).

2. Jon told me that we basically want to replicate the function of LENA app using open-source tools. I've gone through the official website as well as its tutorial youtube video and some reviews. I found it seems like doing three things for autism diagnosis:
(a). **Adult Word Count**. To count how many normal words the speaker says (eh, em, ah, etc. do not count)
(b). **Frequency of vocalizations**. I think it refers to how many words the speaker says in a unit time, like 30 words/min.
(c). **Conversational turns**. How many times the speaker communicates with others.

So, for (a) and (b), I thought we could just transcribe speech to text and do the job. I used *speech_recognition* package in Python with "Google Web Speech API" to transcribe. The accuracy is good but "eh, em, ah" this kind words will not be transcribed.
Besides, I did an experiment that it seems this API will not transcribe other speakers and only transcribe the 1st speaker it hears. I am working on how to solve these problems.

For (c), I found several APIs in Python could be used to do speaker recognition.

SIDEKIT from LIUM

Bob toolkit from Idiap

Speaker diarization from ISCI

I was using SIDEKIT but it's to some extent complicated so I want to make sure if I am going towards the correct direction before fully devoting to learn this API.




