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

### Prerequisites
Ensure you have the following installed on your system:
* **Python 3.8+**
* **FFmpeg (External):** While the code avoids system installation, `yt-dlp` and some internal tools may rely on `ffmpeg` existing in the background for optimal performance.

### Setup Steps
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/adilla203/shark-tank-pitch-analyzer-adilla](https://github.com/adilla203/shark-tank-pitch-analyzer-adilla)
    cd shark-tank-pitch-analyzer
    ```

2.  **Install Dependencies:** **Strict version pinning is required** (`moviepy<2.0` and `decorator<5.0`) to avoid the common `ImportError` and `TypeError` conflicts.
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  Open the `shark_tank_full_analysis.py` script.
2.  Set the `URL` variable at the bottom of the script to any YouTube pitch video you wish to analyze (e.g., the default Scrub Daddy pitch).
3.  Run the script from your terminal:
    ```bash
    python shark_tank_full_analysis.py
    ```

### Expected Output
The script will output the results of the tone analysis, the overall calculated Business Score (0-100), and personalized, randomized verdicts from the four virtual investor personas.
