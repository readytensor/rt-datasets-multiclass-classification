# Datasets for Multi-Class Classification Base category on Ready Tensor

This repo contains all files related to the datasets used in algorithm evaluation for the Multi-Class Classification - Base category.

The `datasets` folder contains the main data files and the schema files for all the benchmark datasets under Multi-Class Classification - Base category. Within each dataset folder in `datasets`:

- The `raw` folder contains the original data files from the source (see attributions below).
- `processed` folder contains the compressed, processed files. These files are used in algorithm evaluations.
  - The CSV file with suffix "\_train.csv" is used for training
  - "\_test.csv" is used for testing (without the targets)
  - "\_test_key.csv" contains the targets for the test data. This test key file is used to generate scores by comparing with predictions.
  - The JSON file with suffix "\_schema.json" is the schema file for the corresponding dataset.
  - The json file with the suffix "\_infer_req.json" contains a sample JSON object with the data to make an inference request to the /infer endpoint.
  - The CSV file with the dataset name, and no other suffix, is the full data (made of both train and test sets).
- The Jupyter notebook file within each dataset folder is used to convert the raw data file(s) in `raw` folder into the processed form in `processed` folder.
- The folder `schema_cfg` contains a csv which is needed by the schema generation script (described below) .

`schema_gen` folder contains a schema gen config file (YAML) and a python script which are used to generate the JSON schema files stored in the `processed` folder for each dataset. The generated schema file conforms to the Ready Tensor specification for this category.

---

The following is the list of datasets along with a brief description for each and its attribution:

---

## DNA Splice Junction

#### Alias (in scorecards): splice_junction

#### Domain / Industry: Molecular Biology

#### Description

The problem posed in this dataset is to recognize, given a sequence of DNA, the boundaries between exons (the parts of the DNA sequence retained after splicing) and introns (the parts of the DNA sequence that are spliced out). This problem consists of two subtasks: recognizing exon/intron boundaries (referred to as EI sites), and recognizing intron/exon boundaries (IE sites). (In the biological community, IE borders are referred to as acceptors while EI borders are referred to as donors.

#### Dataset characteristics

- Number of samples = 3,190
- Number of input features = 62
- Number of target classes = 3
- Has categorical features = Yes
- Has missing values = No

#### Attribution

Creators:
All examples taken from Genbank 64.1
Categories "ei" and "ie" include every "split-gene" for primates in Genbank 64.1
non-splice examples taken from sequences known not to include a splicing site

Donor:
G. Towell, M. Noordewier, and J. Shavlik
{towell,shavlik}@cs.wisc.edu, noordewi '@' cs.rutgers.edu}

Dataset can be found here:
http://archive.ics.uci.edu/ml/datasets/Molecular+Biology+(Splice-junction+Gene+Sequences)

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## Gesture Phase Segmentation

#### Alias (in scorecards): gesture_phase

#### Domain / Industry: Biomechanics / Biosciences

#### Description

Dataset consists of features extracted from 7 videos with people gesticulating, aiming at studying Gesture Phase Segmentation. Features define the velocity and acceleration of hands and wrists. The gestures are classified into one of 5 categories: D (rest position, from portuguese “descanso”), P (preparation), S (stroke), H (hold), R (retraction).

#### Dataset characteristics

- Number of samples = 9,900
- Number of input features = 32
- Number of target classes = 5
- Has categorical features = No
- Has missing values = No

#### Attribution

Original source of data (multiple papers):

Madeo, R. C. B. ; Lima, C. A. M. ; PERES, S. M. . Gesture Unit Segmentation using Support Vector Machines: Segmenting Gestures from Rest Positions. In: Symposium on Applied Computing (SAC), 2013, Coimbra. Proceedings of the 28th Annual
ACM Symposium on Applied Computing (SAC), 2013. p. 46-52.

Wagner, P. K. ; PERES, S. M. ; Madeo, R. C. B. ; Lima, C. A. M. ; Freitas, F. A. . Gesture Unit Segmentation Using Spatial-Temporal Information and Machine Learning. In: 27th Florida Artificial Intelligence Research Society Conference (FLAIRS), 2014, Pensacola Beach. Proceedings of the 27th Florida Artificial Intelligence Research Society Conference (FLAIRS). Palo Alto : The AAAI Press, 2014. p. 101-106.

Creators: Renata Cristina Barros Madeo (Madeo, R. C. B.) Priscilla Koch Wagner (Wagner, P. K.) Sarajane Marques Peres (Peres, S. M.) {renata.si, priscilla.wagner, sarajane} at -A Home 04-06-2020 Dr. Sarajane M. Peres

