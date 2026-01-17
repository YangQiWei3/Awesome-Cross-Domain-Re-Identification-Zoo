# 😎 Awesome-Cross-Domain-Re-Identification-Zoo

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/YangQiWei3/Awesome-Aerial-Ground-Object-Re-Identification/graphs/commit-activity)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Welcome to **Awesome-Cross-Domain-Re-Identification-Zoo**!

This repository is a community-driven collection of resources for **Cross-Domain Re-Identification (ReID)**, aiming to systematically summarize ReID tasks under diverse domain gaps. In this “zoo”, *cross-domain* is interpreted broadly to include settings where models transfer across **capture platforms and viewpoints**, **modalities and spectral bands**, **datasets and distribution shifts**, **environmental conditions**, and **attribute changes**, together with other emerging cross-domain ReID scenarios.

At a fundamental level, these cross-domain ReID problems share a common objective, namely how to **align target features across domains**. By organizing these settings and their representative works within a unified repository, we hope to facilitate deeper discussion on the **core nature of cross-domain ReID**, its **principal challenges**, and the **design principles** that effectively address domain misalignment.

Here you will find curated **papers, datasets, benchmarks, methods, and open-source implementations**, accompanied by brief notes when helpful. We welcome any contributions that help advance cross-domain ReID, such as adding new papers or datasets, updating benchmarks, fixing broken links, refining the taxonomy, or improving the overall coverage and readability of this repository.

> 📩 Feel free to open an issue / PR to add papers, code or datasets.

