## `Title：MVAE-DFDPNnet:Drug-Protein Interaction Prediction via Multi-View Variational Autoencoder and Cascade Deep Forests`
In this study, a novel deep learning framework called Multi-view Variational Auto-Encoder embedded Deep Forest (MVAE-DFDPnet) is proposed for the accurate prediction of Drug-Protein Interactions (DPIs). DPI prediction is critical for drug discovery and precision medicine, and this framework aims to address the challenges posed by the high-dimensionality representation of drug and protein characteristics and their interactions.
file:///C:/Users/feng/Desktop/%E6%8D%95%E8%8E%B7.PNG
MVAE-DFDPnet is developed and maintained by Luo lab at `Shanghai Jiao Tong University`. Please direct your questions regarding MVAE-DFDPnet to Jie Luo: jieluo@sjtu.edu.cn.

### MVAE-DFDPnet is written in Python 3.9, with the following dependencies:
   *   tensorflow    2.2.0
   *   numpy         1.19.2
   *   pandas       1.1.3
   *   xgboost       1.3.3
   *   scikit-learn    0.23.2
   *   Keras         2.4.3
   *   scipy         1.5.2
   *   joblib         0.17.0
      


###  `Code and data`
####  Data preprocessing (similar work with https://github.com/luoyunan/DTINet)
    
* `main.m`:implement data preprocessing 
* `ScaleSimMat.m`:Scale Similar Matrix by Row 
* `RandSurf.m`:network diffusion algorithm (random walk with restart)
* `GetPPMIMatrix.m`:get PPMI matrix
* `compute_similarity.m`:compute Jaccard similarity based on interaction/association network

####   Data preprocessing/data
* drugsim1network.txt: Drug chemical similarity matrix
* drugsim2network.txt: Drug therapeutic similarity matrix
* drugsim3network.txt: Drug sequence similarity matrix
* drugsim4network.txt: Drug biological processes similarity matrix
* drugsim5network.txt: Drug cellular component similarity matrix
* drugsim6network.txt: Drug molecular function similarity matri
* proteinprotein.txt: Protein-Protein interaction matrix
* proteinDisease.txt: Protein-Disease association matrix
* proteinsim1network.txt: Protein sequence similarity matrix
* proteinsim2network.txt: Protein biological processes similarity matrix
* proteinsim3network.txt: Protein cellular component similarity matrix
* proteinsim4network.txt: Protein molecular function similarity matrix
* Sim_drugDisease: Drug-Disease Jaccard similarity matrix
* Sim_proteinDisease.txt: Protein-Disease Jaccard similarity matrix

#### Embedding
* `Demo.py`:compact feature learning by integrating heterogeneous network
* `MVAE`:construct deep network for Multi-View Variational Autoencoder (epoch = 500,batchsize =100)

We provided the pre-trained vector representations for drugs and proteins, which were used to produce the results in our paper.
* drugFeature.txt
* proteinFeature.txt

<p class="red-text">Basic Usage：</p>
```$ python  demo.py```

#### Prediction/Deepforest/
* `deepforest.py`: predict drug-protein interactions (DPIs)
    Basic Usage
     $ python  deepforest.py