Dataset can be found here:
https://archive.ics.uci.edu/ml/datasets/gesture+phase+segmentation#

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## IPUMS Census Small

#### Alias (in scorecards): ipums_census_small

#### Domain / Industry: Demographics / Census

#### Description

The original source for this data set is the IPUMS project (RugglesSobek, 1997). The IPUMS project is a large collection of federal census data which has standardized coding schemes to make comparisons across time easy.

The dataset consists of samples of households or dwellings from the Los Angeles - Long Beach area. We use the smaller version of the dataset which contains a 1 in 1000 sample from the given area. It was formed by sampling from the larger dataset (1 in 100 samples).

The task is to predict the ‘movedin’ category, given various demographic attributes regarding households.

#### Dataset characteristics

- Number of samples = 7,485
- Number of input features = 61
- Number of target classes = 7
- Has categorical features = Yes
- Has missing values = Yes

#### Attribution

Source:

Steven Ruggles and Matthew Sobek et. al.
Integrated Public Use Microdata Series: Version 2.0
Minneapolis: Historical Census Projects,
University of Minnesota, 1997

Relevant paper:

S. Ruggles. (1995). "Sample Designs and Sampling Errors". Historical Methods. Volume 28. Number 1. Pages 40 - 46.

Dataset can be found here:
https://archive.ics.uci.edu/ml/datasets/IPUMS+Census+Database

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## Landsat Satellite

#### Alias (in scorecards): landsat_satellite

#### Domain / Industry: Space / Geospatial Technology

#### Description

The database consists of the multi-spectral values of pixels in 3x3 neighbourhoods in a satellite image, and the classification associated with the central pixel in each neighbourhood. The aim is to predict this classification, given the multi-spectral values. In the sample database, the class of a pixel is coded as a number.

#### Dataset characteristics

- Number of samples = 6,435
- Number of input features = 36
- Number of target classes = 6
- Has categorical features = No
- Has missing values = No

#### Attribution

Source:

Ashwin Srinivasan
Department of Statistics and Data Modeling
University of Strathclyde
Glasgow
Scotland
UK
ross '@' uk.ac.turing

The original Landsat data for this database was generated from data purchased from NASA by the Australian Centre for Remote Sensing, and used for research at:
The Centre for Remote Sensing
University of New South Wales
Kensington, PO Box 1
NSW 2033
Australia.

Dataset can be found here:
http://archive.ics.uci.edu/ml/datasets/Statlog+(Landsat+Satellite)

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## Page Blocks Classification

#### Alias (in scorecards): page_blocks

#### Domain / Industry: Information / Digital Media

#### Description

The problem consists in classifying all the blocks of the page layout of a document that has been detected by a segmentation process. This is an essential step in document analysis in order to separate text from graphic areas. Indeed, the five classes are: text (1), horizontal line (2), picture (3), vertical line (4) and graphic (5).

The inputs used for classification of each block include features such as block height, length, area, eccentricity, mean number of white-black transitions, etc.

#### Dataset characteristics

- Number of samples = 5,473
- Number of input features = 11
- Number of target classes = 5
- Has categorical features = No
- Has missing values = No

#### Attribution

Creator:
Donato Malerba Dipartimento di Informatica University of Bari via Orabona 4 70126 Bari - Italy phone: +39 - 80 - 5443269 fax: +39 - 80 - 5443196 malerbad@vm.csata.it

Donor:
Donato Malerba (c) Date: July 1995

Dataset can be found here:
https://www.openml.org/d/30

---

## Primary Tumor

#### Alias (in scorecards): primary_tumor

#### Domain / Industry: Healthcare

#### Description

This primary tumor domain was obtained from the University Medical Centre, Institute of Oncology, Ljubljana, Yugoslavia. Thanks go to M. Zwitter and M. Soklic for providing the data.

This is one of three domains provided by the Oncology Institute that has repeatedly appeared in the machine learning literature. (See also breast-cancer and lymphography.)

#### Dataset characteristics

- Number of samples = 339
- Number of input features = 17
- Number of target classes = 22
- Has categorical features = Yes
- Has missing values = Yes

#### Attribution

Source / Donors: Igor Kononenko, University E.Kardelj Faculty for electrical engineering Trzaska 25 61000 Ljubljana

Dataset can be found here:

https://www.openml.org/d/171

---

## Soybean Disease

#### Alias (in scorecards): soybean_disease

