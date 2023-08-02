# Customer Scenario Simulator
This solution offers the opportunity to simulate customer scenarios, enabling you to practice and improve your customer service skills effectively. It generates personas and issues for realistic conversational roleplay with an AI chatbot, providing a valuable learning experience. Furthermore, it offers automated feedback on your performance, helping you track your progress and identify areas for improvement. All conversations can be saved as text or PDF files for future reference. Powered by VertexAI and responsible AI techniques, this solution ensures high-quality conversations.

# Domain & Concept Knowledge

## Use Cases

Customer engineers can simulate customer scenarios to gain experience on how to handle different types of requests. This can help them to provide better customer service and resolve issues more quickly in real-life situations. They also get to practice their communication and problem-solving skills in a low-stakes environment.

Seeing the value in practice simulations. I believe that developing a program for this particular use-case can:

- Provide valuable insights and support for a variety of customer scenarios in the cloud.
- Review best practices when interacting with customers. 
- Provide feedback to customer interactions in a learnable and low-stakes environment.

## Why Generative AI?

Generative will enable this simulator tool to generate text interactions that represent the different ways that a customer might interact with a business. It will also enable this tool to analyze any responses provided by the user and use that to generate actionable feedback.

## Problem Formulation

There are several initiatives within Google Cloud like RPG Arena and Pitch World Cup that provide customer engineers with the opportunity to role play customer interactions. However, these initiatives are not always scalable and tailored to the growth and development of an individual customer engineer in Google Cloud. Thus it is important to provide a solution that is personable and scalable for **_all customer engineers_**.

## Potential Risks & Mitigation

Since we cannot accurately predict what responses we will get from the model we used. There is a tendency for the model to produce outputs/feedback that is offensive, misleading or biased. 

Additionally, the model could generate scenarios that do not reflect a given scenario.

These risks will be carefully considered in the following ways:

- Provide an adequate amount of training examples to ensure responses are within a given context.
- Utilize prompt engineering techniques like few-shot prompting and other stop-gaps and guardrails that ensure a limited set of responses.  
- Incorporate a level of reinforcement learning to ensure outputs are accurate.

## Requirements

A customer engineer should be able to:

- Simulate how a customer would interact with a cloud business across different scenarios.
- React to these scenarios
- Receive feedback based on their responses. 
- Decipher best practices and patterns from these interactions.
- Share these best practices and patterns with other customer engineers.

# System Architecture

This solution will utilize a Google Collab Notebook that will send an API call to a VertexAI Generative Studio model. The model will then send a response back to the notebook. Additionally, the solution can save its responses in either a .pdf or .txt format in a Cloud Storage Bucket.

Within VertexAI, I will be utilizing ChatBison to interact with the customer and TextBison to provide feedback based on the conversation. 

![Architecture](Architecture.png)

# Design

The Customer Scenario Simulator is designed to automatically generate customer service scenarios and enable customer service agents to practice resolving issues through conversational chat.


## Key features

- Generate random customer personas and issues
- Chatbot powered conversations with the customer (ChatBison) 
- Automated feedback on agent's performance (TextBison)
- Save conversations as text files or PDFs
- Upload files to Cloud Storage

## Prompt Design Workflow

Here are the few-shot prompts that were used for each model:
