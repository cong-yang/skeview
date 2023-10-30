# SkeView: Skeleton Ground Truth of Shape and Image Datasets

SkeView is an annotation tool based on the theory of diagnosticity hypothesis ([Amos Tversky, Psychological Review, 1977](http://www.ai.mit.edu/projects/dm/Tversky-features.pdf)) for shape and image skeletons. Based on SkeView, we annotate high-quality skeleton Ground Truth (GT) of 17 existing shape and image datasets. 

Paper link: [Skeleton Ground Truth Extraction: Methodology, Annotation Tool and Benchmarks](https://arxiv.org/abs/2310.06437) (Accepted by IJCV 2023).

<img src="skeview.jpg" height="250">

## Datasets

- Image datasets:
  - **SK506**: SK506 (also known as SK-SMALL) was selected from the MS COCO dataset, with 506 natural images (300 for training and 206 for testing) and 16 object classes, including humans, animals, and artifacts. ([Shen et al. IEEE CVPR 2016](https://openaccess.thecvf.com/content_cvpr_2016/papers/Shen_Object_Skeleton_Extraction_CVPR_2016_paper.pdf))
  - **SK1491**: SK1491 (also known as SK-LARGE) is an extension of the SK506 by selecting more images from the MS COCO dataset. It includes 1,491 images (746 for training and 745 for testing). ([Shen et al. IEEE TIP 2017](https://ieeexplore.ieee.org/abstract/document/8000414))
  - **SYMMAX300**: SYMMAX300 is adapted from the Berkeley Segmentation Dataset (BSDS300) with 300 images (200 for training and 100 for testing). There are multiple targets in most images. This dataset is used for local reflection symmetry detection, which is a low-level image feature, without paying attention to the concept of "object". ([Tsogkas et al. ECCV 2012](https://inria.hal.science/hal-00856535/document))
  - **SymPASCAL**: SymPASCAL was selected from the PASCAL-VOC dataset, with 1,435 images (648 for training and 787 for testing). Most images contain multiple targets, partial visibility, and complex backgrounds. ([Ke et al. IEEE CVPR 2017](https://openaccess.thecvf.com/content_cvpr_2017/papers/Ke_SRN_Side-output_Residual_CVPR_2017_paper.pdf))
- Both image and shape datasets:
  - **EM200**: EM200 contains 200 microscopic images (10 classes) of environmental microorganisms (EM). ([Yang et al. ICPR 2014](https://projet.liris.cnrs.fr/imagine/pub/proceedings/ICPR-2014/data/5209d374.pdf))
  - **SmithsonianLeaves**: SmithsonianLeaves contains 343 leaves (187 for training and 156 for testing) from 93 different species of plants. ([Ling et al. IEEE T-PAMI 2007](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=c9bb27a60b6c2555a4c01c4c0b8808f1e3625403))
  - **WH-SYMMAX**: WH-SYMMAX contains 328 cropped images (228 for training and 100 for testing) from the Weizmann Horse dataset. Each image contains one manually segmented target. ([Shen et al. Pattern Recognition 2016](https://www.vlrlab.net/admin/uploads/avatars/Multiple_instance_subspace_learning_via_partial_random_projection_tree_for_local_reflection_symmetry_in_natural_images.pdf))
- Shape datasets:
  - **Animal2000**: Animal2000 contains 2,000 shapes (20 categories, 100 shapes each) ranging from poultry and domestic pets to insects and wild animals. Each class is characterized by large intra-class shape variations. ([Bai et al. ICCV Workshops 2009](http://pages.ucsd.edu/~ztu/publication/iccv09_nordia_ics.pdf))
  - **ArticulatedShapes**: ArticulatedShapes contains 40 images from eight different objects. This challenging dataset consists of various tools, including scissors with holes. ([Ling et al. IEEE T-PAMI 2007](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=c9bb27a60b6c2555a4c01c4c0b8808f1e3625403))
  - **Kimia99**: Kimia99 contains 99 shapes (9 categories, 11 shapes each) assembled from various sources such as tools and hands, etc. ([Sebastian et al. IEEE T-PAMI 2004](https://ieeexplore.ieee.org/abstract/document/1273924))
  - **MPEG7**: MPEG7 contains 1,400 (70 categories, 20 shapes each) shapes defined by their outer closed contours. It poses challenges with respect to deformation (e.g., change of viewpoints and non-rigid object motion) and noises (e.g., quantization and segmentation noise). This dataset is actively used for benchmarking shape representation, matching, and retrieval algorithms. ([Latecki et al. IEEE CVPR 2000](https://ieeexplore.ieee.org/abstract/document/855850))
  - **Kimia216**: Kimia216 contains 216 shapes (18 categories, 12 shapes each) selected from the MPEG7 dataset. It is actively used in skeleton extraction, pruning, matching, and shape retrieval scenarios. ([Sebastian et al. IEEE T-PAMI 2004](https://ieeexplore.ieee.org/abstract/document/1273924))
  - **MPEG400**: MPEG400 contains 400 shapes selected from the MPEG7 dataset (20 categories, 20 shapes each). Instead of directly using the original shapes, boundary noises of these shapes were manually removed for ablation study. ([Yang et al. IEEE ICIP 2014](https://ieeexplore.ieee.org/abstract/document/7025446))
  - **Tetrapod120**: Tetrapod120 contains 120 tetrapod animal shapes from six classes. As the shapes of some species are visually similar, this dataset is normally employed to evaluate shape matching and fine-grained classification algorithms. ([Yang et al. Pattern Recognition 2016](https://www.sciencedirect.com/science/article/abs/pii/S0031320316000431))
  - **SwedishLeaves**: SwedishLeaves contains 1,125 leaf shapes from 15 different Swedish tree species, with 75 leaves per species (25 for training, 50 for testing). This dataset is challenging as some species are quite similar. ([Oskar Söderkvist, Linköping University, 2001](https://www.diva-portal.org/smash/get/diva2:303038/FULLTEXT01.pdf))
  - **Tari56**: Tari56 contains 56 shapes (14 categories, 4 shapes each) for evaluating matching performance under visual transformations. Shapes of the same category show variations in orientation, scale, articulation, and small boundary details. ([Asian et al. ICCV 2005](https://ieeexplore.ieee.org/abstract/document/1544875))


## Format

<img src="matlab.jpg" height="150">

To ensure the smoothness of your research, we provide the original shapes/images, ground truth, and thumb on this page: 
- **Original Shapes/Images**: Original data from various sources, such as GitHub pages, personal webpages, and email exchanges. To the best of our knowledge, this is the most complete zoo of existing shape and image datasets. We do our best to push this domain forward. If you find any copyright issues, please contact me via [email](https://cong-yang.github.io/).
- **Ground Truth**: With .mat and .png formats.
  - .mat: for Matlab users. Each file contains three cells:
    - cell 1: binary shape (aa = mysaving_mat{1};)
    - cell 2: component of ground truth (aa = mysaving_mat{2};), with two sub_cells:
      - sub_cell 1: list of endpoints;
      - sub_cell 2: list of branches; Each branch is represented by endpoint1, endpoint2, and skeleton path between them. Users can conveniently evaluate skeleton matching methods (e.g., [skeleton path similarity](https://ieeexplore.ieee.org/document/4359369)) with them.
    - cell 3: binary skeleton ground truth (aa = mysaving_mat{3};)
  - .png: for Python users. A binary image with skeleton ground truth. Alternatively, users can covert the endpoint and branch lists from .mat files.
- **Thumb**: Visualization of the integrated shape/image and the ground truth.

*: Since each zip file surpasses 25M, please download them via the Google Drive disc links in the Download section.

## Download

Freely download the aforementioned files independently or in one folder from Google Drive based on your needs:

- **Independently**

| Dataset  | Type | Original Data |  Ground Truth  |  Thumb  |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| SK506 | image | [Download](https://drive.google.com/file/d/1YT7e2xejEhQ-rmkDk2TFEzjHrFbK4Yuw/view?usp=sharing) | [Download](https://drive.google.com/file/d/1XDEashqwtZh_0mck48h82A7IwEA-j5rg/view?usp=sharing) | [Download](https://drive.google.com/file/d/1MZKJcRI1Vtyn0Lv_-g-LnWuFFgQyu425/view?usp=sharing) |
| SK1491 | image  | [Download](https://drive.google.com/file/d/1yTlI7b-XC4PHA2NW_sT2OO2ZQrhHRHoe/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1vlGFOy1PzgMuojwXLPLPatHsE5lzzU1r/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1glKWiY8B5almi9N5k0bMm9KRhzlRifYR/view?usp=drive_link) |
| SYMMAX300  | image  | [Download](https://drive.google.com/file/d/1XxgY-7TbiJVaWp9FMhc8f0Vr7R2gG57o/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1ZHhgy8u1xM_nNk1ZWC4q_24RfkKdJbyM/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1tWi7ynb5WPOZMtB8rIJANNrf-f-2tbC_/view?usp=drive_link) |
| SymPASCAL  | image  | [Download](https://drive.google.com/file/d/1yYTkuDNQTI1UMHRb5y6jxnpbOFcRQgkt/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1WoqEcJ8y3iGJPkSOxO_wY4MC2GDV9LSI/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1NHJny7Ft3y04_NAhT6yOFzyC1aEfzwR2/view?usp=drive_link) |
| EM200  | image and shape  | [Download](https://drive.google.com/file/d/1MsXX83xSs_ZrhODErrMXzHpWGVdjW2n4/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1dxDGnokJmA6x1yal_0KrppA2j38OhBUg/view?usp=drive_link) | [Download](https://drive.google.com/file/d/11zV4g7dl0DH_KWgBGwtiQLwZPLrjglE-/view?usp=drive_link) |
| SmithsonianLeaves  | image and shape  | [Download](https://drive.google.com/file/d/12hNjLCWaQh0FmDCwIXUIf4pI3H__ygSm/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1iC0oU-tNAqA8inOGQciJqJSL3Ud7bJ6R/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1QtspopRC04HhNSLsnb_V6KN9xpt1fLZ7/view?usp=drive_link) |
| WH-SYMMAX  | image and shape  | [Download](https://drive.google.com/file/d/1OQzi5goTCVaqQsL30S4sEhYBq3FUIv_Z/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1h4WjROuocIhEdxU1nn2KmS8IcIDjw754/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1sRYLmjPPHCgsgLqVn2U_4ZisKreVyPnV/view?usp=drive_link) |
| Animal2000  | shape | [Download](https://drive.google.com/file/d/1vmksd2CRLihgYa__WH95ouAiu4CFoeNm/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1Fjrfx6pph2oFTqRz5tdScB85yeWy-2l2/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1oxtsKDtdNKUd_5lLGVYYwoY1oOZNc9b9/view?usp=drive_link) |
| ArticulatedShapes  | shape  | [Download](https://drive.google.com/file/d/1wzA4T7-8iDYyXGj1g81HXq_uWN5HwysA/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1d8RuEux48vVtMy-bukBX-IsMftQZOauI/view?usp=sharing) | [Download](https://drive.google.com/file/d/1iI75OA5udE3OPhYUXcQi2J46d_puctcO/view?usp=drive_link) |
| Kimia99  | shape  | [Download](https://drive.google.com/file/d/1mWIrVJ127d-3UTx8fDuSv9IeAVIIpCAG/view?usp=drive_link) | [Download](https://drive.google.com/file/d/14O9Q4bmdaTk-W_8bEDXiXZQGc-7hi7pW/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1FR1f6GFm-letWhJuzYtYTWKjtb1Ivc5X/view?usp=drive_link) |
| MPEG7  | shape  | [Download](https://drive.google.com/file/d/1W4n8gdi0wOx3YPcqlmVd1cEn5pXsIyyJ/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1_drMe5Tba-A9Fr1VtJFGAX0FP2jBQU9R/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1k_4qfSx_j6pXo4B4VGuR9dZM1ZbW4PbP/view?usp=drive_link) |
| Kimia216  | shape  | [Download](https://drive.google.com/file/d/16KyJRlAWJmGe32EN75aoZH7D3XHMXAxb/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1D_wLfITpmRRhy00zXdZWK9-XPdXYRYK9/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1qSv8sOX7kfUXE8rHUHhMp9jq-dvqjYrn/view?usp=drive_link) |
| MPEG400  | shape  | [Download](https://drive.google.com/file/d/1Vf3H7oP1PSIdtxqo0-6lVrmEKnY3p2xV/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1m04__AhdUy0d_uKk5pmOGQb-6GIcT_wD/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1yHh3veW5h8U88nIfWykRiz4ugGB3-apG/view?usp=drive_link) |
| Tetrapod120  | shape  | [Download](https://drive.google.com/file/d/1P-DXfDNHoFZiBEk2wXB91w8tHzuPTT5o/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1vtawOSMS4qT9slYSc19ybHIWnNarybEg/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1Zvtosxz6y_l6vrDgjYH50QAi2yEi1pR4/view?usp=drive_link) |
| SwedishLeaves  | shape  | [Download](https://drive.google.com/file/d/1y9EwKsq_dnNLNkz7gnMCADG2nmh3zqJr/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1V_9CcW_sXtj9N5cAkyhTEk5IPQ-L6g3C/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1eOwKIB0N_MBrc0dFBm0T680uqNZ4wAo2/view?usp=drive_link) |
| Tari56  | shape  | [Download](https://drive.google.com/file/d/13uX2SW19dJJeGzgD2Tg0jvFeqz-hgvHh/view?usp=drive_link) | [Download](https://drive.google.com/file/d/17DKRw8Y-g07WMexCcBpS3WmXgsQylooW/view?usp=drive_link) | [Download](https://drive.google.com/file/d/1de3F4mhJUVMsdaME8nto-mdm8fTtbvHY/view?usp=drive_link) |

- **All in One Folder**
  - [Download](https://drive.google.com/drive/folders/1F1TEZOgShNSGZn2uBtbw0xYen25zsPn9?usp=sharing)
 
## Citation

If you benefit from this work, please cite our paper:

	@article{Yang2023SkeView,
		author = {Yang, Cong and Indurkhya, Bipin and See, John and Gao, Bo and Ke, Yan and Boukhers, Zeyd and Yang, Zhenyu and Grzegorzek, Marcin},
		title = {Skeleton Ground Truth Extraction: Methodology, Annotation Tool and Benchmarks},
		journal = {International Journal of Computer Vision},
            volume = {},
            pages = {1-23},
            year = {2023}
	}
