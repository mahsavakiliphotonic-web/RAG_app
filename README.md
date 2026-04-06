# RAG_app
AI-Powered RAG Document Chatbot
This project implements a Retrieval-Augmented Generation (RAG) pipeline using FlowiseAI. It allows users to upload PDF documents and interact with the content through an intelligent chat interface. The system ensures that the AI's responses are grounded in the provided technical documents, reducing hallucinations and providing high-accuracy information.

🚀 Project Overview
The architecture is designed to handle document processing, embedding generation, and conversational retrieval in a unified low-code environment.

📸 Project Workflow
Note: Replace the placeholder above with the image you sent me.

🛠️ Technical Components & Architecture
The system is built using the following core modules:

1. Data Ingestion & Processing
Pdf File Loader: Handles the initial upload of the source documents.

Recursive Character Text Splitter: * Chunk Size: 1000 characters.

Chunk Overlap: 200 characters.

Purpose: Ensures the text is broken down into manageable pieces while maintaining contextual continuity between chunks.

2. Vector Embeddings & Storage
Google Gemini Embedding: Uses the gemini-embedding-001 model to convert text chunks into high-dimensional vectors.

In-Memory Vector Store: Acts as a temporary database to store and retrieve these vectors quickly during the search phase (Top K = 4).

3. Language Models & Logic
MistralAI (Chat Model): Uses the mistral-tiny model (Temperature: 0.9) to generate human-like responses based on the retrieved data.

Conversational Retrieval QA Chain: The "brain" of the project that connects the Vector Store, the Chat Model, and the memory to provide coherent answers.

Buffer Memory: Stores the conversation history so the chatbot can handle follow-up questions.

📊 Project Report (For Academic Submission)
Project Title: Implementation of a RAG-based Conversational Agent for PDF Intelligence

Objective: To bridge the gap between static document storage and interactive information retrieval using LLMs.

Methodology
The project follows a modular design:

Preprocessing: Documents are split using a recursive strategy to preserve semantic meaning.

Vectorization: Google's state-of-the-art embedding models are used for semantic representation.

Retrieval: An In-Memory vector search identifies the top 4 most relevant chunks for any user query.

Generation: A Mistral-based LLM synthesizes the final answer using the retrieved context.

Key Results
Contextual Accuracy: The system successfully limits answers to the scope of the uploaded PDF.

Efficiency: Using stdio/In-Memory storage allows for rapid prototyping and low-latency responses.

Scalability: The modular nature allows for easy replacement of the mistral-tiny model with larger models like GPT-4 or Gemini Pro for more complex tasks.

<img width="1883" height="830" alt="image" src="https://github.com/user-attachments/assets/efc56603-2442-4d09-b252-68223d1c0e23" />

⚙️ How to Run
Install FlowiseAI.

Import the JSON configuration for this flow.

Configure your API keys for:

MistralAI

Google Gemini

Upload your target PDF and start chatting!

<img width="1883" height="830" alt="image" src="https://github.com/user-attachments/assets/3bf591af-6412-4bf4-90b1-93020f5695ba" />
