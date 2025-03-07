# Fake News & Deepfake Detection Chrome Extension

## Overview
CodeWiz is a Chrome extension designed to help users identify **fake news and deepfake videos**. It integrates **Google Fact Checker API** and **News API** to verify news credibility and provide related articles. Additionally, it includes a **deepfake detection feature** where users can upload videos for analysis. This project also incorporates **NatWest Hackathon's Deepfake Detection Model**, enhancing its ability to detect manipulated content.

## Features
- **News Verification:** Highlights selected news and analyzes its credibility using Google Fact Checker API.
- **Related Articles:** Fetches similar news articles from trusted sources using News API.
- **Deepfake Detection:** Redirects users to a webpage where they can upload videos for deepfake analysis using an AI model.
- **Integrated NatWest Hackathon Model:** Utilizes a deepfake detection system built with CNN + ResNeXt + LSTM for analyzing videos.
- **User-Friendly Interface:** Simple and intuitive Chrome extension UI for quick verification.

## Installation & Setup
### Prerequisites
- Google Chrome
- API Keys for Google Fact Checker API & News API
- Python 3.12
- Required dependencies (listed below)

### Steps

#### Load the Extension in Chrome:
1. Open Chrome and go to `chrome://extensions/`
2. Enable **"Developer mode"** (top-right corner)
3. Click **"Load unpacked"** and select the `codewiz` directory

#### Configure API Keys:
- Update `config.js` with your **Google Fact Checker API** and **News API** keys.

#### Set Up the Deepfake Detection Server:
```sh
cd deepfake_detection
pip install -r requirements.txt
uvicorn app:app --host 0.0.0.0 --port 8000

The server will run locally at http://localhost:8000/
Usage
Select any news text on a webpage and the extension will analyze it.
Click the extension icon to see verification results and related articles.
Use the "Check Deepfake" button to upload a video for deepfake detection.
Deepfake detection results are provided using the NatWest Hackathon's AI model.
Tech Stack
Frontend: JavaScript, HTML, CSS (Chrome Extension UI)
Backend: Python (FastAPI for deepfake detection)
APIs: Google Fact Checker API, News API
Machine Learning: CNN, ResNeXt, LSTM for deepfake detection
Database: Firebase (for storing news verification results)
API Integration
Google Fact Checker API
Used to verify the credibility of news articles.

News API
Fetches related news articles from various sources.

Deepfake Detection API
Runs a deepfake detection model on uploaded videos and returns probability scores for manipulation.

Contributing
Contributions are welcome! Feel free to submit issues and pull requests.

License
This project is licensed under the MIT License.
