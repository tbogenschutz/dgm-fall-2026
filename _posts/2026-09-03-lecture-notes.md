---
layout: distill
title: Lecture Notes from Lecture 1
description: Course Overview and Intro to Machine Learning
date: 2026-09-03

lecturers:
  - name: Ben Lengerich
    url: "https://adaptinfer.org"

authors:
  - name: Erin Bogenschutz
  - name: Tori Bogenschutz
  - name: Natasha Ziman

editors:
  - name: Editor 1 # editor's full name
    url: "#" # optional URL to the editor's homepage

abstract: >
  This lecture introduced the course and the foundations of machine learning. It covers information from the syllabus including grading, the course webpage, and office hours. It also introduced the definition of machine learning, the different categories of machine learning, and machine learning jargon and notation.
---

## Course Overview

### About the Course
STAT 453 introduces the fundamental concepts, methods, and tools used in machine learning, deep learning, and generative modeling. The course focuses on understanding both the ideas behind machine learning methods and how to apply them in practice. 

Find details on course logistics, schedule, lecture notes, and assignments on the course website at https://adaptinfer.org/dgm-fall-2026.

### Instructors
**Professor Ben Lengerich**

Email: lengerich@wisc.edu

Office Hours: Thursdays from 11:00 am to 12:00 pm in Morgridge 5530

Professor Lengerich's research blends data science with medicine using context-adaptive models to understand diseases and improve precision medicine.


**TA Baiheng Chen**

Email: bchen342@wisc.edu

Office Hours: TBD


### Grading
- Homework: 20%
- Midterm Exam: 20%
  - Tentatively on 10/25
  - In-Class, Open-note, No calculator/phone
- Final Exam: 30%
  - Scheduled 12/12
  - Location TBA, Open-note, No calculator/phone
- Final Project: 30%
- Lecture Notes: Up to 5% of extra credit
  - 2% of extra credit for signing up to write notes for a lecture
    - Sign up here: https://docs.google.com/spreadsheets/d/1sRF3iMyxBJqUcGnHgSN8OMbAY7Los42bnqg_hYgCMlI/edit?usp=sharing
    - Template here: https://adaptinfer.org/dgm-fall-2026/notes/lecture-notes-template/
  - 3 x 1% of extra credit for editing a peer's notes

Grades will not be curved
- A: 93-100
- AB: 88-92
- B: 83-87
- BC: 78-82
- C: 70-77
- D: 60-69
- F: Below 60

### Homeworks/Project
Late homework submissions via Canvas will incur a penalty of 10% per day for up to three days, then they will not be accepted.

The project is broken down into parts. The proposal (5%), midway report (5%), presentation (5%), and report (15%). Teams of up to four students are allowed.

---

## What is Machine Learning?

Machine learning (ML) is a way of creating programs that improve their performance at a task through experience. More formally, a program is considered to learn from experience $E$ with respect to a task $T$ and performance measure $P$ if its performance at task $T$, as measured by $P$, improves with experience $E$.

This definition can be broken down into three important components:

- **Task ($T$):** What the machine learning system is trying to accomplish.
- **Experience ($E$):** The data or interactions that the system learns from.
- **Performance measure ($P$):** How we determine whether the system is performing well.

Traditional programming and machine learning differ in how the program is created. In traditional programming, the programmer provides a program that takes inputs and produces outputs. In machine learning, the computer uses inputs and outputs to learn a program.

<img src="{{ '/assets/img/notes/traditional-programming-ml.png' | relative_url }}" />

**Figure 1:** Comparison of traditional programming and machine learning.

### Three Fundamental Questions in Machine Learning

When building a machine learning system, there are three fundamental questions to consider:

1. **Representation:** How should we represent the problem and the information contained in the data?
   
   In probabilistic form, suppose we have variables $X_1, X_2, \ldots, X_8$. To represent the joint distribution of all eight variables, if each variable is Boolean, there are $2^8 = 256$ possible configurations of the variables. By using the conditional independence relationships between variables, a graphical model can represent the same joint distribution using far fewer parameters.

2. **Inference:** Given the representation, what can we conclude or predict about unknown information?
   
   In probabilistic form, suppose we want to determine the probability of one variable given another:

   $$
   P(X_8 \mid X_1)
   $$

   Using the definition of conditional probability:

   $$
   P(X_8 \mid X_1) = \frac{P(X_8, X_1)}{P(X_1)}
   $$

   If the other variables are unobserved, we can marginalize over them:

   $$
   P(X_8 \mid X_1) =
   \frac{\sum_{X_2,\ldots,X_7} P(X_1,\ldots,X_8)}
   {P(X_1)}
   $$

   For Boolean variables, this requires summing over $2^6$ configurations of the six unobserved variables. Independence assumptions can simplify this calculation. Graphical models can be useful because they provide an intermediate representation between explicitly representing every possibility and assuming complete independence.

3. **Learning:** How can we use available data or experience to learn the appropriate model? What model is "right" for the data?
   
   In probabilistic form,

   $$
   M = \underset{M \in \mathcal{H}}{\operatorname{argmax}} \; F(D; M)
   $$

   where:

   - $M$ is the selected model.
   - $\mathcal{H}$ is the hypothesis space, or set of possible models.
   - $D$ is the available data.
   - $F(D; M)$ is a function that evaluates how well model $M$ fits or performs on the data.

   An important question in learning is how to constrain the hypothesis space $\mathcal{H}$ so that we can efficiently search for a useful model rather than considering every possible model.

---

## The Broad Categories of ML

---

## The Supervised Learning Workflow

---

## Necessary ML Notation and Jargon

---

## About the Practical Aspects and Tools

---

## 

---

## 
