# `Title：MVAE-DFDPNnet:Drug-Protein Interaction Prediction via Multi-View Variational Autoencoder and Cascade Deep Forests`

In this study, a novel deep learning framework called Multi-view Variational Auto-Encoder embedded Deep Forest (MVAE-DFDPnet) is proposed for the accurate prediction of Drug-Protein Interactions (DPIs). DPI prediction is critical for drug discovery and precision medicine, and this framework aims to address the challenges posed by the high-dimensionality representation of drug and protein characteristics and their interactions.
file:///C:/Users/feng/Desktop/%E6%8D%95%E8%8E%B7.PNG
MVAE-DFDPnet is developed and maintained by Luo lab at `Shanghai Jiao Tong University`. Please direct your questions regarding MVAE-DFDPnet to Jie Luo: jieluo@sjtu.edu.cn.

## MVAE-DFDPnet is written in Python 3.9, with the following dependencies:
   *   tensorflow    2.2.0
   *   numpy         1.19.2
   *   pandas       1.1.3
   *   xgboost       1.3.3
   *   scikit-learn    0.23.2
   *   Keras         2.4.3
   *   scipy         1.5.2
   *   joblib         0.17.0
      


## `Code and data`
### *  Data preprocessing (similar work with https://github.com/luoyunan/DTINet)
    
    *  main.m:implement data preprocessing 
    *  ScaleSimMat.m:Scale Similar Matrix by Row 
    *  RandSurf.m:network diffusion algorithm (random walk with restart)
    *  GetPPMIMatrix.m:get PPMI matrix
    *  compute_similarity.m:compute Jaccard similarity based on interaction/association network

### *  Data preprocessing/data
    - drugsim1network.txt: Drug chemical similarity matrix
    - drugsim2network.txt: Drug therapeutic similarity matrix
    - drugsim3network.txt: Drug sequence similarity matrix
    - drugsim4network.txt: Drug biological processes similarity matrix
    - drugsim5network.txt: Drug cellular component similarity matrix
    - drugsim6network.txt: Drug molecular function similarity matri
    - proteinprotein.txt: Protein-Protein interaction matrix
    - proteinDisease.txt: Protein-Disease association matrix
    - proteinsim1network.txt: Protein sequence similarity matrix
    - proteinsim2network.txt: Protein biological processes similarity matrix
    - proteinsim3network.txt: Protein cellular component similarity matrix
    - proteinsim4network.txt: Protein molecular function similarity matrix
    - Sim_drugDisease: Drug-Disease Jaccard similarity matrix
    - Sim_proteinDisease.txt: Protein-Disease Jaccard similarity matrix

### *  Embedding
    - Demo.py:compact feature learning by integrating heterogeneous network
    - MVAE:construct deep network for Multi-View Variational Autoencoder (epoch = 500,batchsize =100)

    Basic Usage

    `$ python  demo.py'

### *  Prediction/Deepforest/
   -  deepforest.py: predict drug-protein interactions (DPIs)
    Basic Usage
     $ python  deepforest.py











![mahua](mahua-logo.jpg)
##MaHua是什么?
一个在线编辑markdown文档的编辑器

##MaHua有哪些功能？

* 方便的`导入导出`功能
    *  直接把一个markdown的文本文件拖放到当前这个页面就可以了
    *  导出为一个html格式的文件，样式一点也不会丢失
* 编辑和预览`同步滚动`，所见即所得（右上角设置）
* `VIM快捷键`支持，方便vim党们快速的操作 （右上角设置）
* 强大的`自定义CSS`功能，方便定制自己的展示
* 有数量也有质量的`主题`,编辑器和预览区域
* 完美兼容`Github`的markdown语法
* 预览区域`代码高亮`
* 所有选项自动记忆

##有问题反馈
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流

* 邮件(dev.hubo#gmail.com, 把#换成@)
* 微信:jserme
* weibo: [@草依山](http://weibo.com/ihubo)
* twitter: [@ihubo](http://twitter.com/ihubo)

##捐助开发者
在兴趣的驱动下,写一个`免费`的东西，有欣喜，也还有汗水，希望你喜欢我的作品，同时也能支持一下。
##感激
感谢以下的项目,排名不分先后

* [ace](http://ace.ajax.org/)
* [jquery](http://jquery.com)

##关于作者

```javascript
var ihubo = {
  nickName  : "草依山",
  site : "http://jser.me"
}
```
