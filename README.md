# Extracting-Linguistic-Information-from-LLMs

## Introduction
This repository contains datasets designed for studying 
linguistic knowledge and generalization capabilities of Large Language Models (LLMs), focusing on their morphosyntactic competence. 
We design three diagnostic tasks that are discussed as follows.


## Tasks Overview

**Syntax (Task 1)**  
Syntax (referred to as Task 1 in the paper): Involves labeling syntactic information at the sentence level, specifically identifying subjects, objects, and indirect objects.

**Derivation**  
Derivation – Focuses on the morphological decomposition of derivational words, with two task variants:

- **Task 2**: Conducted across five languages, involving the identification of morpheme boundaries and the labeling of each morpheme.  
- **Task 3**: An in-depth study of morphological decomposition, focusing specifically on German and Amharic.

---

## Dataset Details

### Task 1
The data is sourced from [Universal Dependencies (UD)](https://universaldependencies.org/) treebanks for **10 diverse languages**:  
Amharic (amh), English (eng), French (fra), German (deu), Italian (ita), Latvian (lav), Lithuanian (lit), Maltese (mlt), Polish (pol), and Upper Sorbian (hsb).  

Amharic follows a root-and-pattern morphology where subject, object, and indirect object markers appear as bound morphemes, typically attached to verbs and encoding multiple syntactic functions. In the UD dataset, these morphemes are often segmented as separate words, though they are not independent lexical items and usually co-occur with an overt subject.

To reflect this, we provide two dataset versions: Amharic, which labels whole words with syntactic roles, and Amharic-morph, which segments words and labels the morphemes indicating subject and indirect object.

After preprocessing, the dataset is split into **train**, **dev**, and **test** sets:  
- **Folder**: `syntax/task-1`  
- **Dev/Test Data**: Located in the `0_shot_examples/LANGUAGE_NAME` folder  
- **Training Data**: Located in the corresponding `n_shot_examples/LANGUAGE_NAME` folders, where `n = {0, 1, 3, 5}`  

---

### Task 2
This dataset covers **five languages** sourced from [UniMorph](https://unimorph.github.io/), including only **derivational words**. After preprocessing, the datasets are categorized based on their part of speech: nouns(N), verbs(V), and adjectives(ADJ). The train/test/dev split are provided in their respective folders.
- **Folder**: `derivation/task-2`  
- **Dev/Test Data**: Located in the `0_shot_examples/LANGUAGE_CODE` folder  
- **Training Data**: Located in the corresponding `n_shot_examples/LANGUAGE_CODE` folders, where `n = {0, 1, 3, 5, 10}` 

---

### Task 3
For this task, we provide a **newly curated dataset** for **Amharic** and **German**:  
- **Amharic**: Data sourced from WMT and processed using [HornMorpho](https://github.com/hltdi/HornMorpho/tree/master) (morphological analyzer and generator). Includes Nouns and Verbs. 
- **German**: Data sourced from Wikipedia and processed using the [SMOR tool](https://aclanthology.org/L04-1007.pdf). Inlcudes Nouns and Adjectives.


The dataset is organized as follows:  
- **Folder**: `derivation/task-3`  
- **Dev/Test Data**: Located in the `0_shot_examples/LANGUAGE_CODE` folder  
- **Training Data**: Located in the corresponding `n_shot_examples/LANGUAGE_CODE` folders, where `n = {0, 1, 3, 5, 10}` 

---

## Languages Covered
The following table lists the languages included in the datasets along with their ISO 639-3 codes:

| Language       | ISO3 Code |
|----------------|-----------|
| Amharic        | amh       |
| English        | eng       |
| French         | fra       |
| German         | deu       |
| Italian        | ita       |
| Latvian        | lav       |
| Lithuanian     | lit       |
| Maltese        | mlt       |
| Polish         | pol       |
| Upper Sorbian  | dsb       |


---

## Citation
If you use this dataset in your research, please cite the following paper:
