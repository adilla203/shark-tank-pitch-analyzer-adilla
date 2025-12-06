# Shark Tank Pitch Analyzer (Free & Local Edition)

An AI-powered tool that analyzes business pitches from YouTube videos (like Shark Tank) to predict investment success. 

Unlike other tools that require expensive APIs (GPT-4) or complex system installations (FFmpeg), this project is designed to run **100% locally and free** using smart rule-based NLP and signal processing.

## Features

* **Zero Cost Architecture:** Uses Google's Free Speech Recognition and local Python logic instead of paid OpenAI credits.
* **Vocal Tone Analysis:** Uses `Librosa` to measure the speaker's energy, confidence, and vocal expressiveness in the critical first 90 seconds.
* **Smart Speaker Separation:** Differentiates between the "Pitcher" and the "Sharks" by analyzing sentence context (e.g., filtering for "I/We/Our" statements vs. questions).
* **Dependency-Free Audio:** Uses `MoviePy`'s internal tools to process audio, eliminating the need for a system-wide FFmpeg installation.
* **The Virtual Shark Panel:** Simulates feedback from 4 distinct investor personas:
    * *The Finance Shark* (Focuses on margins & sales)
    * *The Visionary* (Focuses on patents & energy)
    * *The Customer Advocate* (Focuses on problem clarity)
    * *The Skeptic* (Focuses on risks)

## Installation

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd shark-tank-analyzer
