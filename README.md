# Awesome-Dataset-Distillation

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
<img src="https://img.shields.io/badge/Contributions-Welcome-278ea5" alt="Contrib"/> <img src="https://img.shields.io/badge/Number%20of%20Papers-36-FF6F00" alt="PaperNum"/> ![Stars](https://img.shields.io/github/stars/Guang000/Awesome-Dataset-Distillation?color=yellow&label=Stars) ![Forks](https://img.shields.io/github/forks/Guang000/Awesome-Dataset-Distillation?color=green&label=Forks) ![Visitors](https://visitor-badge.glitch.me/badge?page_id=Guang000/Awesome-Dataset-Distillation)


A curated list of awesome papers on dataset distillation and related applications, inspired by [awesome-computer-vision](https://github.com/jbhuang0604/awesome-computer-vision).


**Dataset distillation** is the task of synethesizing a small dataset such that models trained on it achieve high performance on the original large dataset. A dataset distillation algorithm takes as **input** a large real dataset to be distilled (training set), and **outputs** a small synthetic distilled dataset, which is evaluated via testing models trained on this distilled dataset on a separate real dataset (validation/test set). A good small distilled dataset is not only useful in dataset understanding, but has various applications (e.g., continual learning, privacy, neural architecture search, etc.). This task was first introduced in the 2018 paper [*Dataset Distillation* [Tongzhou Wang et al., '18]](https://www.tongzhouwang.info/dataset_distillation/), along with a proposed algorithm using backpropagation through optimization steps.

In recent years (2020-now), dataset distillation has gained increasing attention in the research community, across many institutes and labs. More papers are now being published each year. These wonderful researches have been constantly improving dataset distillation and exploring its various variants and applications.

**This project is curated and maintained by [Guang Li](https://www-lmd.ist.hokudai.ac.jp/member/guang-li/), [Bo Zhao](https://bozhaonanjing.wixsite.com/mysite), and [Tongzhou Wang](https://www.tongzhouwang.info/).**

#### [How to submit a pull request?](./CONTRIBUTING.md)

+ :globe_with_meridians: Project Page
+ :octocat: Code
+ :book: `bibtex`

## Contents
- [Main](#main)
  - [Early Work](#early-work)
  - [Gradient/Trajectory Matching Surrogate Objective](#gradient-objective)
  - [Distribution/Feature Matching Surrogate Objective](#feature-objective)
  - [Optimization](#optimization)
  - [Distilled Dataset Parametrization](#parametrization)
  - [Label Distillation](#label)
  - [Benchmark](#benchmark)
- [Applications](#applications)
	- [Privacy](#privacy)
	- [Federated Learning](#fed)
	- [Continual Learning](#continual)
	- [Model Compression](#model)
	- [Graph Neural Network](#gnn)
	- [Neural Architecture Search](#nas)
	- [Knowledge Distillation](#kd)
	- [Medical](#medical)
	- [Fashion, Art, and Design](#fashion)

<a name="main" />

## Main
+ [Dataset Distillation](https://arxiv.org/abs/1811.10959) (Tongzhou Wang et al., 2018) [:globe_with_meridians:](https://ssnl.github.io/dataset_distillation/) [:octocat:](https://github.com/SsnL/dataset-distillation) [:book:](./citations/wang2018datasetdistillation.txt)


<a name="early-work" />

### Early Work
+ [Gradient-Based Hyperparameter Optimization Through Reversible Learning](https://arxiv.org/abs/1502.03492) (Dougal Maclaurin et al., ICML 2015) [:octocat:](https://github.com/HIPS/hypergrad) [:book:](./citations/maclaurin2015gradient.txt)

<a name="gradient-objective" />

### Gradient/Trajectory Matching Surrogate Objective
+ [Dataset Condensation with Gradient Matching](https://arxiv.org/abs/2006.05929) (Bo Zhao et al., ICLR 2021) [:octocat:](https://github.com/VICO-UoE/DatasetCondensation) [:book:](./citations/zhao2021datasetcondensation.txt)
+ [Dataset Condensation with Differentiable Siamese Augmentation](https://arxiv.org/abs/2102.08259) (Bo Zhao et al., ICML 2021)  [:octocat:](https://github.com/VICO-UoE/DatasetCondensation) [:book:](./citations/zhao2021differentiatble.txt)
+ [Dataset Distillation by Matching Training Trajectories](https://arxiv.org/abs/2203.11932) (George Cazenavette et al., CVPR 2022) [:globe_with_meridians:](https://georgecazenavette.github.io/mtt-distillation/) [:octocat:](https://github.com/georgecazenavette/mtt-distillation) [:book:](./citations/cazenavette2022dataset.txt)
+ [Dataset Condensation with Contrastive Signals](https://arxiv.org/abs/2202.02916) (Saehyung Lee et al., ICML 2022) [:octocat:](https://github.com/saehyung-lee/dcc) [:book:](./citations/lee2022dataset.txt)
+ [Delving into Effective Gradient Matching for Dataset Condensation](https://arxiv.org/abs/2208.00311) (Zixuan Jiang et al., 2022) [:book:](./citations/jiang2022delving.txt)


<a name="feature-objective" />

### Distribution/Feature Matching Surrogate Objective
+ [Dataset Condensation with Distribution Matching](https://arxiv.org/abs/2110.04181) (Bo Zhao et al., 2021) [:octocat:](https://github.com/VICO-UoE/DatasetCondensation) [:book:](./citations/zhao2021distribution.txt)
+ [CAFE: Learning to Condense Dataset by Aligning Features](https://arxiv.org/abs/2203.01531) (Kai Wang et al., CVPR 2022)  [:octocat:](https://github.com/kaiwang960112/cafe) [:book:](./citations/wang2022cafe.txt)


<a name="optimization" />

### Better Optimization
+ [Dataset Meta-Learning from Kernel Ridge-Regression](https://arxiv.org/abs/2011.00050) (Timothy Nguyen et al., ICLR 2021) [:octocat:](https://github.com/google/neural-tangents) [:book:](./citations/nguyen2021kip.txt)
+ [Dataset Distillation with Infinitely Wide Convolutional Networks](https://arxiv.org/abs/2107.13034) (Timothy Nguyen et al., NeurIPS 2021) [:octocat:](https://github.com/google/neural-tangents) [:book:](./citations/nguyen2021kipimprovedresults.txt)
+ [Dataset Distillation using Neural Feature Regression](https://arxiv.org/abs/2206.00719) (Yongchao Zhou et al., 2022) [:book:](./citations/zhou2022dataset.txt)


<a name="parametrization" />

### Distilled Dataset Parametrization
+ [Synthesizing Informative Training Samples with GAN](https://arxiv.org/abs/2204.07513) (Bo Zhao et al., 2022) [:octocat:](https://github.com/vico-uoe/it-gan) [:book:](./citations/zhao2022synthesizing.txt)
+ [Dataset Condensation via Efficient Synthetic-Data Parameterization](https://arxiv.org/abs/2205.14959) (Jang-Hyun Kim et al., ICML 2022) [:octocat:](https://github.com/snu-mllab/efficient-dataset-condensation) [:book:](./citations/kim2022dataset.txt)
+ [Remember the Past: Distilling Datasets into Addressable Memories for Neural Networks](https://arxiv.org/abs/2206.02916) (Zhiwei Deng et al., 2022) [:book:](./citations/deng2022remember.txt)


<a name="label" />

### Label Distillation
+ [Flexible Dataset Distillation: Learn Labels Instead of Images](https://arxiv.org/abs/2006.08572) (Ondrej Bohdal et al., NeurIPS 2020 Workshop) [:octocat:](https://github.com/ondrejbohdal/label-distillation) [:book:](./citations/bohdal2020flexible.txt)
+ [Soft-Label Dataset Distillation and Text Dataset Distillation](https://arxiv.org/abs/1910.02551) (Ilia Sucholutsky et al., IJCNN 2021) [:octocat:](https://github.com/ilia10000/dataset-distillation) [:book:](./citations/sucholutsky2021soft.txt)

<a name="benchmark" />

### Benchmark

+ [DC-BENCH: Dataset Condensation Benchmark](https://arxiv.org/abs/2207.09639) (Justin Cui et al., 2022) [:octocat:](https://github.com/justincui03/dc_benchmark) [:book:](./citations/cui2022dc.txt)

<a name="applications" />

## Applications

<a name="privacy" />

### Privacy
+ [SecDD: Efficient and Secure Method for Remotely Training Neural Networks](https://arxiv.org/abs/2009.09155) (Ilia Sucholutsky et al., AAAI 2021 Student Abstract) [:book:](./citations/sucholutsky2021secdd.txt)
+ [Privacy for Free: How does Dataset Condensation Help Privacy?](https://arxiv.org/abs/2206.00240) (Tian Dong et al., ICML 2022) [:book:](./citations/dong2022privacy.txt)

<a name="fed" />

### Federated Learning
+ [Federated Learning via Synthetic Data](https://arxiv.org/abs/2008.04489) (Jack Goetz et al., 2020) [:book:](./citations/goetz2020federated.txt)
+ [Distilled One-Shot Federated Learning](https://arxiv.org/abs/2009.07999) (Yanlin Zhou et al., 2020) [:book:](./citations/zhou2020distilled.txt)
+ [FedSynth: Gradient Compression via Synthetic Data in Federated Learning](https://arxiv.org/abs/2204.01273) (Shengyuan Hu et al., 2022) [:book:](./citations/hu2022fedsynth.txt)
+ [FedDM: Iterative Distribution Matching for Communication-Efficient Federated Learning](https://arxiv.org/abs/2207.09653) (Yuanhao Xiong et al., 2022) [:book:](./citations/xiong2022feddm.txt)

<a name="continual" />

### Continual Learning
+ [Reducing Catastrophic Forgetting with Learning on Synthetic Data](https://arxiv.org/abs/2004.14046) (Wojciech Masarczyk et al., CVPR 2020 Workshop) [:book:](./citations/masarczyk2020reducing.txt)
+ [Condensed Composite Memory Continual Learning](https://arxiv.org/abs/2102.09890) (Felix Wiewel et al., IJCNN 2021) [:octocat:](https://github.com/FelixWiewel/CCMCL) [:book:](./citations/wiewel2021soft.txt)
+ [Distilled Replay: Overcoming Forgetting through Synthetic Samples](https://arxiv.org/abs/2103.15851) (Andrea Rosasco et al., 2021) [:octocat:](https://github.com/andrearosasco/DistilledReplay) [:book:](./citations/rosasco2021distilled.txt)
+ [Sample Condensation in Online Continual Learning](https://arxiv.org/abs/2206.11849) (Mattia Sangermano et al., IJCNN 2022) [:book:](./citations/sangermano2022sample.txt)

<a name="model" />

### Model Compression
+ [PRANC: Pseudo RAndom Networks for Compacting deep models](https://arxiv.org/abs/2206.08464) (Parsa Nooralinejad et al., 2022) [:octocat:](https://github.com/UCDvision/PRANC) [:book:](./citations/nooralinejad2022pranc.txt)

<a name="gnn" />

### Graph Neural Network
+ [Graph Condensation for Graph Neural Networks](https://arxiv.org/abs/2110.07580) (Wei Jin et al., ICLR 2022) [:octocat:](https://github.com/chandlerbang/gcond) [:book:](./citations/jin2022graph.txt)
+ [Condensing Graphs via One-Step Gradient Matching](https://arxiv.org/abs/2206.07746) (Wei Jin et al., KDD 2022) [:octocat:](https://github.com/ChandlerBang/GCond/tree/main/KDD22_DosCond) [:book:](./citations/jin2022condensing.txt)
+ [Graph Condensation via Receptive Field Distribution Matching](https://arxiv.org/abs/2206.13697) (Mengyang Liu et al., 2022) [:book:](./citations/liu2022graph.txt)

<a name="nas" />

### Neural Architecture Search
+ [Generative Teaching Networks: Accelerating Neural Architecture Search by Learning to Generate Synthetic Training Data](https://arxiv.org/abs/1912.07768) (Felipe Petroski Such et al., ICML 2020) [:octocat:](https://github.com/uber-research/GTN) [:book:](./citations/such2020generative.txt)

<a name="kd" />

### Knowledge Distillation
+ [Knowledge Condensation Distillation](https://arxiv.org/abs/2207.05409) (Chenxin Li et al., ECCV 2022) [:octocat:](https://github.com/dzy3/KCD) [:book:](./citations/li2022knowledge.txt)

<a name="medical" />

### Medical
+ [Soft-Label Anonymous Gastric X-ray Image Distillation](https://arxiv.org/abs/2104.02857) (Guang Li et al., ICIP 2020) [:octocat:](https://github.com/Guang000/Awesome-Dataset-Distillation) [:book:](./citations/li2020soft.txt)
+ [Compressed Gastric Image Generation Based on Soft-Label Dataset Distillation for Medical Data Sharing](https://www.journals.elsevier.com/computer-methods-and-programs-in-biomedicine) (Guang Li et al., CMPB 2022) [:book:](./citations/li2022compressed.txt)

<a name="fashion" />

### Fashion, Art, and Design
+ [Wearable ImageNet: Synthesizing Tileable Textures via Dataset Distillation](https://openaccess.thecvf.com/content/CVPR2022W/CVFAD/html/Cazenavette_Wearable_ImageNet_Synthesizing_Tileable_Textures_via_Dataset_Distillation_CVPRW_2022_paper.html) (George Cazenavette et al., CVPR 2022 Workshop) [:globe_with_meridians:](https://georgecazenavette.github.io/mtt-distillation/) [:octocat:](https://github.com/georgecazenavette/mtt-distillation) [:book:](./citations/cazenavette2022textures.txt)
