# YouTube Audio Mashup Generator

This project allows you to create a mashup of random audio clips from YouTube videos based on a specific singer or search term. It downloads audio from YouTube videos, extracts random segments, and merges them into a single mashup file.

## Features
- Downloads audio from YouTube videos using `yt-dlp`.
- Extracts random clips of specified duration from the audio files.
- Combines the clips into a single mashup audio file.
- Outputs the mashup as an MP3 file.

## Requirements
- Python 3.6+
- Required libraries:
  - `yt-dlp`
  - `pydub`
  - `random`
  - `os`
  - `sys`
  - `concurrent.futures`

## Installation

### Local Environment
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/YouTube-Mashup-Generator.git
   cd YouTube-Mashup-Generator
   ```
2. Install the required libraries:
   ```bash
   pip install yt-dlp pydub
   ```
3. Install FFmpeg (required by `pydub`):
   - **Windows**: Download FFmpeg from [FFmpeg.org](https://ffmpeg.org/download.html) and add it to your PATH.
   - **macOS**: Install via Homebrew:
     ```bash
     brew install ffmpeg
     ```
   - **Linux**: Use your package manager, e.g.,
     ```bash
     sudo apt update && sudo apt install ffmpeg
     ```

### Google Colab
1. Open the Colab notebook and copy the provided code.
2. Install dependencies directly in Colab:
   ```bash
   !pip install yt-dlp pydub
   ```

## Usage

### Local
Run the program with the following syntax:
```bash
python <program.py> <SingerName> <NumberOfVideos> <AudioDurationInSeconds> <OutputFileName>
```
Example:
```bash
python mashup.py "Sharry Maan" 15 5 mashup.mp3
```

### Google Colab
1. Modify the parameters in the script:
   ```python
   singer_name = "Sharry Maan"
   num_videos = 15
   audio_duration = 5
   output_filename = "mashup.mp3"
   ```
2. Run the Colab notebook and download the generated mashup using the download link provided.

## How It Works
1. **Video Search**:
   - Searches YouTube for videos matching the specified singer or search term.
2. **Audio Download**:
   - Downloads the audio track of each video in the best available format.
3. **Audio Processing**:
   - Converts the audio to WAV format (if necessary).
   - Extracts random segments of the specified duration.
4. **Mashup Creation**:
   - Combines the extracted segments into a single MP3 file.

## Project Structure
```
YouTube-Mashup-Generator/
├── audios/               # Directory for downloaded audio files
├── output/               # Directory for the final mashup output
├── mashup.py             # Main script for mashup generation
├── README.md             # Project documentation
```

## Troubleshooting
- **FFmpeg Not Found**:
  Ensure FFmpeg is installed and added to your system's PATH.
- **Audio Not Downloaded**:
  Check your internet connection and ensure the YouTube videos are accessible.
- **Permission Issues**:
  Run the script with appropriate permissions or modify the output directory.

## Contributing
Feel free to submit issues or pull requests to improve the project. Contributions are welcome!

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) for seamless YouTube downloading.
- [pydub](https://github.com/jiaaro/pydub) for audio manipulation.
- [FFmpeg](https://ffmpeg.org/) for audio processing.

