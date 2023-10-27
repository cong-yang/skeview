# SkeView: Skeleton Ground Truth of Shape and Image Datasets

SkeView is an annotation tool based on the theory of diagnosticity hypothesis ([Amos Tversky, 1977](http://www.ai.mit.edu/projects/dm/Tversky-features.pdf)) for shape and image skeletons. Based on SkeView, we annotate high-quality skeleton Ground Truth (GT) for 17 existing shape and image datasets.
- Image datasets:
  - **SK506**: SK506 (also known as SK-SMALL) was selected from the MS COCO dataset, with 506 natural images (300 for training and 206 for testing) and 16 object classes, including humans, animals, and artifacts. ([Shen et al. IEEE CVPR 2016](https://openaccess.thecvf.com/content_cvpr_2016/papers/Shen_Object_Skeleton_Extraction_CVPR_2016_paper.pdf))
  - **SK1491**: SK1491 (also known as SK-LARGE) is an extension of the SK506 by selecting more images from the MS COCO dataset. It includes 1,491 images (746 for training and 745 for testing). (Shen et al. IEEE TIP 2017)
  - **SYMMAX300**: SYMMAX300 is adapted from the Berkeley Segmentation Dataset (BSDS300) with 300 images (200 for training and 100 for testing). There are multiple targets in most images. This dataset is used for local reflection symmetry detection, which is a low-level image feature, without paying attention to the concept of "object". (Tsogkas et al. ECCV 2012)
  - **SymPASCAL**: SymPASCAL was selected from the PASCAL-VOC dataset, with 1,435 images (648 for training and 787 for testing). Most images contain multiple targets, partial visibility, and complex backgrounds. (IEEE CVPR 2017)
  - 
- bbb


# MoireScape*

Our proposed MoireScape dataset contains two subsets:
 - MoireScape-real: It contains 500 real image pairs for evaluating moiré edge map estimation. Each pair includes a real camera-captured screen image and its moiré layer with the setup in Fig. 3. To extract moire edge map from a moire layer, the more_layer_segmentation tool can be used.
 - MoireScape-synthetic: It contains 18,147 different moiré layers and 4,000 natural images. After varying moiré layers and the their combinations, 50,000 synthetic triplets are collected for the purpose of training (90%) and testing(10%). Each triplet contains a natural image, a moiré layer, and their synthetic mixture.

*: Since each subset surpass 25M, please download them via the online disc link in each text file. 
 
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
