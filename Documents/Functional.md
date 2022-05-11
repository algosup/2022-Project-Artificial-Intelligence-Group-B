# Functional Specification

- [Functional Specification](#functional-specification)
  - [1. Introduction](#1-introduction)
    - [Team](#team)
  - [2. Definitions of terms](#2-definitions-of-terms)
  - [3. In-depth](#3-in-depth)
  - [4. Data collection](#4-data-collection)
  - [5. Privacy and confidentiality](#5-privacy-and-confidentiality)
  - [6. Use cases](#6-use-cases)

---

## 1. Introduction

To put you in the context, ALGOSUP is a school where all our classes are in English, but the students still talk in French during their project time.  

This project aims to listen to conversations during project time and detect when they talk in English or French. The students will not interact with the device.

This will be a device to make sure that the students talk in English during project time.  A color will be emitted following the language spoken (green for good English, red for French, and blue for other languages)

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
|--|--|
| Machine learning | Machine learning is a subfield of artificial intelligence, which is broadly defined as the capability of a machine to imitate intelligent human behavior. Artificial intelligence systems are used to perform complex tasks in a way that is similar to how humans solve problems. Machine learning is one way to use AI. |
| AI | Artificial intelligence (AI) is the ability of a computer or a robot controlled by a computer to do tasks that are usually done by humans because they require human intelligence and discernment. |
| Deep learning | Deep Learning, is the concept of computers simulating the process a human brain takes to analyze, think and learn. The deep learning process involves something called a neural network as a part of the thinking process for an AI. It takes an enormous amount of data to train deep learning and a considerably powerful computing device for such computation methods. |
| Hardware | The physical and electronic parts of a computer or other piece of equipment, rather than its software. |

## 3. In-depth

To go furthermore in depth in this project, this software will have to be an artificial intelligence with deep learning of the language.

We want you to train your AI to recognise which language the students are talking. 

To do that, a device should be provided where it will have a light or multiple lights. 
- The light will be red when the students speak French.
- The light will be green when the students speak English.

And to go further,
- The light will be light green when they speak English with a small English accent.
- The light will be yellow when they speak English with both accent.
- The light will be orange when they speak English with a very French accent.
- The light will be blue when the AI doesn’t recognise the language speaking.

So the graduation of color will depend on the accent of the students.

<img src="./pictures/Color chart.png">

## 4. Data collection

To collect data we have thought about two different ways. The first way is to collect many records of all the students in ALGOSUP just by putting a microphone in the room. The advantage of this way of collecting is that the data are more consistent with the usefulness of the device.

On the other hand, there are many disadvantages like the reliability of the data because we need to listen to all the recordings to be sure that students are speaking French when we need it and English when we need it.

To solve this problem we can also record students in the English class to be sure that they speak in English and record them during the meal to make sure they speak in French.

The second way is to use data from the internet with a bank of data. The advantage is the number of data that we can have very quickly and there are no real disadvantages.

## 5. Privacy and confidentiality

We think that it is not necessary to record and keep the records in a cloud to detect a language. Thanks to this we will not need to store the live conversation, the device will detect the language and delete the record after it.

We may encrypt some information to ensure security and confidentiality. We don’t want to connect it to the internet to save the data. It will also make the device difficult to hack because to hack it we will need to have a physics contact with the device.

## 6. Use cases

This device can have multiple use cases:

First of all, it may be used to automatically select the origin language on an automatic translator.

Secondly, it could be used worldwide in middle school to reprimendate the students that speak in their native language in the back of the class during English lessons without disturbing the teacher or the rest of the class.
An example would be, at ALGOSUP, an all-English French school of computer science, if a student were to speak French during project time, the police would be alerted and would take them into custody.
