# Technical Specification #

---

- [Technical Specification](#technical-specification)
  - [1. Introduction](#1-introduction)
    - [a. Overview](#a-overview)
    - [b. Glossary of Terminology](#b-glossary-of-terminology)
    - [c. Context](#c-context)
    - [d. Goal](#d-goal)
    - [e. Out of Scope](#e-out-of-scope)
  - [2. Solutions](#2-solutions)
    - [a. Existing Solutions](#a-existing-solutions)
    - [b. Suggested Solution](#b-suggested-solution)
    - [c. Retained Solutions](#c-retained-solutions)
  - [3. Further Considerations](#3-further-considerations)
    - [a. Security and privacy](#a-security-and-privacy)
    - [b. Risks](#b-risks)
  - [4. Impact of the project](#4-impact-of-the-project)
  - [5. Work](#5-work)
    - [a. Work estimates and timelines](#a-work-estimates-and-timelines)
    - [b. Milestones](#b-milestones)
    - [d. Future work](#d-future-work)
  - [6. End Matter](#6-end-matter)
    - [a. References](#a-references)
    - [b. Acknowledgments](#b-acknowledgments)
  
---

<br>

## 1. Introduction

### a. Overview

This product has to detect the language of a conversation, either English or French.
When a language is detected, an LED will be lit with a color matching the language.

### b. Glossary of Terminology

|                              |                                                                                            |
| ---------------------------- | ------------------------------------------------------------------------------------------ |
| Arduino                      | Microcontroller board that is used to control the electronics in the product.              |
| Artificial Intelligence (AI) | Process of using data to learn patterns and predict future behavior.                       |
| CSV                          | Comma-separated values: Type of file where the data are separated by a comma.              |
| Deep Learning                | Machine Learning concept to simulate the human way of learning using a big amount of data. |
| Greyscale                    | Image type in which only the intensity information is stored, not the colors.              |
| Image                        | Two-dimensional object that is typically displayed on a computer monitor.                  |
| Kaggle                       | Website that allows us to download datasets from the internet and use an online GPU.       |
| Language detection           | Process of detecting the language of a conversation.                                       |
| Machine Learning (ML)        | Process of using data to learn patterns and predict future behavior.                       |
| Neural Network (NN)          | Series of linked neurons similarly to a human brain.                                       |
| Numpy                        | Python library adding support for multi-dimensional arrays, and mathematical functions.    |
| Pandas                       | Python library used for data analysis, including CSV file manipulation.                    |
| Raspberry Pi                 | Microcontroller more performant than the Arduino.                                          |
| Tensorflow                   | Machine learning library that is used to train a model.                                    |

### c. Context

The client is the director of a Computer Science school based in France.
The particularity of this school is that everything is in English with students from all over the world.
As such, most of the conversations are not in English when outside of the classes.

This is why the client requested a language detection system, to force the students to speak English.

### d. Goal

Our client wants a device able to detect the language of a conversation between English and French using an AI.
An accent recognition system will be implemented.

This program should make use of Tensorflow and run on light hardware, as required by the client.

### e. Out of Scope

For the future, we have been thinking about how to improve the device, we want to add more languages like Spanish, Arabic, etc.
We also want to add a voice assistant to correct English mistakes made by users and to give them a better experience.

<br>

## 2. Solutions

### a. Existing Solutions

Many AIs can detect the language of a conversation between English and French.
If we take, for example, Siri, Alexa, or Google Traduction/home, they can detect the language spoken by the user.
The big difference between many of them and our AI is that they can only detect the language if the user previously configured the device with his voice.

### b. Suggested Solution

We initially wanted to have our AI on an Arduino Nano BLE but for the same price, we were able to acquire hardware better fitting the project, the raspberry pi 4.

We don't use Google Collab's GPUs to train our model because they are of the older model `Tesla P80`.
We can't let training run overnight.
The size of our google drive limits our dataset size.

We could pre-process data as they are loaded, using CSV and Pandas.
But this makes it hard to work with Keras DataGenerator.

### c. Retained Solutions

We decided to use a more powerful Raspberry Pi 4.
We will record sound over a 10s period, then convert this stream of data to an image using a MEL spectrogram.
Finally, the AI would take the image as an input and output a probability of it being English or French.

We use Tensorflow and Keras python library to train and run our model.
These are popular libraries that we are taught in class.

We train our model with Kaggle so that we can use GPUs of the newest model `Tesla P100` and unlimited size Dataset.

To process and load the images, we will make the conversion using a `Multiprocess.Pool` to go faster, and once they are processed, we upload the image to a Kaggle dataset.
We will use Keras DataGenerator FlowFromDirectory to load all the images before training.

<br>

## 3. Further Considerations

### a. Security and privacy 

The device will not be connected to the Internet to do the recognition, it will be independent.
The conversation data will be used for language recognition and never be stored.
The main goal is to protect the device and the user from potential hacks or data leaks.

### b. Risks

For this kind of project, we have multiple risks, especially around audios.

**Noises with voices**

Having noises in a voice recording can prevent the AI from predicting the correct language.

To solve this problem you can add a function to your code to add noises to audio.

**Different accents**

In the future, ALGOSUP will have students from all over the world that have accents different from the french which is why the AI will make a probability between 0.5 and 1 to do the accent rating.

If we want to evaluate accents other than French in a certain case, we will need to add more language recognition.

**Background noises**

When people work on a computer, they often make some noises with their keyboard, mouse, or anything else.
If the noises impede the recognition, the light will turn blue.

**No sounds**

Sometimes in a project room, there may be absolutely no sound or noise, in this case, the device will not light up an LED.

<br>

## 4. Impact of the project

The final goal of this project is to detect spoken language.
If we take the example of the ALGOSUP school, detecting the language spoken in English class would allow the teacher to know if someone is speaking French when the teacher is not nearby.
Practice is essential in learning a language and the device can encourage this practice.

<br>

## 5. Work

### a. Work estimates and timelines

| Task                      | Duration | Description                                                                                                                      |
| ------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Functional specifications | 1 week   | Understand the scope of the project, plan, and create personal functional specifications. Ask the client for some clarifications |
| Technical specifications  | 1 week   |                                                                                                                                  |
| Get data                  | 1 week   | Find, download, and unzip the data                                                                                               |
| Familiarization           | 3 days   | Look at and plot the data                                                                                                        |
| Preparation               | 1 week   | Split, clean, and organize the data then format it into fixed-sized images                                                       |
| Modeling                  | 3 weeks  | Create a model, train, test, fine-tune, repeat                                                                                   |
| Hardware                  | 1 week   | Put the software on the hardware (Raspberry) and make sure it works                                                              |

### b. Milestones

- Finding an English and a french voice dataset on the Internet
- Converting the audio data into a spectrogram to be compatible with the model
- Creating a model able to analyze a spectrogram and determine the spoken language between French and English
- Training the model with the labeled data
- Testing the model with random data (and improve the model until the accuracy during the test reach 96%)
- Inserting the model on the raspberry pi

### d. Future work

<br>

## 6. End Matter

### a. References

<https://pub.towardsai.net/spoken-language-recognition-using-convolutional-neural-networks-6aec5963eb18>
<https://github.com/fraunhofer-iais/language-recognition>
<https://commonvoice.mozilla.org/en/datasets>

### b. Acknowledgments

During this project, we will be accompanied and helped by a few people and it is important to thank them.
To begin with, we will follow Jackie Boscher's lessons for a few weeks to learn artificial intelligence, deep learning, and python.
Finally, we would like to thank Franck Jeannin and the ALGOSUP school for their advice, help, and materials.
