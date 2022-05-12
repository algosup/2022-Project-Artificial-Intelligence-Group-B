# Technical Specification # 

---
- [1. Introduction](#1-introduction)
    - [a. Overview, Problem Description, Summary, or Abstract](#a-overview-problem-description-summary-or-abstract)
    - [b. Glossary of Terminology](#b-glossary-of-terminology)
    - [c. Context or Background](#c-context-or-background)
    - [d. Goals or Product and Technical Requirements](#d-goals-or-product-and-technical-requirements)
    - [e. Non-Goals or Out of Scope](#e-non-goals-or-out-of-scope)
    - [f. Future Goals](#f-future-goals)
- [2. Solutions](#2-solutions)
    - [a. Current or Existing Solution / Design](#a-current-or-existing-solution--design)
    - [b. Suggested or Proposed Solution / Design](#b-suggested-or-proposed-solution--design)
    - [c. Alternate Solutions / Designs](#c-alternate-solutions--designs)
- [3. Further Considerations](#3-further-considerations)
    - [a. Security and privacy considerations](#a-security-and-privacy-considerations)
    - [b. Risks](#b-risks)
- [4. Success Evaluation](#4-success-evaluation)
    - [a. Impact](#a-impact)
- [5. Work](#5-work)
    - [a. Work estimates and timelines](#a-work-estimates-and-timelines)
    - [b. Prioritization](#b-prioritization)
    - [c. Milestones](#c-milestones)
    - [d. Future work](#d-future-work)
- [6. End Matter](#6-end-matter)
    - [a. References](#a-references)
    - [b. Acknowledgments](#b-acknowledgments)
  
---



<br>

## 1. Introduction


### a. Overview, Problem Description, Summary, or Abstract

This product has to detect the language of a conversation between English and French. When one langue will be detected, the user must be warned he is talking in this language.

### b. Glossary of Terminology
|                              |                                                                               |
| ---------------------------- | ----------------------------------------------------------------------------- |
| Arduino                      | Microcontroller board that is used to control the electronics in the product. |
| Artificial Intelligence (AI) | Process of using data to learn patterns and predict future behavior.          |
| Keras                        | Machine learning library that is used to train a model.                       |
| Language detection           | Process of detecting the language of a conversation.                          |
| Machine Learning             | Process of using data to learn patterns and predict future behavior.          |
| Tensorflow                   | Machine learning library that is used to train a model.                       |

### c. Context or Background

The client is the director of a Computer Science school based in France. The particularity of this school is that everything happens in English even though all the students are French. But the students have a hard time complying with this rule. As such, most of their conversations take place in French when outside of the classes.

This is why the client requested a language detection system, to force the students to speak English.

### d. Goals or Product and Technical Requirements

Our client wants a device that will detect the language of a conversation between English and French. To do that we need to create an AI which can detect the difference between the two languages.

This program should make use of Tensorflow and run on an Arduino Nano 33 BLE Sense, as required by the client.

### e. Non-Goals or Out of Scope

<!-- TODO Product and technical requirements that will be disregarded -->

### f. Future Goals

For the future, we have been thinking about how to improve the device, we want to add more languages like Spanish, Arabic, etc. We also want to add a voice assistant to correct English mistakes made by users and to give them a better experience.



<br>

## 2. Solutions

### a. Current or Existing Solution / Design

That exists many AI capable to detect the language of a conversation between English and French. If we take for example Siri, Alexa, or Google Traduction all of them can detect the language spoken by the user. The big difference between many of them and our AI is that they are capable to detect the language only if the user configured the device with his voice.

### b. Suggested or Proposed Solution / Design

We want to use Arduino to put our AI in and connect it to a light. The AI would take images as input and output the language. Those images would be spectrograms of the conversation.

### c. Alternate Solutions / Designs



<br>

## 3. Further Considerations

### a. Security and privacy considerations

The device will not be connected to the Internet to do its language search, it will be independent. The conversation data will be used for language search and will be deleted once processed. The main goal is protect the device and the user from potential hacks or data leaks.

### b. Risks



<br>

## 4. Success Evaluation

### a. Impact



<br>

## 5. Work

### a. Work estimates and timelines

### b. Prioritization

### c. Milestones

### d. Future work



<br>

## 6. End Matter

### a. References

### b. Acknowledgments
