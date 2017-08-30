# README #

### What is this repository for? ###

* Code suplementing FEDCSIS MIDI 2017 paper ["What Looks Good with my Sofa: Multimodal Search Engine for Interior Design"](https://arxiv.org/abs/1707.06907) by Ivona Tautkute, Aleksandra Możejko, Wojciech Stokowiec, Tomasz Trzciński, Łukasz Brocki and Krzysztof Marasek
* Visual/textual search blend demo version

### Dependencies ###

* Installation of Open CV 2
* Python 3

### Installation ###

## Docker

* Build docker container `docker build -t container-name .`
* Run on port 3000 `docker run -p 3000:3000 -it container-name`

## Locally

* Download YOLO weights (https://drive.google.com/open?id=0BywyiovWX-UkeGNxdkxKdDMtdDg)
* Install Open CV and requirements from `requirements.txt`
* Run the app `python3 run.py`

### Web app ###
* Start on localhost by running run.py

* Configuration of Flask app interface: app/web_interface.py


### Notebooks ###

* Results for IKEA Dataset - contains accuracy calculations for visual search, recall curve on IKEA dataset
* Interior style dataset benchmark - contains accuracy calculations for visual and textual search on Style dataset
* Results for calculating similarity - contains similarity metric calculations for different text queries and objects in IKEA dataset

### Visual Search ###

* Visual search functions: finder.py
* Visual feature extraction: cnn_feature_extraction.py
* Functions for YOLO object detection: detect_objects.py
* Model parameters: parameters.py

### Textual Search ###
* Query transformation using SVD and finding n-nearest neigbhours: search_engine.py
* Word2vec and Countvect "training": training.py
* tSNE visualization: embedding.py
* blender.py - leftover
* Query transformation using LSTM is in the jupyter notebook sent on style-search channel on slack
