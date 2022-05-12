# Functional Specification

- [1. Introduction](#1-introduction)
  - [Team](#team)
- [2. Definitions of terms](#2-definitions-of-terms)
- [3. In-depth](#3-in-depth)
- [4. Data collection](#4-data-collection)
- [5. Privacy and confidentiality](#5-privacy-and-confidentiality)
- [6. Use cases](#6-use-cases)

---



## 1. Introduction

The goal of this project is to create a device. It would listen to conversations and detect whether the language is English or French. The students will not interact with the device.

A color will be emitted following the language spoken (green for good English, red for French, and blue for other languages).

We have 9 weeks to complete this project, from April 25th to June 24th, 2022.

### Team

The team will be composed of:

- Clémentine CUREL as Project Manager
- Louis DE LAVENNE DE CHOULOT DE CHABAUD-LA-TOUR as Tech Leader
- Max BERNARD
- Léo CHARTIER
- Thomas PLANCHARD
- Quentin CLEMENT



## 2. Definitions of terms

| Terms | Definition |
| ----- | ---------- |
| Artificial intelligence (AI) | Ability of a computer or a robot controlled by a computer to do tasks that are usually done by humans because they require human intelligence and discernment. |
| Deep Learning | Concept of computers simulating the process a human brain takes to analyze, think and learn. The deep learning process involves something called a Neural Network as a part of the thinking process for an AI. It takes an enormous amount of data to train Deep Learning and a considerably powerful computing device for such computation methods. |
| Hardware | Physical and electronic parts of a computer or other piece of equipment, opposite to the software which corresponds to the programs and instructions that run on the computer. |
| Machine learning | Subfield of artificial intelligence, which is broadly defined as the capability of a machine to imitate intelligent human behavior. Artificial intelligence systems are used to perform complex tasks in a way that is similar to how humans solve problems. Machine learning is one way to use AI. |



## 3. In-depth

To go further in-depth on this project, this software will have to be an Artificial Intelligence using Deep Learning.
The AI should be trained to recognize which language people are talking in.

The produced device should be provided with a light that would change color depending on the spoken language:
- Red when speaking French.
- Green when speaking English.

And to go further, the device may also detect accents and use more colors of the light:
| Light green | English with a small English accent     |
| Orange      | English with a very French accent       |
| Yellow      | English with both accents               |
| Blue        | Other language or unrecognized language |
The color gradient would depend on the accents as represented in this picture:

<img src="./pictures/Color chart.png">



## 4. Data collection

One of the crucial points of this project is the training of the AI. To do so, a lot of data (voice recording) is needed.
There are two ways to get such data:

The first way is to record the people in our building by placing microphones in the rooms. The advantage of this method is that the data is more consistent with one of the use cases for the device.
On the other hand, there are many disadvantages like the reliability of the data. We would need to listen to all the recordings to make sure the subjects are speaking French when we need it and English when we need it.

The second way is to use data from the internet with a bank of data. The advantage is the number of data that we can have very quickly. Moreover, there are no real disadvantages.



## 5. Privacy and confidentiality

The records will not be kept in a cloud to detect a language. Thanks to this, we will not need to store the live conversation. The device will detect the language and delete the record afterward.

The encryption of some information may be required to ensure security and confidentiality. The device will not connect to the internet to save the data. This will also make the device difficult to hack because it would require physical contact with the device.



## 6. Use cases

This device can have multiple use cases:

First of all, it may be used to automatically select the origin language on an automatic translator.

Secondly, it could be used worldwide in schools to make sure students speak English in English classes and not in their native language.
An example would be, at ALGOSUP, an all-English French school of computer science, if a student were to speak French during project time, the police would be alerted and would take them into custody.
