# Local-LLM-Deployment-and-Interaction

# Running LLMs Locally: Llama3 and Gemma7B

This repository contains instructions and scripts to set up and run two language models (LLMs), Llama3 and Gemma7B, locally on your machine. By following this guide, you'll be able to interact with both models using the `curl` command.

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Setup Instructions](#setup-instructions)
   - [Llama3](#llama3)
   - [Gemma7B](#gemma7b)
4. [Usage](#usage)
5. [Comparison](#comparison)
6. [Repository Structure](#repository-structure)
7. [Video Demonstration](#video-demonstration)
8. [Conclusion](#conclusion)
9. [References](#references)

## Introduction

This project demonstrates how to download, install, and run two large language models, Llama3 and Gemma7B, on a local machine. The goal is to interact with these models using the `curl` command and compare their performance on identical prompts.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- Python 3.7 or higher
- Git
- Docker (recommended for easier setup)
- curl
- A suitable text editor or IDE (e.g., VSCode)

## Setup Instructions

### Llama3

1.  **Download Llama3:** Follow the instructions on the official [Llama3](https://ollama.com/library/llama3) to download and set up the model.

2.  **Install Dependencies:**

pip install -r requirements.txt

3.  **Run Llama3 Model:**

python run\_llama3.py

4.  **Verify Setup:** You can verify if Llama3 is running correctly by using the `curl` command:

curl -X POST http://localhost:5000/predict -d '{"prompt": "Hello, Llama3!"}'

### Gemma7B

1.  **Download Gemma7B:** Follow the instructions on the official [Gemma7B](https://ollama.com/library/gemma) to download and set up the model.
2.  **Install Dependencies:**

pip install -r requirements.txt

3.  **Run Gemma7B Model:**

python run\_gemma7b.py

4.  **Verify Setup:** Similar to Llama3, verify the setup using `curl`:

curl -X POST http://localhost:6000/predict -d '{"prompt": "Hello, Gemma7B!"}'

## Usage

After setting up both models, you can interact with them via the `curl` command.

### Llama3 Interaction

curl -X POST http://localhost:5000/predict -d '{"prompt": "Tell me a joke."}'

### Gemma7B Interaction

curl -X POST http://localhost:6000/predict -d '{"prompt": "Tell me a joke."}'

## Comparison

To compare the performance of both models, you can pass the same prompt to each model and observe their responses. This helps in understanding the strengths and weaknesses of each model.

## Repository Structure

.
├── llama3/
│   ├── run_llama3.py
│   ├── requirements.txt
│   └── ...
├── gemma7b/
│   ├── run_gemma7b.py
│   ├── requirements.txt
│   └── ...
├── README.md
└── setup_instructions.md


## Video Demonstration

A video demonstration of setting up and interacting with both models is available at: [YouTube Link](https://youtu.be/9CvIERY34p4)

## Conclusion

This project provided hands-on experience in setting up and running LLMs locally. By comparing the responses from Llama3 and Gemma7B, we gained insights into their capabilities and performance.

## References

*   [Llama3](https://ollama.com/library/llama3)
*   [Gemma7B](https://ollama.com/library/gemma)
*   [Medium Article: 50 Open Source Options for Running LLMs Locally](https://medium.com/thedeephub/50-open-source-options-for-running-llms-locally-db1ec6f5a54f)
