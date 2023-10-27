# SkeView: Skeleton Ground Truth of Shape and Image Datasets

SkeView is an annotation tool based on the theory of diagnosticity hypothesis ([Amos Tversky, Psychological Review, 1977](http://www.ai.mit.edu/projects/dm/Tversky-features.pdf)) for shape and image skeletons. Based on SkeView, we annotate high-quality skeleton Ground Truth (GT) for 17 existing shape and image datasets.

<img src="skeview.jpg" height="300">

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


## Dataformat

Our proposed MoireScape dataset contains two subsets:
 - MoireScape-real: It contains 500 real image pairs for evaluating moiré edge map estimation. Each pair includes a real camera-captured screen image and its moiré layer with the setup in Fig. 3. To extract moire edge map from a moire layer, the more_layer_segmentation tool can be used.
 - MoireScape-synthetic: It contains 18,147 different moiré layers and 4,000 natural images. After varying moiré layers and the their combinations, 50,000 synthetic triplets are collected for the purpose of training (90%) and testing(10%). Each triplet contains a natural image, a moiré layer, and their synthetic mixture.

*: Since each subset surpass 25M, please download them via the online disc link in each text file. 

## Download

Our proposed MoireScape dataset contains two subsets:
 - MoireScape-real: It contains 500 real image pairs for eval
 
## Citation

If you benefit from this work, please cite the mentioned and our paper:

	@article{Yang2023Moire,
		author = {Cong Yang and Zhenyu Yang and Yan Ke and Tao Chen and Marcin Grzegorzek and John See},
		title = {Doing More With Moiré Pattern Detection in Digital Photos},
		journal = {IEEE Transactions on Image Processing},
            volume = {32},
            pages = {694-708},
            year = {2023}
	}
