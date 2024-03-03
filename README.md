# WhisperAI
 
This repository provides Python code utilizing the `openai-whisper` library to transcribe audio files from a specified folder and save the transcripts to corresponding text files.

### Installation

1.  Prerequisites:

    -   Python 3.8-3.11
    -   `pip` package manager
2.  Install dependencies: Run the following command in your terminal:

    Bash

    ```
    pip install openai-whisper ffmpeg tqdm

    ```

### Usage

1.  Clone or download the repository: Obtain the code by cloning the repository or downloading the files.

2.  Modify configuration variables: Open the Jupyter Notebook file (`*.ipynb`) and adjust these variables at the beginning:

    -   `root_folder`: The path to the directory containing your audio files (e.g., `C:/Users/YOURUSER/Documents/`).
    -   `exit_folder`: The path to the directory where you want to save the transcripts (e.g., `C:/Users/YOURUSER/Documents/`).
    -   `audio_ext`: The extension of your audio files (e.g., `.m4a`, `.mp3`, `.wav`).
    -   `language`: The language of your audio files (e.g., `it` for Italian).
3.  Run the code: Execute the Jupyter Notebook file via the appropriate command or by opening it in a Jupyter Notebook environment.

### Available Models and Languages

Whisper offers various model sizes with different accuracy and efficiency levels:

| Size | Parameters | English-only Model | Multilingual Model | Required VRAM | Relative Speed |
| tiny | 39 M | tiny.en | tiny | ~1 GB | ~32x |
| base | 74 M | base.en | base | ~1 GB | ~16x |
| small | 244 M | small.en | small | ~2 GB | ~6x |
| medium | 769 M | medium.en | medium | ~5 GB | ~2x |
| large | 1550 M | N/A | large | ~10 GB | 1x |

drive_spreadsheetExport to Sheets

Whisper supports multiple languages, but performance may vary. Refer to the official documentation for details: <https://github.com/openai/whisper>

### Additional Notes

-   This code requires `ffmpeg` to be installed on your system. Refer to the official documentation for installation instructions: <https://ffmpeg.org/>
-   The code assumes your audio files are within the `root_folder` or its subdirectories. You might need to modify the searching logic for different file structures.
-   The provided example demonstrates Italian transcription. Update the `language` variable for other languages.
