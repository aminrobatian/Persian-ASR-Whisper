# Whisper Model Evaluation on Persian Language  

This repository contains the results of evaluating Whisper model variations on the Persian language using the **Common Voice Corpus 19.0 - Persian** dataset. The dataset was filtered and analyzed before evaluation, and the results are presented in this repository.  

## Dataset Details  

We utilized the **train**, **dev**, and **test** partitions of the Common Voice Corpus 19.0 - Persian dataset, applying the following filter criterion:

downvotes == 0 and upvotes >= 2


### Dataset Sizes  

The dataset sizes, measured by the number of files, before and after filtering are summarized below:  

| Partition | Number of Files Before Filtering | Number of Files After Filtering |  
|-----------|-----------------------------------|----------------------------------|  
| Train     | 29,175                           | 27,869                          |  
| Dev       | 9,687                            | 8,922                           |  
| Test      | 10,404                           | 9,121                           |  

### Dataset Statistics  

Statistics regarding the lengths of audio files in each partition are as follows:  

| Partition | Min Length (s) | Max Length (s) | Average Length (s) |  
|-----------|----------------|----------------|---------------------|  
| Train     | 0.97           | 10.34          | 3.81               |  
| Dev       | 1.07           | 10.42          | 4.25               |  
| Test      | 1.40           | 10.63          | 4.90               |  

## JSON Files  

The dataset's TSV files were converted into JSON files for easier processing. The following files are included:  

- `cv-corpus-19.0-2024-09-13-fa-train.json`  
- `cv-corpus-19.0-2024-09-13-fa-dev.json`  
- `cv-corpus-19.0-2024-09-13-fa-test.json`  

These files are generated from the filtered dataset and contain metadata about the audio files.


