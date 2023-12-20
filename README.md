### :book: **GSDD: Generative Space Dataset Distillation for Image Super-Resolution (AAAI2024)** :tada:

#### :computer: This is the official implementation of GSDD accepted by AAAI-2024.:smile: Thanks for watching! :heart: 

**:page_facing_up: [Paper](https://github.com/eric930711/GSDD) :scroll: [Supp](https://www.google.com/intl/zh-CN/drive/features.html) :chart_with_upwards_trend: [Poster](https://github.com/eric930711/GSDD) :movie_camera: [Video](https://www.youtube.com/@RealAAAI)**

***
### Overview
<div align=center>
<img src=https://github.com/eric930711/GSDD/blob/main/Figure/R1.png#pic_center width=80% />
</div>

***
###  Setup Environment

```
conda create -n GSDD python=3.8
conda activate GSDD

pip install -r requirements.txt
```
###  Dependencies
```
NVIDIA RTX3090Ti
Windows 10 or Ubuntu
CUDA = V11.0
```

###  Usage

Pretrained models can be downloaded [here](https://www.google.com/intl/zh-CN/drive/features.html).</br>
Distilled samples can be downloaded [here](https://www.google.com/intl/zh-CN/drive/features.html).

#### Demo
```
python demo_GSDD.py
```

#### Train
```
python train_GSDD.py
```
#### Test
```
python test_GSDD.py
```
Some available options:

- ```--dataset: training and testing dataset```
- ```--batch_size: batch size```

### Table of Contents

<details>
  <summary>Abstract (click me)</summary>
  
> **Single image super-resolution (SISR), especially in the real world, usually builds a large amount of LR-HR image pairs to learn representations that contain rich textural and structural information. However, relying on massive data for model training not only reduces training efficiency, but also causes heavy data storage burdens. In this paper, we attempt a pioneering study on dataset distillation (DD) for SISR problems to explore how data could be slimmed and compressed for the
task. Unlike previous coreset selection methods which select a few typical examples directly from the original data, we remove the limitation that the selected data cannot be further edited, and propose to synthesize and optimize samples to preserve more task-useful representations. Concretely, by utilizing pre-trained GANs as a suitable approximation of realistic data distribution, we propose GSDD, which distills data in a latent generative space based on GAN-inversion techniques. By optimizing them to match with the practical data distribution in an informative feature space, the distilled data could then be synthesized. Experimental results demonstrate that when trained with our distilled data, GSDD can achieve comparable performance to the state-of-the-art (SOTA) SISR algorithms, while a nearly ×8 increase in training efficiency and a saving of almost 93.2% data storage space can be realized. Further experiments on challenging real-world data also demonstrate the promising generalization ability of GSDD.**
</details>

<details>
  <summary>Method</summary>
  
  ![GSDD](https://github.com/eric930711/GSDD/blob/main/Figure/Framework.png)

</details>

<details>
  <summary>Datasets</summary></br>
  
  **Our experimental datasets include [OST](https://github.com/xinntao/SFTGAN?tab=readme-ov-file#ost-dataset) and [DPED](https://people.ee.ethz.ch/~ihnatova/). The distilled OST image data (i.e., ICP=50, 100, 200, and 500) will be published soon.**
</details>
  
  <details>
    <summary>Quantitative Comparison</summary>
    
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R8.png width=100% />
  <figure class="half">
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R9.png width=49% />
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R10.png width=49% />
  </figure>
    
  </details>
  <details>
    <summary>Qualitative Presentation</summary>
    
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R2.png width=100% />
  <div align=center>
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R3.png width=70% />
  </div>
    
  </details>
  <details>
    <summary>Distilled Samples Showcase</summary>
  <div align=center>  
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R4.png width=70% />
  </div>
    
  </details>

  <details>
    <summary>Influence of Varying ICP Numbers</summary>

  <div align=center>
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R5.png width=70% />
  </div>
    
  </details>
  
  <details>
  <summary>Ablation Study</summary>
  
<figure class="half">
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R6.png width=49% />
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R7.png width=49% />
</figure>
</details>

</details>

<details>
  <summary>Conclusion</summary>
  
 > **This paper focuses on exploring the possibility of applying DD to benefit low-level CV tasks (especially for SISR). Overall, we propose a GSDD framework that optimizes and synthesizes training samples by the GAN-inversion manipulation in a latent generative space. Our optimization process is based on a distribution- matching data condensation strategy, so that the SISR network can have comparable performance to models trained on the original dataset. We further improve the approach by proposing a distillation loss with the regularization term R. Finally, we demonstrate its effectiveness via extensive experiments. We achieve a competitive performance compared to SOTA SISR solutions under the premise of a nearly ×8 increase in training efficiency and a saving of almost 93.2% data storage space. We wish that the study opens a new perspective in SR research and expect to see it facilitates more practical applications in the future.**
</details>

***

### :star: Acknowledgement :star:

**This work received strong support from [SSL](https://github.com/SSL92) and Tom Cai. We would like to thank them!** :handshake::handshake::handshake:
  
