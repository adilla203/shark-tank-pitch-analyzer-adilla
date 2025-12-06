# Shark Tank Pitch Analyzer

An AI tool that analyzes business pitches from YouTube videos, like Shark Tank, to predict investment success.

This project runs entirely locally and free. It uses smart rule-based NLP and signal processing. Unlike other tools, it does not need expensive APIs or complex system setups.

## Features

* **No Cost Structure:** Utilizes Google's Free Speech Recognition and local Python logic instead of paid OpenAI credits.
* **Vocal Tone Analysis:** Employs `Librosa` to assess the speaker's energy, confidence, and vocal expressiveness in the key first 90 seconds.
* **Smart Speaker Separation:** Tells apart the "Pitcher" and the "Sharks" by analyzing sentence context, filtering for "I/We/Our" statements and questions.
* **Dependency-Free Audio:** Leverages `MoviePy`'s internal tools to process audio, removing the need for a system-wide FFmpeg installation.
* **The Virtual Shark Panel:** Simulates feedback from four distinct investor personas:
    * *The Finance Shark* (Focuses on margins and sales)
    * *The Visionary* (Focuses on patents and energy)
    * *The Customer Advocate* (Focuses on problem clarity)
    * *The Skeptic* (Focuses on risks)

## Installation

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd shark-tank-analyzer
