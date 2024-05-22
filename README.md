Gemini Quizify is an AI-driven tool designed to dynamically generate quizzes from user-provided documents. The primary goal of the tool is to enhance the learning experience by providing instant feedback and detailed explanations, thus reinforcing the understanding of various topics.

Introduction

Gemini Quizify leverages advanced AI technology to create customized quizzes based on the content of uploaded documents. Whether you're a student looking to reinforce your knowledge or an educator aiming to create engaging assessments, Gemini Quizify provides an efficient and interactive solution.

Features

Document Ingestion: Upload PDF documents for quiz generation.
Embedding Creation: Utilize Vertex AI for creating embeddings from document content.
Quiz Generation: Automatically generate quiz questions based on the uploaded documents.
Interactive UI: User-friendly interface built with Streamlit for easy quiz interaction.
Instant Feedback: Receive immediate feedback and explanations for quiz answers.
Installation
Prerequisites
Python 3.7+
Streamlit
Google Cloud SDK
Necessary Python libraries (see requirements.txt)

Steps

Clone the Repository

pip install -r requirements.txt

Set Up Google Cloud

Create a Google Cloud account and project.

Enable Vertex AI APIs.

Set up a service account with the necessary permissions and download the JSON key file.

Set the environment variable for the Google Cloud credentials:

export GOOGLE_APPLICATION_CREDENTIALS="path/to/your-service-account-file.json"

Usage

streamlit run task_10.py
Upload Documents

Use the provided interface to upload PDF documents.
Generate Quiz

Enter the topic for the quiz and select the number of questions.
Click "Generate" to create the quiz.
Take the Quiz

Answer the questions displayed.
Receive instant feedback and explanations.

Components

DocumentProcessor
Handles the ingestion and processing of PDF documents.

EmbeddingClient
Initializes the embedding creation using Vertex AI.

ChromaCollectionCreator
Stores and manages the document embeddings in a Chroma collection.

QuizGenerator
Generates quiz questions based on the processed documents and embeddings.

QuizManager
Manages the quiz flow, including question navigation and answer validation.
