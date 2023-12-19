:book: **GSDD: Generative Space Dataset Distillation for Image Super-Resolution (AAAI-2024)** :tada: :tada: :tada:

:computer: This is the official version of the implementation of the paper GSDD accepted at the 38th Annual AAAI Conference on Artificial Intelligence.

![First page](https://github.com/eric930711/GSDD/blob/main/Figure/R1.png)

# Table of Contents

<details>
  <summary>Abstract</summary>
  
  Single image super-resolution (SISR), especially in the real world, usually builds a large amount of LR-HR image pairs to learn representations that contain rich textural and structural information. However, relying on massive data for model training not only reduces training efficiency, but also causes heavy data storage burdens. In this paper, we attempt a pioneering study on dataset distillation (DD) for SISR problems to explore how data could be slimmed and compressed for the
task. Unlike previous coreset selection methods which select a few typical examples directly from the original data, we remove the limitation that the selected data cannot be further edited, and propose to synthesize and optimize samples to preserve more task-useful representations. Concretely, by utilizing pre-trained GANs as a suitable approximation of realistic data distribution, we propose GSDD, which distills data in a latent generative space based on GAN-inversion techniques. By optimizing them to match with the practical data distribution in an informative feature space, the distilled data could then be synthesized. Experimental results demonstrate that when trained with our distilled data, GSDD can achieve comparable performance to the state-of-the-art (SOTA) SISR algorithms, while a nearly ×8 increase in training efficiency and a saving of almost 93.2% data storage space can be realized. Further experiments on challenging real-world data also demonstrate the promising generalization ability of GSDD.
</details>

<details>
  <summary>Methods</summary>
  
![GSDD](https://github.com/eric930711/GSDD/blob/main/Figure/Framework.png)
</details>


<details>
  <summary>Results</summary>

![synthetic-SR](https://github.com/eric930711/GSDD/blob/main/Figure/R2.png)

![realistic-SR](https://github.com/eric930711/GSDD/blob/main/Figure/R3.png)
</details>
