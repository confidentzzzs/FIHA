# FIHA: Fine-grained Hallucinations Evaluations in Large Vision Language Models

## Project Description

FIHA (Fine-grained Hallucinations Evaluations) is a framework designed to evaluate the hallucinations in Large Vision Language Models (LVLMs). The project aims to generate and evaluate question-answer pairs automatically without manual annotations, utilizing the Davidson Scene Graph (DSG) to structure the QA pairs. FIHA comprises four benchmarks derived from two datasets: MSCOCO and Foggy Cityscapes. The download linked for the 500 sample from MS COCO: https://drive.google.com/drive/folders/1dXokt_eFJeh58fZe5UoJtQ1umHSEbLGq?usp=sharing and download link for 150 sample from Foggy Cityscapes: https://drive.google.com/drive/folders/1eN2js1CIW5i9uto60D9VZiTyTroVOKN2?usp=sharing



## Benchmark usage

There are 4 benchmark which can be directly used to test the LVLMS' performance. The demo of running experiment on CHATGPT-4V can be find at demo_gpt4v.py and get the output file which includes the response from the CHATGPT-4V. 
Later you could test the score with the  

## Create your own benchmark

### Set up the environment:

The environment setup for FIHA QA generated framework relies on py-bottom-up-attention. Please follow the instructions in the environment setup repository to configure your environment in following link https://github.com/airsplay/py-bottom-up-attention.
After setup, there is two approach to genereate QA
### QA from images
1. extract the object and attribute pair through, demo can be find at feature_extraction_from_image.ipynb, then you can get a file end with .xlsx 
2. using the .xlsx to extract the relations and generated QA by QA_Generation.ipynb 
### QA from captions
1. generated the captions from the image
2. extract the entities and relations from captions
3. generated QA pairs through template
Those three steps are includes in QA_Generation.ipynb 

### Paper url
https://aclanthology.org/2025.findings-acl.622/

