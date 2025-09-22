# Conversation-Management-Classification-using-Groq-API
Objective

This assignment demonstrates how to:
Manage conversation history with summarization and truncation.
Perform structured classification & extraction using Groq API’s OpenAI-compatible SDK with JSON schema validation.
The implementation is done in Google Colab without external frameworks (only standard Python + requests/openai).


 Configure API Key

Add your Groq API key (OpenAI-compatible) in the notebook:

import os
os.environ["OPENAI_API_KEY"] = "your_groq_api_key_here"

 Task 1: Conversation Management with Summarization
Features

Maintains running history of user–assistant messages.
Supports truncation by turns (last n messages) or by length (characters/words).
Performs periodic summarization after every k-th run using the Groq API.
Stores/updates summaries in history for long-running chats.

Demo
Feed multiple conversation samples.
Show outputs with different truncation limits.
Example: Summarization triggered every 3rd conversation turn.

 Task 2: JSON Schema Classification & Information Extraction
Features
Defines a JSON schema to extract 5 details:

name
email
phone
location
age

Uses Groq function calling (OpenAI SDK compatible) for structured responses.

Validates the output against the schema.

Demo
Parses at least 3 different sample chats.
Shows schema-validated outputs.

 How to Run

Open the notebook in Colab.

Insert your API key.

Run the cells for Task 1 and Task 2 sequentially.

Check printed outputs for:

Conversation summaries

JSON-extracted details