#### Domain / Industry: Plant Pathology

#### Description

This is the soybean disease diagnosis dataset. Samples contain 35 attributes from soybean that can be used to classify each sample into one of 19 disease types. The features are all categorical, some nominal and some ordered.

#### Dataset characteristics

- Number of samples = 683
- Number of input features = 35
- Number of target classes = 19
- Has categorical features = Yes
- Has missing values = Yes

#### Attribution

Dataset from this study:

R.S. Michalski and R.L. Chilausky "Learning by Being Told and Learning from Examples: An Experimental Comparison of the Two Methods of Knowledge Acquisition in the Context of Developing an Expert System for Soybean Disease Diagnosis", International Journal of Policy Analysis and Information Systems, Vol. 4, No. 2, 1980.

Donor:
Ming Tan & Jeff Schlimmer (Jeff.Schlimmer%cs.cmu.edu)

Dataset can be found here:
https://archive.ics.uci.edu/ml/datasets/Soybean+(Large)

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## Spotify Song Genre

#### Alias (in scorecards): spotify_genre

#### Domain / Industry: Music / Audio Streaming

#### Description

This dataset consists of features of songs from various genres such as Trap, Techno, Techhouse, HipHop, Rap, Pop, Emo, etc. In this task, we use the song features such as danceability, energy, key, loudness, speechiness, tempo etc. to identify the song genre.

The original dataset contained 42,305 songs from 15 genres. We filtered the dataset to contain songs from 7 genres, namely, Hiphop, Trap, Techno, RnB, Rap, Pop and Emo.

Some songs were marked under multiple genres. In such cases, we retained only the first observed sample of the song to keep the problem under the multi-class classification category. So each song has a single genre in the final processed dataset.

#### Dataset characteristics

- Number of samples = 13,566
- Number of input features = 13
- Number of target classes = 7
- Has categorical features = Yes
- Has missing values = No

#### Attribution

Dataset can be found here:
https://www.kaggle.com/datasets/mrmorj/dataset-of-songs-in-spotify

---

## Steel Plate Fault

#### Alias (in scorecards): steel_plate_fault

#### Domain / Industry: Steelmaking / Steel

#### Description

A dataset of steel plates faults, classified into 7 different types. The goal is to train machine learning for automatic pattern recognition.

#### Dataset characteristics

- Number of samples = 1,941
- Number of input features = 27
- Number of target classes = 7
- Has categorical features = No
- Has missing values = No

#### Attribution

Source:

Semeion, Research Center of Sciences of Communication, Via Sersale 117, 00128, Rome, Italy.
www.semeion.it

Dataset can be found here:
http://archive.ics.uci.edu/ml/datasets/steel+plates+faults

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---

## Vehicle Silhouettes

#### Alias (in scorecards): vehicle_silhouettes

#### Domain / Industry: Automotive

#### Description

The purpose is to classify a given silhouette as one of four types of vehicle, using a set of features extracted from the silhouette. The vehicle may be viewed from one of many different angles.

Four "Corgie" model vehicles were used for the experiment: a double decker bus, Cheverolet van, Saab 9000 and an Opel Manta 400. This particular combination of vehicles was chosen with the expectation that the bus, van and either one of the cars would be readily distinguishable, but it would be more difficult to distinguish between the cars.

The features were extracted from the silhouettes by the HIPS (Hierarchical Image Processing System) extension BINATTS, which extracts a combination of scale independent features utilising both classical moments based measures such as scaled variance, skewness and kurtosis about the major/minor axes and heuristic measures such as hollows, circularity, rectangularity and compactness.

The original purpose of the study was to find a method of distinguishing 3D objects within a 2D image by application of an ensemble of shape feature extractors to the 2D silhouettes of the objects. Measures of shape features extracted from example silhouettes of objects to be discriminated were used to generate a classification rule tree by means of computer induction.

#### Dataset characteristics

- Number of samples = 1,846
- Number of input features = 18
- Number of target classes = 4
- Has categorical features = No
- Has missing values = No

#### Attribution

Data comes from this study:
Siebert,JP. Turing Institute Research Memorandum TIRM-87-018 "Vehicle Recognition Using Rule Based Methods" (March 1987).

Source:

Drs.Pete Mowforth and Barry Shepherd
Turing Institute
George House
36 North Hanover St.
Glasgow
G1 2AD

Dataset can be found here:
https://archive.ics.uci.edu/ml/datasets/Statlog+(Vehicle+Silhouettes)

UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

---
