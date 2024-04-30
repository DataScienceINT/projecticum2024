# Projecticum Data Science HU Spring 2024

This is the GitHub repository for the project from the Data Science Innovative Testing in Life Sciences and Chemistry group assignment.

## Basic information
The goal of the project is to develop a small NER model to identify concepts from Materials and Methods in scientific literature mentioning parameters for PBPK models.

Some extra information about PBPK models, their aim and their development is available in the background directory.

## Tools
The model will be developed in Python using the [spaCy](https://spacy.io/) library, with a [scispaCy](https://allenai.github.io/scispacy/) model as a base. A [Prodigy](https://prodi.gy/) license key was given to the students for NER annotation and should **not** be made visible in any public location. We recommend to use Prodigy in a [conda](https://docs.anaconda.com/free/miniconda/) environment (with a recent Python version, e.g. 3.10), and to add "?session=yourfirstname" at the end of the localhost url to keep track of who annotated in case datasets need to be merged.

## Training data
- A training database was be developed using articles identified in [Towards harmonization of test methods for in vitro hepatic clearance studies](https://ars.els-cdn.com/content/image/1-s2.0-S0887233319305909-mmc1.xlsx). PDFs for these articles can be found in the data directory. Extraction of text as been performed already and stored in the file data/projecticum_dataset.jsonl.  The full text database will be uploaded in the data directory as well. Note that more articles can be collected, depending on progress.
- The type of entities to be collected needs to be listed and defined.
- Prodigy will then be used to collect NER annotations.
- From these annotations, an NER model can then be [trained](https://spacy.io/usage/training).

We recommend iterations of annotation/training to see how data collection improves performance. Intermediate models can be trained using [Prodigy](https://prodi.gy/features/training) directly.

## Deliverables
-	Trained NER model + training database 
-	List and definition of entities recognized by the model (in directory reporting)
-	F1 score (cross validation) per entity (in directory reporting)
-	All code and materials generated backed up in this repo (in directory code) + short summary of hurdles encountered (in directory reporting)