---
# 📖 Table of Contents
- [🌟 Spotlight: Our Contributions](#-spotlight-our-contributions)
- [📊 Publication Trends](#-publication-trends)
- [📝 Papers & Methods](#-papers--methods)
  - [Platform and Viewpoint Gap](#1-platform-and-viewpoint-gap)
    - [Aerial ↔ Ground ReID](#11-aerial--ground-reid)
      - [Image-based AG-ReID](#111-image-based-ag-reid)
      - [Video-based AG-ReID](#112-video-based-ag-reid)
  - [Modality and Spectrum Gap](#2-modality-and-spectrum-gap)
    - [Visible ↔ Infrared ↔ Thermal ReID](#21-visible--infrared--thermal-reid)
      - [Image-based VI-ReID](#211-image-based-vi-reid)
      - [Video-based VI-ReID](#212-video-based-vi-reid)
    - [RGB ↔ Depth](#22-rgb--depth)
    - [Sketch ↔ Photo](#23-sketch--photo)
    - [Image ↔ Text](#24-image--text)
  - [Dataset and Domain Shift](#3-dataset-and-domain-shift)
  - [Condition Gap](#4-condition-gap)
  - [Attribute Shift](#5-attribute-shift)
    - [Clothes-Changing ReID](#51-clothes-changing-reid)  
- [💾 Datasets](#-datasets)
- [📈 Star History](#-star-history)
- [🤝 Contributing](#-contributing)
- [🤝 Acknowledgments](#-acknowledgments)
- [📧 Contact](#-contact)
- [📌 Citation](#-citation)
---
# 🌟 Spotlight: Our Contributions

Selected works from our research group on **cross-domain ReID**:

- **[WACVW 2026]** SAS-VPReID: A Scale-Adaptive Framework with Shape Priors for Video-based Object Re-Identification at Extreme Far Distances  [Paper](https://arxiv.org/pdf/2601.05535) · [Code](https://github.com/YangQiWei3/SAS-VPReID)
- **[Arxiv 2025]** SD-ReID: View-aware Stable Diffusion for Aerial-Ground Object Re-Identification  [Paper](https://arxiv.org/abs/2504.09549)
- **[Arxiv 2025]** LATex: Leveraging Attribute-based Text Knowledge for Aerial-Ground Object Re-Identification  [Paper](https://arxiv.org/abs/2503.23722)
- **[ICASSP 2025]** Hierarchical Proxy Learning for Cloth-Changing Person Re-Identification  [Paper](https://ieeexplore.ieee.org/abstract/document/10889915)

> 📩 Feel free to open an issue if you have any questions about our paper.

---


# 📊 Publication Trends
Automatic statistics based on the papers listed in this repository.

![Publication Trend](assets/publication_trend.svg)

---

# 📝 Papers & Methods

## 📚1 Platform and Viewpoint Gap
> **Platform and Viewpoint Gap** focuses on ReID scenarios in which the domain shift primarily arises from differences in capture platforms and viewpoints. Representative examples include **aerial ↔ ground** matching, high-angle ↔ eye-level viewpoints, long-range ↔ close-range imagery, and cross-camera view changes. Compared with conventional ReID, these settings typically exhibit more pronounced variations in **scale, perspective, occlusion, and background context**, thereby posing a greater challenge for learning representations that generalize across **cross-view** and **cross-platform** distributions.

### 📚1.1 Aerial ↔ Ground ReID
> Aerial ↔ Ground ReID targets person or vehicle re-identification across aerial and ground imaging platforms, where the source and target domains differ substantially in viewpoint geometry and sensing conditions. This setting is characterized by large changes in scale, perspective distortion, and background clutter, and may further involve severe occlusion and limited visual detail due to long-range capture. As a result, effective methods are expected to learn representations that remain discriminative under cross-platform and cross-view distribution shifts, enabling robust matching between UAV-based observations and ground-level camera data.

#### 📝1.1.1 Image-based AG-ReID

| Conference / Journal | Method | Title | Resources |
|:---|:---|:---|:---|
| **AAAI 2026** | TAG-CLIP | Text-based Aerial-Ground Object Retrieval | [Paper](https://arxiv.org/pdf/2511.08369) · [Code](https://github.com/Flame-Chasers/TAG-PR)|
| **AAAI 2026** | — | Semantic-Driven Progressive Refinement for Aerial Ground Person ReID: A Challenging Large-Scale Benchmark | Coming Soon |
| **NeurIPS 2025** | GSAlign | Geometric and Semantic Alignment Network for Aerial-Ground Person Re-Identification | [Paper](https://openreview.net/attachment?id=bxELEjg3VE&name=pdf) · [Code](https://github.com/stone96123/GSAlign?tab=readme-ov-file) |
| **ICCV 2025** | VIF | Bridging the Sky and Ground: Towards View-Invariant Feature Learning for Aerial-Ground Person Re-Identification | [Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Khalid_Bridging_the_Sky_and_Ground_Towards_View-Invariant_Feature_Learning_for_ICCV_2025_paper.html) |
| **Arxiv 2025** | SD-ReID | View-aware Stable Diffusion for Aerial-Ground Person Re-Identification | [Paper](https://arxiv.org/abs/2504.09549) |
| **Arxiv 2025** | LATex | Leveraging Attribute-based Text Knowledge for Aerial-Ground Person Re-Identification | [Paper](https://arxiv.org/abs/2503.23722) |
| **ICME 2025** | DTST | Dynamic Token Selective Transformer for  Aerial-Ground Person Re-Identification | [Paper](https://yuhaiw.github.io/DTS-AGPReID/ICMEYuhai.pdf) · [Code](https://github.com/YuhaiW/reidselecttoken) |
| **CVPR 2025** | SeCap | Self-Calibrating and Adaptive Prompts for Cross-view Person Re-Identification in Aerial-Ground Networks | [Paper](https://arxiv.org/abs/2503.06965) · [Code](https://github.com/wangshining681/SeCap-AGPReID) |
| **TOMM 2025** | CVAF | A CLIP-Based View-Consistent Alignment Framework for Aerial-Ground Person Re-Identification | [Paper](https://dl.acm.org/doi/pdf/10.1145/3785482) |
| **ICIG 2025** | PDPA | Perspective Driven Prototype Alignment for Aerial-Ground Person Re-identification | [Paper](https://link.springer.com/chapter/10.1007/978-981-95-3393-0_42) |
| **自动化学报 2025** | — | Implicit Decoder Alignment for Aerial-ground Person Re-identification | [Paper](https://www.aas.net.cn/cn/article/doi/10.16383/j.aas.c240705) |
| **CVPR 2024** | VDT | View-decoupled Transformer for Person Re-identification under Aerial-ground Camera Network | [Paper](https://arxiv.org/abs/2403.14513) · [Code](https://github.com/LinlyAC/VDT-AGPReID?tab=readme-ov-file) |
| **TITS 2024** | AG-ReID.v2 | Bridging Aerial and Ground Views for Person Re-identification | [Paper](https://arxiv.org/abs/2401.02634) · [Code](https://github.com/huynguyen792/AG-ReID.v2) |
| **ICME 2023** | Explain | Aerial-Ground Person Re-ID | [Paper](https://arxiv.org/abs/2303.08597) |
| **ATR 2017** | — | Person Re-Identification Across Aerial and Ground-Based Cameras by Deep Feature Fusion | [Paper](https://publica.fraunhofer.de/bitstreams/ef904224-f31f-484d-b8d2-56695e46779c/download) |
| **SENSORS 2025** | CVNet | Lightweight Cross-View Vehicle ReID with Multi-Scale Localization | [Paper](https://www.mdpi.com/1424-8220/25/9/2809) |
| **RS 2025** | AGID | Aerial-Ground Cross-View Vehicle Re-Identification: A Benchmark Dataset and Baseline | [Paper](https://www.mdpi.com/2072-4292/17/15/2653) |

<div align="center"><b>🏆 Challenges & Workshops</b></div>

| Conference / Journal | Title | Resources |
|:---|:---|:---|
| **IJCB 2023** | AG-ReID 2023: Aerial-Ground Object Re-identification Challenge Results | [Paper](https://cvlab.cse.msu.edu/pdfs/IJCB_AG_ReID2023_Challenge_Summary_Paper.pdf) |

<div align="center"><b>💾 Datasets</b></div>

| Dataset | Source | Download | Access Code |
| :--- | :--- | :--- | :--- |
| **LAGPeR / G2APS-ReID** | CVPR 2025 | [Link](https://pan.baidu.com/share/init?surl=MRrhqoQzwxw7qOx4Lqdl2g) | - |
| **CARGO** | CVPR 2024 | [Link](https://drive.google.com/file/d/1yDjyH0VtW7efxP3vgQjIqTx2oafCB67t/view) | - |
| **AG-ReID.v2** | TITS 2024 | [Link](https://drive.google.com/drive/folders/16r7G_CuUqfWG6_UCT7goIGRMqJird6vK) | - |
| **AG-ReID** | ICME 2023 | [Link](https://drive.google.com/file/d/1hzieEPlXfjkN3V3XWqI5rAwpF_sCF1K9/view) | - |

#### 📝1.1.2 Video-based AG-ReID
| Conference / Journal | Method | Title | Resources |
|:---|:---|:---|:---|
| **WACVW 2026** | SAS-VPReID | A Scale-Adaptive Framework with Shape Priors for Video-based Person Re-Identification at Extreme Far Distances | [Paper](https://arxiv.org/pdf/2601.05535) · [Code](https://github.com/YangQiWei3/SAS-VPReID) |
| **WACVW 2026** | S3-CLIP | Video Super Resolution for Person-ReID | [Paper](https://arxiv.org/abs/2601.08807) · [Code](https://github.com/TomasDelaney/S3-CLIP) |
| **CVPR 2025** | AG-VPReID | A Challenging Large-Scale Benchmark for Aerial-Ground Video-based Person Re-Identification | [Paper](https://arxiv.org/abs/2503.08121) |
| **IJCB 2025** | VM-TAPS | View-specific Memory with Temporal and Scale Awareness Framework for Video-based Cross-View Person Re-Identification | [Paper](https://www.di.ubi.pt/%7Ehugomcp/doc/rashid_ijcb2025.pdf) · [Code](https://github.com/MdRashidunnabi/VM-TAPS) |
| **TBIOM 2025** | DetReIDX | A Stress-Test Dataset for Real-World UAV-Based Person Recognition | [Paper](https://arxiv.org/pdf/2505.04793) |
| **TBIOM 2025** | MTF–CVReID | Seeing Across Time and Views: Multi-Temporal Cross-View Learning for Robust Video Person Re-Identification | [Paper](https://arxiv.org/pdf/2511.02564) · [Code](https://github.com/MdRashidunnabi/MTF-CVReID) |
| **ECCV 2024** | — | Cross-Platform Video Person ReID: A New Benchmark Dataset and Adaptation Approach | [Paper](https://arxiv.org/abs/2408.07500) · [Code](https://github.com/FHR-L/VSLA-CLIP)  |

<div align="center"><b>🏆 Challenges & Workshops</b></div>

| Conference / Journal | Title | Resources |
|:---|:---|:---|
| **WACV 2026** | VReID-XFD: Video-based Object Re-identification at Extreme Far Distance Challenge Results | [Paper](https://arxiv.org/pdf/2601.01312v1) |
| **IJCB 2025** | AG-VPReID 2025: Aerial-Ground Video-based Object Re-identification Challenge Results | [Paper](https://arxiv.org/pdf/2506.22843) |

<div align="center"><b>💾 Datasets</b></div>

| Dataset | Source | Download | Access Code |
| :--- | :--- | :--- | :--- |
| **DetReIDX** | TBIOM 2025 | [Link](https://github.com/kailashhambarde/DetReIDX/tree/main) | - |
| **AG-VPReID** | CVPR 2025 | [Link](https://drive.google.com/drive/folders/1wtdhKzK9Fbj7xkGAM84KNJ1uYCxSMHdj) | - |
| **IJCB 2025** | AG-VPReID.VIR| [Link](https://drive.google.com/drive/folders/1Iy814PqWjwIZcv6CZpieFju-Dop9Y2G7) | - |

---

#### More Related Exploration

| Conference / Journal | Title | Resources |
|:---|:---|:---|
| **Arxiv 2025** | Multi-modal Multi-platform Person Re-Identification: Benchmark and Method | [Paper](https://arxiv.org/pdf/2503.17096) · [Code](https://github.com/MP-ReID/mp-reid) · [Dataset](https://drive.google.com/file/d/1hImLEMcsBB2kNV4McGyksVAumLjZQoUU/view) |
| **TCSVT 2025** | AEA-FIRM: Adaptive Elastic Alignment with Fine-Grained Representation Mining for Text-based Aerial Pedestrian Retrieval | [Paper](https://ieeexplore.ieee.org/document/11072214) · [Code](https://github.com/xbdxwyh/AEA-FIRM-main) · [Dataset](https://drive.google.com/file/d/1YYIpBDoJzTIwYRlpWUqEHmpo5GK05S_W/view) |
| **IJCB 2025** | AG-VPReID.VIR: Bridging Aerial and Ground Platforms for Video-based Visible-Infrared Person Re-ID | [Paper](https://arxiv.org/abs/2507.17995)|
| **SPL 2025** | Omni-Directional View Person Re-Identification Through 3D Human Reconstruction | [Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10839551) |
| **ACM MM 2024** | AerialGait: Bridging Aerial and Ground Views for Gait Recognition | [Paper](https://dl.acm.org/doi/pdf/10.1145/3664647.3681002) |

---

## 📚2 Modality and Spectrum Gap
> .

### 📚2.1 Visible ↔ Infrared ↔ Thermal ReID
> .

#### 📝2.1.1 Image-based VI-ReID
#### 📝2.1.2 Video-based VI-ReID

### 📚2.2 RGB ↔ Depth
> .

### 📚2.3 Sketch ↔ Photo
> .

### 📚2.4 Image ↔ Text
> .

## 📚3 Dataset and Domain Shift
> .

## 📚4 Condition Gap
> .
## 📚5 Attribute Shift
> .

### 📚5.1 Clothes-Changing ReID
> .

#### 📝5.1.1 Image-based CC-ReID

## 📈 Star History
<picture>
  <source media="(prefers-color-scheme: dark)"
    srcset="https://api.star-history.com/svg?repos=YangQiWei3/Awesome-Aerial-Ground-Object-Re-Identification&type=Date&theme=dark" />
  <source media="(prefers-color-scheme: light)"
    srcset="https://api.star-history.com/svg?repos=YangQiWei3/Awesome-Aerial-Ground-Object-Re-Identification&type=Date" />
  <img alt="Star History Chart"
    src="https://api.star-history.com/svg?repos=YangQiWei3/Awesome-Aerial-Ground-Object-Re-Identification&type=Date" />
</picture>


---

## 🤝 Contributing

PRs / Issues are welcome! Please follow these rules:

1. Add your entry to the correct section (Papers / Challenges / Datasets).
2. Keep tables sorted by **Year (desc)**, then **Venue**.
3. Formatting:

   * Venue in **bold** (e.g., `**CVPR 2025**`)
   * Use `—` if method is unknown
   * Resource order: `Paper · Code · Dataset · Project` (only include available links)

**Template**

```markdown
| **VENUE YEAR** | Method | Paper Title | [Paper](link) · [Code](link) · [Dataset](link) · [Project](link) |
```


---

## 🤝 Acknowledgments

We express our sincere gratitude to the academic community and all researchers contributing to the advancement of Aerial-Ground Object Re-Identification.

## 📧 Contact

Questions, suggestions and collaborations are welcome. Please feel free to reach out:

- **Email**: [dutyqw@mail.dlut.edu.cn](mailto:dutyqw@mail.dlut.edu.cn)
- **GitHub**: [Yang Qiwei](https://github.com/YangQiWei3)

## 📌 Citation

If you find our work or this repository useful in your research, please consider citing:

```bibtex
@article{yang2026sas,
  title={SAS-VPReID: A Scale-Adaptive Framework with Shape Priors for Video-based Person Re-Identification at Extreme Far Distances},
  author={Yang, Qiwei and Zhang, Pingping and Wang, Yuhao and Gong, Zijing},
  journal={arXiv preprint arXiv:2601.05535},
  year={2026}
}

@article{wang2025sd,
  title={SD-ReID: View-aware Stable Diffusion for Aerial-Ground Person Re-Identification},
  author={Wang, Yuhao and Hu, Xiang and Wang, Lixin and Zhang, Pingping and Lu, Huchuan},
  journal={arXiv preprint arXiv:2504.09549},
  year={2025}
}

@article{zhang2025latex,
  title={Latex: Leveraging attribute-based text knowledge for aerial-ground person re-identification},
  author={Zhang, Pingping and Hu, Xiang and Wang, Yuhao and Lu, Huchuan},
  journal={arXiv preprint arXiv:2503.23722},
  year={2025}
}

@INPROCEEDINGS{10889915,
  author={Yu, Chenyang and Liu, Xuehu and Dai, Ju and Zhang, Pingping and Lu, Huchuan},
  booktitle={ICASSP 2025 - 2025 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Hierarchical Proxy Learning for Cloth-Changing Person Re-Identification}, 
  year={2025},
  volume={},
  number={},
  pages={1-5},
  keywords={Training;Multiprotocol label switching;Clothing;Semantics;Signal processing;Feature extraction;Acoustics;Speech processing;Identification of persons;cloth-changing person re-identification;hierarchical proxy learning;sample balance;joint training},
  doi={10.1109/ICASSP49660.2025.10889915}}


@misc{awesome_agpreid,
  title        = {Awesome Aerial-Ground Object Re-Identification},
  author       = {Yang, Qiwei, Zhang, Pingping and Gong, Zijing},
  howpublished = {\url{https://github.com/YangQiWei3/Awesome-Aerial-Ground-Object-Re-Identification}},
  year         = {2026},
  note         = {A curated list of papers, datasets, and resources for AGPReID.}
}