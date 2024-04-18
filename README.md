# Projecticum Data Science HU Spring 2024

This is the GitHub repository for the project from the Data Science Innovative Testing in Life Sciences and Chemistry group assignment.

## Basic information
The goal of the project is to develop a small NER model to identify concepts from Materials and Methods in scientific literature mentioning parameters for PBPK models.

The model will be developed in Python using the [spaCy](https://spacy.io/) library, with a [scispaCy](https://allenai.github.io/scispacy/) model as a base.

## Training data
- A training database will be developed using articles identified in [Towards harmonization of test methods for in vitro hepatic clearance studies](https://ars.els-cdn.com/content/image/1-s2.0-S0887233319305909-mmc1.xlsx). PDFs for these articles can be found in the data directory. Partial extraction of text as been performed already, but students can contribute [here](https://aryastark.ontoxnams-hu.src.surf-hosted.nl/) (Note: Add "?session=yourfirstname" at the end of the url. Username and password are your first name). The full text database will be uploaded in the data directory as well. Note that more articles can be collected, depending on progress.
- The type of entities to be collected needs to be listed and defined.
- [Prodigy](https://prodi.gy/) will then be used to collect NER annotations - license number is available upon request but shoould **not** be made visible in any public location. 
- From these annotations, an NER model can then be [trained](https://spacy.io/usage/training).

We recommend iterations of annotation/training to see how data collection improves performance.

Deliverables:
-	Trained NER model + training database 
-	List and definition of entities recognized by the model (in directory reporting)
-	F1 score (cross validation) per entity (in directory reporting)
-	All code and materials generated backed up in this repo (in directory code) + short summary of hurdles encountered (in directory reporting)

