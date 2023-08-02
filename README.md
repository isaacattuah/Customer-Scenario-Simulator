# Customer Scenario Simulator

This project uses Vertex AI and Generative models to simulate customer service scenarios for practice.

## Overview

The goal is to provide a tool for customer engineers to gain experience handling different customer interactions in a low-stakes environment.

It generates a random customer persona (angry, impatient etc) and technical issue category (networking, storage etc). The engineer then has a conversational chat with the AI-powered customer bot to resolve the issue.

After the chat, an AI model provides feedback on the interaction. Conversations are saved as text or PDF files, and uploaded to cloud storage.

![Architecture](Architecture.png)

## Models Used

The models that were selected from Generative AI Studio in Vertex AI were:

* `chat-bison` for powering conversations with the simulated customer
* `text-bison` for generating feedback on the engineer's performance

## Features
* Generate random customer personas and cloud tech issues
* Chatbot for natural conversations
* Automated feedback system
* Save chats as text/PDF
* Upload to cloud storage bucket
* Jupyter notebook interface

## Setup
The notebook requires a Google Cloud Project with the following APIs enabled:

* Vertex AI API
* Cloud Storage API
  
Install the required libraries:

```
pip install shapely
pip install google-cloud-aiplatform
pip install google-cloud-storage
pip install fpdf
```

Update the notebook with your Cloud Project ID, Region, and Bucket name.

## Usage
* Run the cells to initialize the libraries, models and generate a sample customer scenario
* Chat with the persona by typing messages
* Type `EXIT` to end the conversation
* The next cell will generate feedback
* Further cells handle saving as text/PDF and uploading to cloud storage

## References
* [Vertex AI Documentation](https://cloud.google.com/vertex-ai/docs)
* [Test chat prompts](https://cloud.google.com/vertex-ai/docs/generative-ai/chat/test-chat-prompts)

