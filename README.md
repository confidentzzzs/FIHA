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

### Citation 
@inproceedings{yan-etal-2025-fiha,
    title = "{FIHA}: Automated Fine-grained Hallucinations Evaluations in Large Vision Language Models with {D}avidson Scene Graphs",
    author = "Yan, Bowen  and
      Zhang, Zhengsong  and
      Jing, Liqiang  and
      Hossain, Eftekhar  and
      Du, Xinya",
    editor = "Che, Wanxiang  and
      Nabende, Joyce  and
      Shutova, Ekaterina  and
      Pilehvar, Mohammad Taher",
    booktitle = "Findings of the Association for Computational Linguistics: ACL 2025",
    month = jul,
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.findings-acl.622/",
    doi = "10.18653/v1/2025.findings-acl.622",
    pages = "12014--12026",
    ISBN = "979-8-89176-256-5",
    abstract = "The rapid development of Large Vision-Language Models (LVLMs) often comes with widespread hallucination issues, making cost-effective and comprehensive assessments increasingly vital. Current approaches mainly rely on costly annotations and are not comprehensive {--} in terms of evaluating all aspects, such as relations, attributes, and dependencies between aspects. Therefore, we introduce the FIHA (automated Fine-graIned Hallucination evAluation in LVLMs), which could access LVLMs hallucination in an LLM-free and annotation-free way and model the dependency between different types of hallucinations. FIHA can generate Q{\&}A pairs on any image dataset at minimal cost, enabling hallucination assessment from both image and caption. Based on this approach, we introduce a benchmark called FIHA-v1, which consists of diverse questions on various images from three datasets. Furthermore, we use the Davidson Scene Graph (DSG) to organize the structure among Q{\&}A pairs, in which we can increase the reliability of the evaluation. We evaluate representative models using FIHA-v1, highlighting their limitations and challenges. We released our code and data at https://github.com/confidentzzzs/FIHA."
}
