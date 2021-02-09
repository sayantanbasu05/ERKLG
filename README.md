# ERLKG

This is the repository for the paper

>[ERLKG: Entity Representation Learning and Knowledge Graph based association analysis of COVID-19 through mining of unstructured biomedical corpora *Sayantan Basu\*, Sinchani Chakraborty*, Atif Hassan*, Sana Siddique*,Ashish Anand*](https://www.aclweb.org/anthology/2020.sdp-1.15/)

accepted at [Scholarly Document Processing, EMNLP 2020](https://ornlcda.github.io/SDProc/index.html).


We introduce a generic, human-out-of-the loop pipeline, ERLKG, to perform rapid association analysis of any biomedical entity with other existing entities from a corpora of the same domain. Our pipeline consists of a Knowledge Graph (KG) created from the Open Source CORD-19 dataset by fully automating the procedure of information extraction using **SciBERT**. The best latent entity representations are then found by benchnmarking different KG embedding techniques on the task of link prediction using a **Graph Convolution Network Auto Encoder (GCN-AE)**. We demonstrate the utility of ERLKG with respect to COVID-19 through multiple qualitative evaluations. Due to the lack of a gold standard, we propose a relatively large intrinsic evaluation dataset for **COVID-19** and use it for validating the top two performing KG embedding techniques. We find TransD to be the best performing KG embedding technique with Pearson and Spearman correlation scores of 0.4348 and 0.4570 respectively. We demonstrate that a considerable number of ERLKG’s top protein, chemical and disease predictions are currently in consideration for COVID-19 related research.


## Pipeline Architecture
<p align="center">
  <img width="700" alt="mono_ar" src="https://github.com/sayantanbasu05/ERKLG/blob/master/Images/ERLKG_illustration.jpg">
</p>

Illustrator: [Sanket Wakade](https://www.linkedin.com/in/sanket-wakade/)

## Link Prediction

Method | ROC | AP| 
--- | --- | ---
RotatE (Sun et al., 2019) | 0.858 | **0.887**
TransD (Ji et al., 2015) | **0.860** | 0.883
TransE (Bordes et al., 2013) | 0.853 | 0.877
DistMult (Yang et al., 2015) | 0.855 | 0.883
ComplEx (Trouillon et al., 2016) | 0.852 | 0.881
Node2Vec (Grover and Leskovec, 2016)	 | 0.821 | 0.849
Table 1: Link Prediction performance of different KG embedding techniques on the test set using the GCN-AE model


## Proposed Intrinsic Evaluation Datasets
We have released two datasets for intrinsic evaluation, namely, COV19_729 and COV19_25. The datasets are present in [dataset for intrinsic evaluation](https://github.com/sayantanbasu05/ERKLG/tree/master/Dataset%20for%20Intrinsic%20Evaluation) folder that contain 729 and 25 entities along with their types (chemicals, proteins or diseases). Each entity has a corresponding physician rating (on a scale of 1 to 5) which measures its association with COVID-19.

## Result

<p align="center">
  <img width="800" alt="mono_ar" src="https://github.com/sayantanbasu05/ERKLG/blob/master/Images/COV19_25%20Dataset%20Construction.png">
</p>


## 



### For a more detailed explanation of the project, please visit this [blog post](https://www.deepwizai.com/erlkg)


Author Details: [Sayantan Basu](https://www.linkedin.com/in/sayantan-basu-a29861a1/), [Sinchani Chakraborty](https://www.linkedin.com/in/sinchani-chakraborty-087321ab/), [Atif Hassan](https://www.linkedin.com/in/atif-hassan-1a8a45127/), Sana Siddique and [Ashish Anand](https://www.linkedin.com/in/anandashish/)

## Cite
If your work is inspired by our research and/or you use our provided datasets then please cite this paper.
```
@inproceedings{Basu2020ERLKGER,
  title={ERLKG: Entity Representation Learning and Knowledge Graph based association analysis of COVID-19 through mining of unstructured biomedical corpora},
  author={Sayantan Basu and Sinchani Chakraborty and Atif Hassan and Sana Siddique and A. Anand},
  booktitle={SDP@EMNLP},
  year={2020}
}
```
