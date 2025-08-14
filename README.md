Dream Weaver AI 🌙
An intelligent dream interpreter that combines the deep reasoning of Google's Gemini Pro with real-time web insights to provide concise and meaningful analysis of your dreams.
![python-badge](https://img.shields.io/badge/Python-3.9%2B-blue.svg)

![license-badge](https://img.shields.io/badge/License-MIT-green.svg)

![colab-badge](https://colab.research.google.com/assets/colab-badge.svg)

Short Description

Dream Weaver AI is a Python application that offers a multi-layered approach to dream interpretation. Instead of relying on a single source, it first generates a creative interpretation using the Gemini AI model. It then grounds this interpretation by fetching relevant symbolic meanings from the web. Finally, it synthesizes both sources into a short, coherent, and insightful summary, delivered in a structured JSON format.

Key Features

AI-Powered Interpretation: Leverages the advanced reasoning of Google's Gemini 1.5 Flash model for an initial deep analysis.
Web-Sourced Context: Uses the Serper API to fetch top Google search snippets for traditional dream meanings, adding a layer of conventional wisdom.
Unified Summary: Uniquely merges the AI interpretation and web insights, feeding them back into Gemini to produce a final, concise, and ultimate interpretation.
Configurable & Concise: Easily control the length of the output using max_output_tokens to ensure the interpretations are brief and to the point.
Secure Setup: Designed for use in Google Colab, utilizing the userdata module to securely manage API keys.
Structured Output: Delivers all information in a clean, predictable JSON object, perfect for integration into other applications.
How It Works
The application follows a simple yet powerful three-step process to generate its final interpretation:
code
Code

Step 1: User Input

The process starts when a user provides a query describing their dream (e.g., "I had a dream about falling from a great height").
Step 2: Dual-Path Analysis

The user's query is sent down two paths simultaneously for analysis:

Path A (AI Interpretation): The query is sent to the Google Gemini API to generate a creative and deep initial interpretation.
Path B (Web Context): The query is sent to the Serper API to fetch the top 3 most relevant web search snippets related to that dream's meaning.
Step 3: Synthesis and Summarization

The initial AI interpretation (from Path A) and the web snippets (from Path B) are combined into a single body of text.
This combined text is then sent back to the Google Gemini API with a new prompt asking it to merge and summarize all the information.
Step 4: Final Output

The Gemini API returns a final, concise, and unified interpretation.


Technology Stack
Language: Python 3
AI Model: Google Gemini 1.5 Flash
Web Search: Serper API (for Google Search Results)
Environment: Google Colab
Core Libraries: google-generativeai, requests, json
Setup and Usage
This project is optimized for use in a Google Colab notebook.
1. Prerequisites
A Google Account to use Google Colab.
A Google API Key. You can get one from Google AI Studio.
A Serper API Key from Serper.dev.
2. Configuration in Google Colab
Open a new Colab Notebook and paste the project's Python code into a cell.
Store Your API Keys Securely:
In your Colab notebook, click on the key icon (🔑) in the left sidebar.
Click "Add new secret".
Create a secret named GOOGLE_API_KEY and paste your Google API key as the value.
Create another secret named my-key and paste your Serper API key as the value.
Make sure to enable the toggle to make these secrets available to the notebook.
Install Libraries: Run this command in a code cell to install the required packages.
