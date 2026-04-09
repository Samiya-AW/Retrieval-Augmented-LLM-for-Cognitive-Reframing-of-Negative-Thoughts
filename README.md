# LLM-Based Cognitive Reframing for Negative Thoughts

Overview

This project implements a retrieval-augmented Large Language Model (LLM) system for cognitive reframing of negative thoughts. The system is inspired by research on human–AI interaction for mental health support.

It combines semantic retrieval with an instruction-tuned LLM to generate balanced and rational responses to distorted thoughts.

Dataset

The system uses the publicly available cognitive reframing dataset from:

Cognitive Reframing of Negative Thoughts through Human–Language Model Interaction

Each record contains:

Situation
Distorted Thought
Rational Reframe

Methodology

The system follows a simple and effective pipeline:

Embedding Generation
Used SentenceTransformers (all-MiniLM-L6-v2) to convert thoughts into vector representations.
Semantic Retrieval
Retrieved top-k similar thought–reframe pairs using cosine similarity.
Prompt Construction
Built structured prompts using retrieved examples.
LLM Generation
Generated reframes using an open-source instruction-tuned model
(TinyLlama/TinyLlama-1.1B-Chat-v1.0).
Example

Input Thought:
I am a complete failure.

Generated Reframe:
Failing one exam does not define your abilities. It is an opportunity to learn and improve.

Tech Stack
Python
Pandas
PyTorch
SentenceTransformers
HuggingFace Transformers
TinyLlama (1.1B Chat Model)
Google Colab
Key Features
Retrieval-augmented generation (RAG)
Fully open-source (no paid APIs)
Context-aware reframing using real dataset examples
Simple, reproducible pipeline
Future Work
Improve prompt design for more structured CBT responses
Compare retrieval-only vs LLM-based approaches
Add automatic evaluation metrics for generated reframes
