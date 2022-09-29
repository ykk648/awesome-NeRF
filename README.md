# Awesome Neural Radiance Fields (NeRF) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of awesome neural radiance fields (NeRF) papers. All papers are grouped according to keywords/tasks, and sorted by year. We hope this review can help peers who are interested in conducting NeRF related research.

## Contributing
Warmly welcome everyone to participate in this project!!! If you are interested in joining our team and organizing NeRF related papers/codes/projects together, please submit PR according to the following guide. We'll put your name on the list of contributors.


[Submit a Pull Request](./submit-pr.md)

## Table of Contents

- [Papers](#Papers)
    - [Survey](#survey)
    - [NeRF](#nerf)
        - [Data Augmentation](#data-augmentation)
        - [Few shot](#few-shot)
        - [Rendering Performance](#rendering-performance)
        - [Theory](#theory)
        - [Training & Inference Efficiency](#training--inference-efficiency)
    - [NeRF Related Tasks](#nerf-related-tasks)
        - [Deblur & Denoise](#deblur--denoise)
        - [Depth Estimation](#depth-estimation)
        - [Editing](#editing)
        - [Face](#face)
        - [High Dynamic Range (HDR)](#high-dynamic-range-hdr)
        - [Human](#human)
        - [Large Scale Scene](#large-scale-scene)
        - [Pose Misalignment](#pose-misalignment)
        - [Stylized](#stylized)
        - [Surface Reconstruction](#surface-reconstruction)
        - [Text & Image Guided Generation](#text--image-guided-generation)
        - [Video](#video)
        - [View Synthesis Extrapolation](#view-synthesis-extrapolation)
    - [Unclassified](#unclassified)
- [Datasets](#datasets)
- [Talks & Videos](#talks--videos)
- [Blogs](#blogs)
- [Acknowledgment](#acknowledgment)
- [Team](#team)


## Papers

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2020|ECCV|[TF](https://github.com/bmild/nerf) [Torch](https://github.com/yenchenlin/nerf-pytorch)|[NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis](https://dl.acm.org/doi/pdf/10.1145/3503250)|

### Survey

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|Computer Graphics Forum||[Neural Fields in Visual Computing and Beyond](https://arxiv.org/pdf/2111.11426.pdf)||
|2020|Computer Graphics Forum||[State of the Art on Neural Rendering](https://onlinelibrary.wiley.com/doi/am-pdf/10.1111/cgf.14022)||

### NeRF

#### Data Augmentation

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Torch](https://github.com/VITA-Group/Aug-NeRF)|[Aug-NeRF: Training Stronger Neural Radiance Fields with Triple-Level Physically-Grounded Augmentations](https://openaccess.thecvf.com/content/CVPR2022/papers/Chen_Aug-NeRF_Training_Stronger_Neural_Radiance_Fields_With_Triple-Level_Physically-Grounded_Augmentations_CVPR_2022_paper.pdf)|

#### Few Shot

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[Dense Depth Priors for Neural Radiance Fields from Sparse Input Views](https://openaccess.thecvf.com/content/CVPR2022/papers/Roessle_Dense_Depth_Priors_for_Neural_Radiance_Fields_From_Sparse_Input_CVPR_2022_paper.pdf)|
|2022|CVPR|[TF](https://m-niemeyer.github.io/regnerf)|[RegNeRF: Regularizing Neural Radiance Fields for View Synthesis from Sparse Inputs](https://openaccess.thecvf.com/content/CVPR2022/papers/Niemeyer_RegNeRF_Regularizing_Neural_Radiance_Fields_for_View_Synthesis_From_Sparse_CVPR_2022_paper.pdf)|
|2022|CVPR||[AutoRF: Learning 3D Object Radiance Fields from Single View Observation](https://openaccess.thecvf.com/content/CVPR2022/papers/Muller_AutoRF_Learning_3D_Object_Radiance_Fields_From_Single_View_Observations_CVPR_2022_paper.pdf)|[Project Page](https://sirwyver.github.io/AutoRF/)|
|2022|CVPR|[Torch](https://github.com/mjmjeong/InfoNeRF)|[InfoNeRF: Ray Entropy Minimization for Few-Shot Neural Volume Rendering](https://openaccess.thecvf.com/content/CVPR2022/papers/Kim_InfoNeRF_Ray_Entropy_Minimization_for_Few-Shot_Neural_Volume_Rendering_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/dunbar12138/DSNeRF)|[Depth-supervised NeRF: Fewer Views and Faster Training for Free](https://openaccess.thecvf.com/content/CVPR2022/papers/Deng_Depth-Supervised_NeRF_Fewer_Views_and_Faster_Training_for_Free_CVPR_2022_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/ajayjain/DietNeRF)|[Putting NeRF on a Diet: Semantically Consistent Few-Shot View Synthesis](https://openaccess.thecvf.com/content/ICCV2021/papers/Jain_Putting_NeRF_on_a_Diet_Semantically_Consistent_Few-Shot_View_Synthesis_ICCV_2021_paper.pdf)|[Project Page](https://www.ajayj.com/dietnerf)|
|2021|ICCV|[Torch](https://github.com/yilundu/nerflow)|[Neural Radiance Flow for 4D View Synthesis and Video Processing](https://openaccess.thecvf.com/content/ICCV2021/papers/Du_Neural_Radiance_Flow_for_4D_View_Synthesis_and_Video_Processing_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/apchenstu/mvsnerf)|[MVSNeRF: Fast Generalizable Radiance Field Reconstruction from Multi-View Stereo](https://openaccess.thecvf.com/content/ICCV2021/papers/Chen_MVSNeRF_Fast_Generalizable_Radiance_Field_Reconstruction_From_Multi-View_Stereo_ICCV_2021_paper.pdf)|[Project Page](https://apchenstu.github.io/mvsnerf/)|
|2021|CVPR|[Torch](https://github.com/sxyu/pixel-nerf)|[pixelNeRF: Neural Radiance Fields from One or Few Images](https://openaccess.thecvf.com/content/CVPR2021/papers/Yu_pixelNeRF_Neural_Radiance_Fields_From_One_or_Few_Images_CVPR_2021_paper.pdf)|[Project Page](https://alexyu.net/pixelnerf/)|

#### Rendering Performance

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[Ref-NeRF: Structured View-Dependent Appearance for Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR||[Urban Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Rematas_Urban_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/idiap/GeoNeRF)|[GeoNeRF: Generalizing NeRF with Geometry Priors](https://openaccess.thecvf.com/content/CVPR2022/papers/Johari_GeoNeRF_Generalizing_NeRF_With_Geometry_Priors_CVPR_2022_paper.pdf)|[Project Page](https://www.idiap.ch/paper/geonerf/)|
|2022|CVPR||[NeRFReN: Neural Radiance Fields with Reflections](https://openaccess.thecvf.com/content/CVPR2022/papers/Guo_NeRFReN_Neural_Radiance_Fields_With_Reflections_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/VITA-Group/Aug-NeRF)|[Aug-NeRF: Training Stronger Neural Radiance Fields with Triple-Level Physically-Grounded Augmentations](https://openaccess.thecvf.com/content/CVPR2022/papers/Chen_Aug-NeRF_Training_Stronger_Neural_Radiance_Fields_With_Triple-Level_Physically-Grounded_Augmentations_CVPR_2022_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/quan-meng/gnerf)|[GNeRF: GAN-based Neural Radiance Field without Posed Camera](https://openaccess.thecvf.com/content/ICCV2021/papers/Meng_GNeRF_GAN-Based_Neural_Radiance_Field_Without_Posed_Camera_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/autonomousvision/unisurf)|[UNISURF: Unifying Neural Implicit Surfaces and Radiance Fields for Multi-View Reconstruction](https://openaccess.thecvf.com/content/ICCV2021/papers/Oechsle_UNISURF_Unifying_Neural_Implicit_Surfaces_and_Radiance_Fields_for_Multi-View_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/vincentfung13/MINE)|[MINE: Towards Continuous Depth MPI with NeRF for Novel View Synthesis](https://openaccess.thecvf.com/content/ICCV2021/papers/Li_MINE_Towards_Continuous_Depth_MPI_With_NeRF_for_Novel_View_ICCV_2021_paper.pdf)|
|2021|ICCV|[TF](https://github.com/google/nerfies)|[Nerfies: Deformable Neural Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/Park_Nerfies_Deformable_Neural_Radiance_Fields_ICCV_2021_paper.pdf)|[Project Page](https://nerfies.github.io/)|

#### Theory

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2020|ECCV|[TF](https://github.com/bmild/nerf) [Torch](https://github.com/yenchenlin/nerf-pytorch)|[NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis](https://dl.acm.org/doi/pdf/10.1145/3503250)|

#### Training & Inference Efficiency

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Torch](https://github.com/Xharlie/pointnerf)|[Point-NeRF: Point-based Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Xu_Point-NeRF_Point-Based_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/lwwu2/diver-rt)|[DIVeR: Real-time and Accurate Neural Radiance Fields with Deterministic Integration for Volume Rendering](https://openaccess.thecvf.com/content/CVPR2022/papers/Wu_DIVeR_Real-Time_and_Accurate_Neural_Radiance_Fields_With_Deterministic_Integration_CVPR_2022_paper.pdf)|
|2022|CVPR||[Fourier PlenOctrees for Dynamic Radiance Field Rendering in Real-time](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Fourier_PlenOctrees_for_Dynamic_Radiance_Field_Rendering_in_Real-Time_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/sunset1995/DirectVoxGO)|[Direct Voxel Grid Optimization: Super-fast Convergence for Radiance Fields Reconstruction](https://openaccess.thecvf.com/content/CVPR2022/papers/Sun_Direct_Voxel_Grid_Optimization_Super-Fast_Convergence_for_Radiance_Fields_Reconstruction_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/dvlab-research/EfficientNeRF)|[EfficientNeRF – Efficient Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_EfficientNeRF__Efficient_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR||[Mip-NeRF 360: Unbounded Anti-Aliased Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Barron_Mip-NeRF_360_Unbounded_Anti-Aliased_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2021|ICCV|[TF](https://github.com/google/mipnerf)|[Mip-NeRF: A Multiscale Representation for Anti-Aliasing Neural Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/Barron_Mip-NeRF_A_Multiscale_Representation_for_Anti-Aliasing_Neural_Radiance_Fields_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/sxyu/plenoctree)|[PlenOctrees for Real-time Rendering of Neural Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/Yu_PlenOctrees_for_Real-Time_Rendering_of_Neural_Radiance_Fields_ICCV_2021_paper.pdf)|[Project Page](https://alexyu.net/plenoctrees/)|
|2021|ICCV|[Torch](https://github.com/creiser/kilonerf)|[KiloNeRF: Speeding up Neural Radiance Fields with Thousands of Tiny MLPs](https://openaccess.thecvf.com/content/ICCV2021/papers/Reiser_KiloNeRF_Speeding_Up_Neural_Radiance_Fields_With_Thousands_of_Tiny_ICCV_2021_paper.pdf)|
|2021|ICCV|[TF](https://github.com/google-research/google-research/tree/master/snerg)|[Baking Neural Radiance Fields for Real-Time View Synthesis](https://openaccess.thecvf.com/content/ICCV2021/papers/Hedman_Baking_Neural_Radiance_Fields_for_Real-Time_View_Synthesis_ICCV_2021_paper.pdf)|[Project Page](https://phog.github.io/snerg/)|
|2021|CVPR|[TF](https://github.com/google-research/google-research/tree/master/snerg)|[DeRF: Decomposed Radiance Fields](https://openaccess.thecvf.com/content/CVPR2021/papers/Rebain_DeRF_Decomposed_Radiance_Fields_CVPR_2021_paper.pdf)|[Project Page](https://ubc-vision.github.io/derf/)|

### NeRF Related Tasks

#### Deblur & Denoise

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Torch](https://github.com/limacv/Deblur-NeRF)|[Deblur-NeRF: Neural Radiance Fields from Blurry Images](https://openaccess.thecvf.com/content/CVPR2022/papers/Ma_Deblur-NeRF_Neural_Radiance_Fields_From_Blurry_Images_CVPR_2022_paper.pdf)|
|2022|CVPR||[NAN: Noise-Aware NeRFs for Burst-Denoising](https://openaccess.thecvf.com/content/CVPR2022/papers/Pearl_NAN_Noise-Aware_NeRFs_for_Burst-Denoising_CVPR_2022_paper.pdf)|[Project Page](https://noise-aware-nerf.github.io/)|
|2022|CVPR||[NeRF in the Dark: High Dynamic Range View Synthesis from Noisy Raw Images](https://openaccess.thecvf.com/content/CVPR2022/papers/Mildenhall_NeRF_in_the_Dark_High_Dynamic_Range_View_Synthesis_From_CVPR_2022_paper.pdf)|

#### Depth Estimation

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[AR-NeRF: Unsupervised Learning of Depth and Defocus Effects from Natural Images with Aperture Rendering Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Kaneko_AR-NeRF_Unsupervised_Learning_of_Depth_and_Defocus_Effects_From_Natural_CVPR_2022_paper.pdf)|[Project Page](https://www.kecl.ntt.co.jp/people/kaneko.takuhiro/projects/ar-nerf/)|
|2021|ICCV|[Torch](https://github.com/weiyithu/NerfingMVS)|[NerfingMVS: Guided Optimization of Neural Radiance Fields for Indoor Multi-view Stereo](https://openaccess.thecvf.com/content/ICCV2021/papers/Wei_NerfingMVS_Guided_Optimization_of_Neural_Radiance_Fields_for_Indoor_Multi-View_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/vincentfung13/MINE)|[MINE: Towards Continuous Depth MPI with NeRF for Novel View Synthesis](https://openaccess.thecvf.com/content/ICCV2021/papers/Li_MINE_Towards_Continuous_Depth_MPI_With_NeRF_for_Novel_View_ICCV_2021_paper.pdf)|

#### Editing

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Torch](https://github.com/lwwu2/diver-rt)|[DIVeR: Real-time and Accurate Neural Radiance Fields with Deterministic Integration for Volume Rendering](https://openaccess.thecvf.com/content/CVPR2022/papers/Wu_DIVeR_Real-Time_and_Accurate_Neural_Radiance_Fields_With_Deterministic_Integration_CVPR_2022_paper.pdf)|
|2022|CVPR|[Jittor](https://github.com/IGLICT/NeRF-Editing)|[NeRF-Editing: Geometry Editing of Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Yuan_NeRF-Editing_Geometry_Editing_of_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/MrTornado24/FENeRF)|[FENeRF: Face Editing in Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Sun_FENeRF_Face_Editing_in_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR||[RigNeRF: Fully Controllable Neural 3D Portraits](https://openaccess.thecvf.com/content/CVPR2022/papers/Athar_RigNeRF_Fully_Controllable_Neural_3D_Portraits_CVPR_2022_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/zju3dv/object_nerf)|[Learning Object-Compositional Neural Radiance Field for Editable Scene Rendering](https://openaccess.thecvf.com/content/ICCV2021/papers/Yang_Learning_Object-Compositional_Neural_Radiance_Field_for_Editable_Scene_Rendering_ICCV_2021_paper.pdf)|[Project Page](https://zju3dv.github.io/object_nerf/)|
|2021|CVPR|[Torch](https://github.com/autonomousvision/giraffe)|[GIRAFFE: Representing Scenes as Compositional Generative Neural Feature Fields](https://openaccess.thecvf.com/content/CVPR2021/papers/Niemeyer_GIRAFFE_Representing_Scenes_As_Compositional_Generative_Neural_Feature_Fields_CVPR_2021_paper.pdf)||
|2020|NIPS|[Torch](https://github.com/autonomousvision/graf)|[GRAF: Generative Radiance Fields for 3D-Aware Image Synthesis](https://proceedings.neurips.cc/paper/2020/file/e92e1b476bb5262d793fd40931e0ed53-Paper.pdf)||

#### Face

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[LOLNeRF: Learn from One Look](https://openaccess.thecvf.com/content/CVPR2022/papers/Rebain_LOLNerf_Learn_From_One_Look_CVPR_2022_paper.pdf)|[Project Page](https://ubc-vision.github.io/lolnerf/)|
|2022|CVPR|[Torch](https://github.com/MrTornado24/FENeRF)|[FENeRF: Face Editing in Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Sun_FENeRF_Face_Editing_in_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR||[CoNeRF: Controllable Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Kania_CoNeRF_Controllable_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/CrisHY1995/headnerf)|[HeadNeRF: A Real-time NeRF-based Parametric Head Model](https://openaccess.thecvf.com/content/CVPR2022/papers/Hong_HeadNeRF_A_Real-Time_NeRF-Based_Parametric_Head_Model_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/primecai/Pix2NeRF)|[Pix2NeRF: Unsupervised Conditional π-GAN for Single Image to NeuralRadiance Fields Translation](https://openaccess.thecvf.com/content/CVPR2022/papers/Cai_Pix2NeRF_Unsupervised_Conditional_p-GAN_for_Single_Image_to_Neural_Radiance_CVPR_2022_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/YudongGuo/AD-NeRF)|[AD-NeRF: Audio Driven Neural Radiance Fields for Talking Head Synthesis](https://openaccess.thecvf.com/content/ICCV2021/papers/Guo_AD-NeRF_Audio_Driven_Neural_Radiance_Fields_for_Talking_Head_Synthesis_ICCV_2021_paper.pdf)|
|2021|CVPR||[Dynamic Neural Radiance Fields for Monocular 4D Facial Avatar Reconstruction](https://openaccess.thecvf.com/content/CVPR2021/papers/Gafni_Dynamic_Neural_Radiance_Fields_for_Monocular_4D_Facial_Avatar_Reconstruction_CVPR_2021_paper.pdf)|[Project Page](https://gafniguy.github.io/4D-Facial-Avatars/)|

#### High Dynamic Range (HDR)

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[HDR-NeRF: High Dynamic Range Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Huang_HDR-NeRF_High_Dynamic_Range_Neural_Radiance_Fields_CVPR_2022_paper.pdf)|

#### Human

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|ECCV|[code](https://github.com/apple/ml-neuman)|[NeuMan: Neural Human Radiance Field from a Single Video](https://arxiv.org/abs/2203.12575)||
|2022|CVPR||[Structured Local Radiance Fields for Human Avatar Modeling](https://openaccess.thecvf.com/content/CVPR2022/papers/Zheng_Structured_Local_Radiance_Fields_for_Human_Avatar_Modeling_CVPR_2022_paper.pdf)|
|2022|CVPR|[Code](https://github.com/pfnet-research/surface-aligned-nerf)|[Surface-Aligned Neural Radiance Fields for Controllable 3D Human Synthesis](https://openaccess.thecvf.com/content/CVPR2022/papers/Xu_Surface-Aligned_Neural_Radiance_Fields_for_Controllable_3D_Human_Synthesis_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/chungyiweng/humannerf)|[HumanNeRF: Free-viewpoint Rendering of Moving People from Monocular Video](https://openaccess.thecvf.com/content/CVPR2022/papers/Weng_HumanNeRF_Free-Viewpoint_Rendering_of_Moving_People_From_Monocular_Video_CVPR_2022_paper.pdf)|
|2022|CVPR||[DoubleField: Bridging the Neural Surface and Radiance Fields for High-fidelity Human Reconstruction and Rendering](https://openaccess.thecvf.com/content/CVPR2022/papers/Shao_DoubleField_Bridging_the_Neural_Surface_and_Radiance_Fields_for_High-Fidelity_CVPR_2022_paper.pdf)|
|2021|ICCV|[Code](https://github.com/zju3dv/animatable_nerf)|[Animatable Neural Radiance Fields for Modeling Dynamic Human Bodies](https://openaccess.thecvf.com/content/ICCV2021/papers/Peng_Animatable_Neural_Radiance_Fields_for_Modeling_Dynamic_Human_Bodies_ICCV_2021_paper.pdf)|[Project Page](https://zju3dv.github.io/animatable_nerf/)|
|2021|ICCV|[Torch](https://github.com/nogu-atsu/NARF)|[Neural Articulated Radiance Field](https://openaccess.thecvf.com/content/ICCV2021/papers/Noguchi_Neural_Articulated_Radiance_Field_ICCV_2021_paper.pdf)|

#### Large Scale Scene

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[Urban Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Rematas_Urban_Radiance_Fields_CVPR_2022_paper.pdf)|
|2022|CVPR|[Code](https://github.com/jetd1/NeRFusion)|[NeRFusion: Fusing Radiance Fields for Large-Scale Scene Reconstruction](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhang_NeRFusion_Fusing_Radiance_Fields_for_Large-Scale_Scene_Reconstruction_CVPR_2022_paper.pdf)|
|2022|CVPR||[Mega-NeRF: Scalable Construction of Large-Scale NeRFs for Virtual Fly-Throughs](https://openaccess.thecvf.com/content/CVPR2022/papers/Turki_Mega-NERF_Scalable_Construction_of_Large-Scale_NeRFs_for_Virtual_Fly-Throughs_CVPR_2022_paper.pdf)|
|2022|CVPR||[Block-NeRF: Scalable Large Scene Neural View Synthesis](https://openaccess.thecvf.com/content/CVPR2022/papers/Tancik_Block-NeRF_Scalable_Large_Scene_Neural_View_Synthesis_CVPR_2022_paper.pdf)|
|2022|CVPR|[Torch](https://github.com/rover-xingyu/Ha-NeRF)|[Hallucinated Neural Radiance Fields in the Wild](https://openaccess.thecvf.com/content/CVPR2022/papers/Chen_Hallucinated_Neural_Radiance_Fields_in_the_Wild_CVPR_2022_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/apple/ml-gsn)|[Unconstrained Scene Generation with Locally Conditioned Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/DeVries_Unconstrained_Scene_Generation_With_Locally_Conditioned_Radiance_Fields_ICCV_2021_paper.pdf)|[Project Page](https://apple.github.io/ml-gsn/)|
|2021|CVPR||[NeRF in the Wild: Neural Radiance Fields for Unconstrained Photo Collections](https://openaccess.thecvf.com/content/CVPR2021/papers/Martin-Brualla_NeRF_in_the_Wild_Neural_Radiance_Fields_for_Unconstrained_Photo_CVPR_2021_paper.pdf)|[Project Page](https://nerf-w.github.io/)|

#### Pose Misalignment

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2021|ICCV||[BARF: Bundle-Adjusting Neural Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/Lin_BARF_Bundle-Adjusting_Neural_Radiance_Fields_ICCV_2021_paper.pdf)|[Project Page](https://chenhsuanlin.bitbucket.io/bundle-adjusting-NeRF/)|

#### Stylized

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Jittor](https://github.com/IGLICT/StylizedNeRF)|[StylizedNeRF: Consistent 3D Scene Stylization as Stylized NeRF via 2D-3D Mutual Learning](https://openaccess.thecvf.com/content/CVPR2022/papers/Huang_StylizedNeRF_Consistent_3D_Scene_Stylization_As_Stylized_NeRF_via_2D-3D_CVPR_2022_paper.pdf)|

#### Surface Reconstruction

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2021|ICCV|[Torch](https://github.com/autonomousvision/unisurf)|[UNISURF: Unifying Neural Implicit Surfaces and Radiance Fields for Multi-View Reconstruction](https://openaccess.thecvf.com/content/ICCV2021/papers/Oechsle_UNISURF_Unifying_Neural_Implicit_Surfaces_and_Radiance_Fields_for_Multi-View_ICCV_2021_paper.pdf)|

#### Text & Image Guided Generation

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR|[Code](https://github.com/cassiePython/CLIPNeRF)|[CLIP-NeRF: Text-and-Image Driven Manipulation of Neural Radiance Fields](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_CLIP-NeRF_Text-and-Image_Driven_Manipulation_of_Neural_Radiance_Fields_CVPR_2022_paper.pdf)||

#### Video

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|ECCV|[code](https://github.com/apple/ml-neuman)|[NeuMan: Neural Human Radiance Field from a Single Video](https://arxiv.org/abs/2203.12575)||
|2021|CVPR|[Torch](https://github.com/albertpumarola/D-NeRF)|[D-NeRF: Neural Radiance Fields for Dynamic Scenes](https://openaccess.thecvf.com/content/CVPR2021/papers/Pumarola_D-NeRF_Neural_Radiance_Fields_for_Dynamic_Scenes_CVPR_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/facebookresearch/nonrigid_nerf)|[Non-Rigid Neural Radiance Fields: Reconstruction and Novel View Synthesis of a Dynamic Scene From Monocular Video](https://openaccess.thecvf.com/content/ICCV2021/papers/Tretschk_Non-Rigid_Neural_Radiance_Fields_Reconstruction_and_Novel_View_Synthesis_of_ICCV_2021_paper.pdf)|
|2021|CVPR||[Dynamic Neural Radiance Fields for Monocular 4D Facial Avatar Reconstruction](https://openaccess.thecvf.com/content/CVPR2021/papers/Gafni_Dynamic_Neural_Radiance_Fields_for_Monocular_4D_Facial_Avatar_Reconstruction_CVPR_2021_paper.pdf)|[Project Page](https://gafniguy.github.io/4D-Facial-Avatars/)|
|2021|CVPR||[Learning Compositional Radiance Fields of Dynamic Human Heads](https://openaccess.thecvf.com/content/CVPR2021/papers/Wang_Learning_Compositional_Radiance_Fields_of_Dynamic_Human_Heads_CVPR_2021_paper.pdf)|[Project Page](https://ziyanw1.github.io/hybrid_nerf/)|


#### View Synthesis Extrapolation

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2022|CVPR||[Ray Priors through Reprojection: Improving Neural Radiance Fields for Novel View Extrapolation](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhang_Ray_Priors_Through_Reprojection_Improving_Neural_Radiance_Fields_for_Novel_CVPR_2022_paper.pdf)||

### Unclassified

|Year|Conf/Jour|Code|Title|OtherInfo|
|:-:|:-:|:-:|:-:|:-:|
|2021|ICCV|[Torch](https://github.com/wbjang/code-nerf)|[CodeNeRF: Disentangled Neural Radiance Fields for Object Categories](https://openaccess.thecvf.com/content/ICCV2021/papers/Jang_CodeNeRF_Disentangled_Neural_Radiance_Fields_for_Object_Categories_ICCV_2021_paper.pdf)|
|2021|ICCV|[Torch](https://github.com/POSTECH-CVLab/SCNeRF)|[Self-Calibrating Neural Radiance Fields](https://openaccess.thecvf.com/content/ICCV2021/papers/Jeong_Self-Calibrating_Neural_Radiance_Fields_ICCV_2021_paper.pdf)| 

## Datasets

|Year|Name|Task|Instances|
|:-:|:-:|:-:|:-:|

## Talks & Videos

|Year|Theme|Speaker/Publisher|Language|
|:-:|:-:|:-:|:-:|

## Blogs

|Year|Title|Writer|Language|
|:-:|:-:|:-:|:-:|
|2022|[NeRF及其发展](https://zhuanlan.zhihu.com/p/512538748)|yuqiSun|CN|
|2022|[NeRF at CVPR 2022](https://dellaert.github.io/NeRF22/)|Frank Dellaert|EN|
|2021|[NeRF at ICCV 2021](https://dellaert.github.io/NeRF21/)|Frank Dellaert|EN|
|2020|[NeRF Explosion 2020](https://dellaert.github.io/NeRF/)|Frank Dellaert|EN|

## Acknowledgment
When we reviewed the literatures about NeRF, we found that this excellent [repo](https://github.com/yenchenlin/awesome-NeRF) had not been updated for a long time, so we reorganized and released our [awesome-NeRF](https://github.com/koolo233/awesome-NeRF). Some features were borrowed from [repo](https://github.com/yenchenlin/awesome-NeRF), so we are grateful for their works.

## Team
### Team Members
[Zhongwei Qiu](https://github.com/qiuzhongwei-USTB) (Leader), [Zijiang Yang](https://github.com/koolo233), [Tianle Cheng](https://github.com/Oak112)
### Contributors


