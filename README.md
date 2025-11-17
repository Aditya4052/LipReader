# LipReader
Marathi Lip Reading Dataset (MLRD-20)
MLRD-20 is a word-level lip reading dataset in the Marathi language, created by recording videos from 38 native speakers. The dataset contains isolated word utterances, mouth-cropped videos, and associated annotations. This repository provides the annotation files, sample videos, and processing/training code for researchers and developers working on visual speech recognition in low-resource languages.

📦 Dataset Overview
Language: Marathi
Total Speakers: 38
Vocabulary Size: 20 words
Total Videos (Original): 760
With Augmentation (lighten/darken): 2,280 videos
Video Format: .mp4, 64x64 pixels, 2 seconds, 25 FPS
Augmentations: Lighten, Darken (x3 total per word)
🗂 Directory Structure
marathi-lip-reading-mlrd20/
├── annotation.csv               # CSV file with word ID and label
├── notebooks/
│   └── mlrd20_demo.ipynb        # Sample notebook for loading and using the dataset
├── scripts/
│   └── augment.py               # Code for video augmentation
├── LICENSE                      # MIT License (for code)
├── dataset_image.png            # Previw Image
├── LICENSE-CC-BY-SA-4.0         # CC BY-SA 4.0 (for dataset)
└── README.md
🧾 Annotations
All videos in the dataset are annotated in a CSV file named annotations.csv, located at the root of the dataset. Each row in the CSV corresponds to a single video clip and includes the following fields:

Column Name	Description
filename	Name of the video file (e.g., s1_w1_base.mp4)
speaker_id	Speaker identifier (e.g., s1 for Speaker 1)
word_id	Word identifier (e.g., w1, w2, ..., w20)
word_text	Marathi word spoken in the video (e.g., शिवाजी)
augmentation	Type of augmentation applied (base, lighten, or darken)
frames	Number of frames in the video (fixed at 50)
fps	Frames per second (fixed at 25.00)
duration	Duration of the video in seconds (fixed at 2.000)
Example Entries

filename,speaker_id,word_id,word_text,augmentation,frames,fps,duration
s1_w1_base.mp4,s1,w1,छत्रपती,base,50,25.00,2.000
s1_w2_base.mp4,s1,w2,शिवाजी,base,50,25.00,2.000
s1_w3_base.mp4,s1,w3,महाराज,base,50,25.00,2.000
s1_w4_base.mp4,s1,w4,हे,base,50,25.00,2.000
Each speaker (s1 to s38) recorded all 20 words (w1 to w20) in three versions:

base (original)
lighten (increased brightness)
darken (decreased brightness)
Total Entries: 2,280 rows in annotations.csv

🗣 Vocabulary (20 Words)
w1: छत्रपती       w11: महान
w2: शिवाजी        w12: राजे
w3: महाराज        w13: होते
w4: हे             w14: त्यांनी
w5: महाराष्ट्राच्या w15: रयतेचे
w6: मातीमध्ये      w16: राज्य
w7: जन्मलेले       w17: म्हणजेच
w8: एक             w18: स्वराज्य
w9: शूरवीर         w19: स्थापना
w10: आणि           w20: केले
🚀 How to Use
Download the full dataset from Kaggle.
Clone this repository:
git clone https://github.com/yourusername/marathi-lip-reading-mlrd20.git
cd marathi-lip-reading-mlrd20
Open the notebooks/mlrd20_demo.ipynb to view a working example of how to load and process videos and annotations.
👨‍💻 Authors
This dataset and repository were created by:

Muaaj Nesarikar
Aditya Patil
Vedant Desai
Sushant More
📄 License
🧠 Code is licensed under the MIT License.
📊 Dataset (videos + annotations) is licensed under CC BY-SA 4.0.
📬 Citation
To cite this dataset in your research, please use the following BibTeX (example):

@misc{mlrd2025,
  title={MLRD-20: A Marathi Lip Reading Dataset},
  author={Vedant Desai and Muaaj Nesarikar and Aditya Patil and Sushant More},
  year={2025},
  note={https://www.kaggle.com/datasets/desaivedantanil/mlrd-20}
}
🙌 Acknowledgements
Special thanks to all student volunteers who contributed recordings for this dataset.
