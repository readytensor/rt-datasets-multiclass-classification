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
