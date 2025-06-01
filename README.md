# A Contrastive Learning Approach to Bug Severity Classification with Large Language Model Embeddings

Bug severity classification is critical for prioritizing software issues effectively. This project leverages Large Language Models (LLMs), specifically CodeBERT, to classify bug reports based on severity levels by generating contextual embeddings of bug descriptions. A contrastive learning strategy is applied to enhance the embedding space, improving separation between bug report classes and leading to better classification accuracy.

Our approach was evaluated on the NASA PITS and Mozilla bug datasets and compared with traditional embedding-based models like Doc2Vec. Results show that fine-tuning LLMs with contrastive learning improves performance, especially in diverse and imbalanced datasets.

## Core Features

- Contrastive learning using NT-Xent loss to structure the embedding space  
- Embedding generation using CodeBERT (RoBERTa-based LLM)  
- Fully connected classification head trained on bug report embeddings  
- Evaluation across intra- and cross-project datasets  
- Comparison with non-contrastive LLM and traditional Doc2Vec models  
- t-SNE visualization for understanding embedding separability  


## Datasets Used

- **NASA PITS Dataset** (5 projects, 3,282 combined bug reports)  
- **Mozilla Bug Reports** (9,998 bug reports across multiple severity levels)

Only the bug descriptions and severity levels are used for training. The models are tested in both same-project and cross-project settings.

## Experimental Settings

We evaluate the following:

- LLM + Contrastive Learning (ours)  
- LLM without Contrastive Learning  
- Doc2Vec + MLP (baseline from prior work)

Key metrics include **Accuracy** and **F1-score**, especially relevant for imbalanced datasets.

## Background

This work originated as a course project in the graduate course *Applications of LLMs to Software Engineering* at Ontario Tech University. The project was developed by Mosarrat Rumman, Emon Roy, and Anushka Zaman under the supervision of Professor Jeremy Bradbury. It was later extended into a research paper submitted to the COMPSAC 2025 SETA track.

Initial implementation by [Mosarrat Rumman](https://github.com/mosarrat28).  
Currently owned and maintained under the Software Engineering & Education Research Lab ([SEER Lab](https://github.com/seer-lab)) and the [Software Quality Research Lab (SQRL)](https://www.sqrlab.ca/).

## Paper Link

*A Contrastive Learning Approach to Bug Severity Classification with Large Language Model Embeddings*  
Accepted to **COMPSAC 2025, SETA Track**  
📄 **Link to the paper will be announced soon.**

## Citation

Citation details will be added upon publication.

## Contact

For questions, feedback, or collaboration inquiries, please contact:

- **Mosarrat Rumman** – [GitHub Profile](https://github.com/mosarrat28), [mosarrat.rumman@ontariotechu.net](mailto:mosarrat.rumman@ontariotechu.net)  
- **Software Quality Research Lab (SQRL)** – [www.sqrlab.ca](https://www.sqrlab.ca/)  
- **Professor Jeremy Bradbury** – [jeremy.bradbury@ontariotechu.ca](mailto:jeremy.bradbury@ontariotechu.ca)  
