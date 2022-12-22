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

---

##

#### Alias (in scorecards):

#### Domain / Industry:

#### Description

#### Dataset characteristics

- Number of samples =
- Number of input features =
- Number of target classes =
- Has categorical features =
- Has missing values =

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

##

#### Alias (in scorecards):

#### Domain / Industry:

#### Description

#### Dataset characteristics

- Number of samples =
- Number of input features =
- Number of target classes =
- Has categorical features =
- Has missing values =

#### Attribution

---

##

#### Alias (in scorecards):

#### Domain / Industry:

#### Description

#### Dataset characteristics

- Number of samples =
- Number of input features =
- Number of target classes =
- Has categorical features =
- Has missing values =

#### Attribution

---

##

#### Alias (in scorecards):

#### Domain / Industry:

#### Description

#### Dataset characteristics

- Number of samples =
- Number of input features =
- Number of target classes =
- Has categorical features =
- Has missing values =

#### Attribution

---

##

#### Alias (in scorecards):

#### Domain / Industry:

#### Description

#### Dataset characteristics

- Number of samples =
- Number of input features =
- Number of target classes =
- Has categorical features =
- Has missing values =

#### Attribution

---
