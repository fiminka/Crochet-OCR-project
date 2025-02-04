# Extracting On-Screen Text from YouTube Crochet Tutorials using OCR

## Overview
This project automates the extraction of on-screen text from YouTube crochet tutorials using Optical Character Recognition (OCR). Many tutorials contain valuable instructions as embedded text, which are not available for direct download. Our solution processes these videos, extracts the text, and converts it into a structured PDF format for easier reference and accessibility.

## Features
- Downloads YouTube videos containing crochet tutorials.
- Extracts on-screen text using OCR.
- Processes and refines extracted text using post-processing techniques.
- Saves extracted text into a structured PDF format.
- Provides statistical analysis on extracted text data.

## Tech Stack & Dependencies
The project is built in **Python** and utilizes the following libraries:
- [`easyocr`](https://github.com/JaidedAI/EasyOCR) - For extracting text from video frames.
- [`cv2`](https://pypi.org/project/opencv-python/) (OpenCV) - For image preprocessing.
- [`yt_dlp`](https://github.com/yt-dlp/yt-dlp) - For downloading YouTube videos.
- [`numpy`](https://numpy.org/) - For numerical operations.
- [`matplotlib`](https://matplotlib.org/) - For visualizing data, including plotting graphs and displaying images.
- [`scikit-learn`](https://scikit-learn.org/) - For machine learning tasks such as feature extraction and calculating metrics.
- [`networkx`](https://networkx.org/) - For creating networks and graph structures.
- [`tqdm`](https://github.com/tqdm/tqdm) - For progress visualization.
- [`torch`](https://pytorch.org/) - For deep learning computations (required by EasyOCR).
- [`re`](https://docs.python.org/3/library/re.html) - For regex-based text processing.
- [`deep-text-recognition-benchmark`](https://github.com/clovaai/deep-text-recognition-benchmark) - For fine-tuning OCR models.

## Project Structure
```
│── data
│   ├── marchewka                   # Carrot dataset
│   ├── patterns                    # Carrot dataset
│   ├── train                       # Train dataset
│   ├── test                        # Test dataset
│   ├── marchewka_regex.txt         # Carrot labels after regex
│   ├── marchewka.txt               # Carrot labels
│
│── notebooks
│   ├── extract_text.ipynb          # OCR methods & text extraction
│   ├── statistics.ipynb            # Analysis of extracted text
│   ├── accuracy.ipynb              # Accuracy tests on outputs in different stages
│   ├── post_processing.ipynb       # Cleaning & formatting OCR output
│   ├── main.ipynb                  # Main project pipeline with PDF extraction
│   ├── Roboto                      # Font folder needed for PDF generation
│
│── .gitignore                      # Files and folders to be ignored by Git
│── README.md                       # Project documentation
│── requirements.txt                # Dependencies list
```

## Installation & Setup
### Prerequisites
Ensure you have Python (<3.11) installed. Create a virtual environment and install the dependencies.

```bash
# Clone the repository
git clone https://github.com/wust-research-group/final-machine-learning-project-crochetteam
cd final-machine-learning-project-crochetteam

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt

#clone deep-text-recognition-benchmark
git clone git@github.com:clovaai/deep-text-recognition-benchmark.git
```

## Results & Statistics
The extracted text can be analyzed using `statistics.ipynb`, which provides:
- Word frequency analysis.
- Accuracy evaluation against ground truth data.
- Character distribution statistics.
- Exploratory Data Analysis (EDA).

## Contributors

<table>
<tr>
    <td align="center" style="word-wrap: break-word; width: 150.0; height: 150.0">
        <a href=https://github.com/fiminka>
            <img src=https://avatars.githubusercontent.com/u/81615393?v=4 width="100;"  style="border-radius:50%;align-items:center;justify-content:center;overflow:hidden;padding-top:10px" alt=Wiktoria Fimińska/>
            <br />
            <sub style="font-size:14px"><b>Wiktoria Fimińska</b></sub>
        </a>
    </td>
    <td align="center" style="word-wrap: break-word; width: 150.0; height: 150.0">
        <a href=https://github.com/AMysliwiec>
            <img src=https://avatars.githubusercontent.com/u/82213599?v=4 width="100;"  style="border-radius:50%;align-items:center;justify-content:center;overflow:hidden;padding-top:10px" alt= Alicja Myśliwiec/>
            <br />
            <sub style="font-size:14px"><b>Alicja Myśliwiec</b></sub>
        </a>
    </td>
    <td align="center" style="word-wrap: break-word; width: 150.0; height: 150.0">
        <a href=https://github.com/grzesiaaa>
            <img src=https://avatars.githubusercontent.com/u/81617044?v=4v=4 width="100;"  style="border-radius:50%;align-items:center;justify-content:center;overflow:hidden;padding-top:10px" alt=Julia Grzegorzewska/>
            <br />
            <sub style="font-size:14px"><b>Julia Grzegorzewska</b></sub>
        </a>
    </td>
</tr>
</table>


