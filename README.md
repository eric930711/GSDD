## :book: **GSDD: Generative Space Dataset Distillation for Image Super-Resolution (AAAI 2024)** :tada:

### :computer: This is the official implementation of GSDD accepted by AAAI-2024.:smile: Thanks for watching! :heart:

***

<img src=https://github.com/eric930711/GSDD/blob/main/Figure/R1.png#pic_center width=70% />

***

# Table of Contents

<details>
  <summary>Abstract</summary>
  
> **Single image super-resolution (SISR), especially in the real world, usually builds a large amount of LR-HR image pairs to learn representations that contain rich textural and structural information. However, relying on massive data for model training not only reduces training efficiency, but also causes heavy data storage burdens. In this paper, we attempt a pioneering study on dataset distillation (DD) for SISR problems to explore how data could be slimmed and compressed for the
task. Unlike previous coreset selection methods which select a few typical examples directly from the original data, we remove the limitation that the selected data cannot be further edited, and propose to synthesize and optimize samples to preserve more task-useful representations. Concretely, by utilizing pre-trained GANs as a suitable approximation of realistic data distribution, we propose GSDD, which distills data in a latent generative space based on GAN-inversion techniques. By optimizing them to match with the practical data distribution in an informative feature space, the distilled data could then be synthesized. Experimental results demonstrate that when trained with our distilled data, GSDD can achieve comparable performance to the state-of-the-art (SOTA) SISR algorithms, while a nearly ×8 increase in training efficiency and a saving of almost 93.2% data storage space can be realized. Further experiments on challenging real-world data also demonstrate the promising generalization ability of GSDD.**
</details>

<details>
  <summary>Method</summary>
  
  ![GSDD](https://github.com/eric930711/GSDD/blob/main/Figure/Framework.png)

</details>

<details>
  <summary>Experiment</summary>

  Our experimental datasets include [OST](https://github.com/xinntao/SFTGAN?tab=readme-ov-file#ost-dataset) and [DPED](https://people.ee.ethz.ch/~ihnatova/).
  
  <details>
    <summary>Quantitative Comparison</summary>
    
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R2.png width=70% />
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R3.png width=70% />
    
  </details>
  <details>
    <summary>Qualitative Presentation</summary>
    
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R2.png width=70% />
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R3.png width=70% />
    
  </details>
  <details>
    <summary>Distilled Samples</summary>
    
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R4.png width=70% />  
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R5.png width=70% />
    
  </details>
</details>

<details>
  <summary>Ablation Study</summary>
  
<figure class="half">
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R6.png width=40% />
  <img src=https://github.com/eric930711/GSDD/blob/main/Figure/R7.png width=40% />
</figure>

</details>
