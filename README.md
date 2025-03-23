# AI-Chatbot

This project is a Python-based chatbot that uses Google Generative AI (Gemini) and Langchain to help answer questions related to Governance, Risk, and Compliance (GRC). It leverages knowledge extracted from multiple PDF documents on key GRC topics to provide informed responses.

## Features

- **PDF Text Extraction**: Extracts content from multiple PDF files related to GRC, including frameworks like COSO, NIST, GDPR, and the Sarbanes-Oxley Act.
- **Generative AI Model**: Uses the Google Generative AI (Gemini) model to provide context-aware responses to user queries.
- **Chat History**: Maintains a conversation history, which helps the assistant provide more accurate and relevant responses over time.
- **API Integration**: Connects to the Google Generative AI model using an API key, which must be set in the environment.
- **Response Formatting**: The chatbot's responses are structured in JSON format, displaying the topic, summary, sources, and tools mentioned.

## Requirements

- Python 3.x
- Required Python packages:
  - `langchain`
  - `python-dotenv`
  - `pydantic`
  - `langchain-google-genai google-generativeai`
  - `PyPDF2`
  
## Code
Two variations were created: one where the PDF data is directly included in the prompt, and another where the data is stored separately as a knowledge base.
`Code1` is data in prompt 
`Code2` is data stored in knowlage base 

## Outputs 
Each version is asked ten questions, with their token usage, response times, and answers recorded for comparison.

