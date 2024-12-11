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

# Whisper Models Performance on Persian Common Voice Corpus

This section presents the evaluation of Whisper models on the Persian Common Voice Corpus 19.0, using Word Error Rate (WER) as the metric across the train, dev, and test sets. The models vary in size, from the "tiny" model to the "large-v3," with results showing the trade-offs between model size, VRAM usage, and WER.

### Model Performance Summary

| Model       | Parameters | Required VRAM | WER % (Train) | WER % (Dev) | WER % (Test) |
|-------------|------------|---------------|---------------|-------------|--------------|
| **tiny**    | 39 M       | ~1 GB         | 245.47        | 159.26      | 301.95       |
| **base**    | 74 M       | ~1 GB         | 133.43        | 114.87      | 160.40       |
| **small**   | 244 M      | ~2 GB         | 78.01         | 93.66       | 87.08        |
| **medium**  | 769 M      | ~5 GB         | 54.86         | 87.52       | 70.35        |
| **turbo**   | 809 M      | ~6 GB         | 38.50         | 80.41       | 48.76        |
| **large-v3**| 1550 M     | ~10 GB        | 32.91         | 77.27       | 35.83        |

*Table 1: WER performance of Whisper models on the Persian Common Voice Corpus.*



