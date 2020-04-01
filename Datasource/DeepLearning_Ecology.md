FROM IMAGINECOLOGY https://gitlab.com/ecostat/imaginecology Vincent Miele, see 01 April 2020

# PAPERS
---

#### Generalities

[Christin et al, MEE 2019](papers/mee-christin2019_DL_in_ecology.pdf) Common questions about how and when to use deep learning.

[Weinstein et al, JAE 2018](papers/janeco-weinstein2018_computervision_for_ecology.pdf) Brief primer on ecological computer vision to outline its goals, tools and
applications to animal ecology.

[Waldchen, MEE 2018](papers/mee-waldchen2018_species_identification.pdf) A focus on deep learning neural networks as a technology that ena-
bled breakthroughs in automated species identification

[Brodick et al, TREE 2019](papers/tree-brodrick2019_CNN.pdf) A walkthrough of how to use CNN for ecological applications.

[Lamba et al, Curr.Biol.2019](papers/curbio-lambda2019_deeplearning_conservation.pdf) Current and future applications of supervised deep learning
in environmental conservation.

#### Camera traps

[Tabak et al, MEE 2018](papers/mee-tabak2018_cameratrap_tensorflow.pdf) ResNet-18 architecture and 3,367,383 images to automatically classify wildlife species from camera trap images obtained from five states across the United States. Datasets and R package available (see next sections). Updated version in [Tabak et al, biorxiv 2020](papers/biorxiv-tabak2020_MLWIC2.pdf)

[Norouzzadeh, PNAS 2018](papers/pnas-norouzzadeh2018_identif_count_animals.pdf) Alexnet, VGG, GoogLeNet, ResNet.
Identify, count, and describe the behaviors of 48 species in the 3.2 million-image Snapshot Serengeti dataset. Detect empty images + identify species + count animals.

[Beery et al, arxiv 2018](papers/arxiv-beery2018_terra_incognita_caltechcameratraps.pdf) Inception-v3 [56] model pretrained on ImageNet. Faster-RCNN model using two different backbones, ResNet-101 [58] and Inception-ResNet-v2. State-of-the-art algorithms show excellent performance when tested at the same location where they were trained. However,  generalization to new locations is poor.

[Schnieder et al, arxiv 2019](papers/arxiv-schneider2018_camera_trap.pdf) ResNet-101 architecture + Faster R-CNN outperforms YOLOv2.0 on camera trap images using the Reconyx Camera Trap and the Snapshot Serengeti data sets.

[Willi et al, MEE 2018](papers/mee-willi2018_identifying_species.pdf) ResNet-18 to identify species on four datasets (Table 1). Shows the differences of performance between training from scratch and transfer learning. (Fig 3,4)

[Gomez-Villa et al, Eco Info 2017](papers/ecoinfo-gomezvilla2017_CNN_Seregenti.pdf) Seregenti dataset analyzed with AlexNet, VGGNet, GoogLenet and ResNets.

[Chen et al, Eco Evol 2017](papers/ecoevo-chen2019_cameratrap_alexnet.pdf) AlexNet based. A dataset consisting of 8,368 images of wild and domestic animals in farm.

[Ahumada et al, Env. Conv. 2019](papers/envconv-ahumada2019_wildlifeinsights.pdf) Present Wildlife Insights, a platform that can process classification on your images automatically. Use pretrained Inception model, finetuned with 18 millions of images from partners and will be retrained when new data come in. Not available yet, data will be published with the platform. 

[Falzon et al, preprint 2019](papers/biorxiv-falzon2019_ClassifyMe_software.pdf) ClassifyMe is a software for automated animal detection on camera trap images. The user can download 5 different models trained on differents dataset and run the detection on its own machine. Use YoloV2 and won't allow re-train on own dataset. Not available yet. 

[Norouzzadeh, arXiv 2019](papers/arxiv-norouzzadeh2019_active_learning_camera_trap.pdf) Use active learning : after the training the model can access a bank of unlabeled images and ask to annotate some specific images for another training. It also uses Faster-R-CNN to find animals, the image are then cropped to remove the background and finally classified with ResNet-50.

[Schneider, Eco Evol 2020](papers/ecoevo-schneifer2020_camera_traps_guidelines.pdf) DenseNet201, Inception-ResNet-V3, InceptionV3, NASNetMobile, MobileNetV2,
and Xception. Parks Canada dataset containing 47,279 images collected from 36 locations with 55 animal species. Classifications **with <500 images had low  recall** +  classifying species **from untrained locations were less accurate**

[Sahinfar et al, Eco. Info. 2020](papers/ecoinfo-shahinfar2020_guideslines_nbimages.pdf), Discussion about high level of image similarity (reduce the CNN performance) and the number of images to achieve good performance (<300 image / class, poor performance). Data from Australia, Serengeti and Wisconsin.

#### Animal detection/classification

[Parham et al, Proc. 2018](papers/proc-parham2018_deeplearn_animal.pdf) A 5-component detection pipeline for use in a computer vision-based animal recognition system. Using YOLO.

[Villon et al, Eco. Info. 2018](papers/ecoinfo-villon2018_fish_identification.pdf) GoogLeNet architecture. Identification of fish species on underwater images. Try differents dataset for the training (with and without parts of fish, with and without the environment around fish). The average accuracy is the same for all datasets but there are difference between species. Also add decision rules after the training to improve performance. 

[Huang et al, Neurocomputing 2019](papers/neurocomputing-huang2019_fasterRCNN_marine.pdf) Tests the effect of 3 data-augmentation methods on underwater images: turbulence simulation, perspective transformation and illumination simulation. It improves the results more than standard data augmentation. 

[Milosevic et al, SciToEnv 2019](papers/scitotenv-milosevic2019_gradcam_larvae.pdf) Uses ResNet50 to classify 10 different species of larvae with very good accuracy. Also uses GradCam which reveals relevant informations of what is used by the model. 

#### Segmentation/Masking (i.e. detecting exact contours)

[Abrams et al, Ecoinfo 2019](papers/ecoinfo-abrams2019_canopy_habitatnet.pdf) Based on the U-Net. Segmenting habitat images of tropical rainforests.
Trained with 800 canopy images and 700 understory images.

[Brodick et al, TREE 2019](papers/tree-brodrick2019_CNN.pdf) Segmentation of coral reefs.

#### Face recognition / Re-Identification (Re-Id)

[Schofield et al, Sci. Adv. 2019](papers/sciadv-schofield2019_facerecognition_chimpanzee.pdf) Chimpanzee face recognition from videos in the wild using deep learning.
Annotation with [VIA software](http://www.robots.ox.ac.uk/~vgg/software/via/). Detection with SSD with VGG-16. 

[Hansen et al, Comp. Ind. 2018](papers/compind-hansen2018_pig-facerecognition-VGGface.pdf) Pig-face recognition with a VGG-face model and a home-made 6-layers CNN implemented in Keras, using data augmentation (image rotation). Grad-CAM (class-activated mapping)  shows what regions of an input image are activating the network for a given class.

[He et al, arxiv 2019](papers/arxiv-he2019_distinguishing_individual_red_pandas.pdf) Red pandas face recognitions in 3 steps : face detection with YoloV2, face alignement with U-Net and face identification with VGG-16. They used 2877 images of 51 pandas. 93% of top 1 ranking and 91% without face alignement. 

[Schneider et al, Mee 2019](papers/mee-schneider2019_pastpresentfuture_animal_identification.pdf) Summary of past approaches for re-ID (re-identify an individual animal upon re-encounter). Presents different deep learning methods to do it : CNN and Siamese Network, as well as different metrics : verification, close-set and open-set identification. Gives recommendations to make a dataset for re-ID.

[Bogucki et al, Cons. Bio. 2019](papers/convsbio-bogucki2019_whale_re_id.pdf) A 3-CNN pipeline for whale Re-ID : a first CNN to find and crop the head of the whale, a second CNN to find 2 keypoints, used to orient the head and re-crop more precisely, and a third CNN to classify and identify the whale.

[Ferreira et al, biorxiv 2019](papers/biorvix-ferreira2019_re_id_small_birds.pdf) Re-Id on 3 small birds species (10,10 and 30 individuals). Masks of birds are extracted with Mask-RCNN and then classified with VGG-19 to predict identity . 800+ pictures/individual are used for VGG19 training. They use data augmentation and also add blur/noise to be closer to the test set. Achieves around 90% accuracy for the 3 species but doesn't work well with new birds.

[Körschens et al, arxiv 2018](papers/arxiv-korschens2018_elephant_reid.pdf) Automatic Identification of Elephants. Yolo is used to crop the head. ResNet50 was modified to extract features not from the last layer before the classification layer, but from earlier activation layers + PCA to reduce dimension + SVM to classify.

[Moskvya et al, arxiv 2019](papers/arxiv-moskvyak2019_reid_raymanta.pdf) Re-id of manta rays. The network is optimized using the **semi-hard triplet loss** function, dapting FaceNet. The distance between the learned embedding points provides a dissimilarity measure. 

[Bouma et al, arxiv 2019](papers/arxiv-bouma2019_dolphin_embedding.pdf) Dolphin identification using **batch-hard triplet loss** function. Imbalanced dataset containing 3544 images of 185 individuals. Based on ResNet-50, with an output layer of size 128. 

[Schnieder et al, arxiv 2019](papers/arxiv-schneider2019_siamese_reid.pdf) Re-id of humans, chimpanzees, whales, fruit flies, and octopus. Five **siamese** similarity comparison networks based on the AlexNet, VGG-19,DenseNet201, MobileNetV2, and InceptionV3. 

#### Counting

[Torney et al, MEE 2019](papers/mee-torney2019_wildbeest_count_yolo.pdf) Count wildbeest on aerial images. Each photo is divided into 40 864*864 sub-images for training. Modify slightly Yolov3 architecture to adapt to their problem : less anchors, different shape of anchor boxes, only one scale (instead of 3, object are always at the same distance), change loss function to reduce false positives. Give very high accuracy (similar to expert labels) and speed. 

[Gray et al, MEE 2018](papers/mee-gray2018_sea_turtle_count.pdf) Counting sea turtles on drone images. Relatively small dataset : 467 photos, but each one is divided in 2800 100*100 sub-image for the CNN input. CNN of modest size : 4 convolutions + 2 dense layers. The model finds 9% more turtle than there really are.

[Guirado et al, Sci.Rep 2019](papers/scirep-guirado2019_whale_count.pdf) Whale counting in satellite and aerial images. GoogleNet Inception v3 + Faster R-CNN, a two-step CNN-based approach capable of counting whales in vast areas with a reduced computational cost, where the first CNN is used to filter out water potential false positives (ships,foam and rocks) but keeping candidate images to be analyzed later by the second and much slower CNN. 

[Guirado et al, Remote Sensing 2020 ](papers/remotesensing-guirado2020_tree_cover_CNN.pdf) Estimating tree cover with a Inception v3 CNN. Images from Google Maps corresponding to the FAO’s GDA 0.5 ha forest and non-forest plots + the Northwestern
Polytechnical University NWPU-RESISC45 dataset [48], a set of publicly available reference
orthoimages for the classification of remotely sensed images. 

#### Pose and shape 
[Zuffi et al, ICCV 2019](papers/papers/arxiv-zuffi2019_zebra_pose.pdf) Neural network to predict 3D pose, shape and texture of zebras. 


#### Model interpretation

[Miao et al, Scientific reports](papers/scirep-miao2019_interpretation_model_camera_trap.pdf)
Use several methods to understand and interpret the weights after training. The model is VGG16 (and ResNet50), trained on 111 000 camera trap images with 20 species of Gorongosa National Park. They use GG-CAM, GBP, Grad-CAM to extract localized visual features of single images,  Mutual Information (MI)  to generalize within-species features and hierarchical clustering to inspect the visual similarities between species. 

<a name="codes"></a>
# CODES
---
NOTA BENE: Tutorials on a subset of the following codes are available in [another section.](projects/) 

#### General purpose object detection

(for an introduction about this section, see [this page](https://towardsdatascience.com/r-cnn-fast-r-cnn-faster-r-cnn-yolo-object-detection-algorithms-36d53571365e))

[YOLO](https://github.com/AlexeyAB/darknet) In YOLO a single convolutional network predicts the bounding boxes and the class probabilities for these boxes. Widely used, in particular with animals as "object" to detect. [arXiv preprint](papers/ieee-redmon2016_yolo.pdf)

> Tutorial by @vm-lbbe and @Gasp34 [available here](projects/giraffechestWithYolo).

[Mask-R-CNN](https://github.com/matterport/Mask_RCNN) The model generates bounding boxes and segmentation masks (a *mask* is the exact contours of an objects) of objects in the image. The mask detection requires a training on annotated images with the contours of all objects (animals for instance). [arXiv preprint](papers/arxiv-he2018_mask-R-CNN.pdf)

> Tutorial by @vm-lbbe and @Gasp34 [available here](projects/giraffechestWithMaskRCNN).

[RetinaNet](https://github.com/fizyr/keras-retinanet) New loss called Focal Loss to correct the problem of imbalance between foreground and background classes. [arXiv preprint](papers/arxiv-lin2018_focal_loss.pdf)

>Tutorial by @vm-lbbe and @Gasp34 [available here](projects/cameraTrapDetectionWithRetinanet).

#### Camera traps

[Camera Trap Classifier](https://github.com/marco-willi/camera-trap-classifier) This repository contains code and documentation to train and apply CNN for identifying animal species in photographs from camera traps. Code in Python and based on Tensorflow.
> Tutorial  by @vm-lbbe and @Gasp34 [available here](projects/classificationWithCameraTrapClassifier).

[Microsoft codes](https://www.microsoft.com/en-us/research/project/accelerating-image-based-biodiversity-surveys/) including a too dedicated to camera traps with [Megadetector](https://github.com/microsoft/CameraTraps)
One-class animal detector (i.e. detects any animal but does not classify) trained on several hundred thousand bounding boxes from a variety of ecosystems.

> Tutorial by @vm-lbbe and @Gasp34 [available here](projects/detectionWithMegaDetector).

[MLWIC2: Machine Learning for Wildlife Image Classification in R](https://github.com/mikeyEcology/MLWIC2)
This package identifies animal species in camera trap images by implementing the model described in [Tabak et al, MEE 2018](papers/mee-tabak2018_cameratrap_tensorflow.pdf) and updated in [Tabak et al,biorxiv 2020](papers/biorxiv-tabak2020_MLWIC2.pdf) Linux, Mac, (Windows)



[DLCTI](https://github.com/Evolving-AI-Lab/deep_learning_for_camera_trap_images)
Along with [Norouzzadeh, PNAS 2018](papers/pnas-norouzzadeh2018_identif_count_animals.pdf)
> Deprecated

[Animal Scanner]() Software for classifying humans, animals, and empty frames in camera trap images.
Along with [Yousif et al, Eco Evo 2019](papers/ecoevo-yousif2019_animalscanner_software.pdf)
> Deprecated

#### Face recognition
[face_recognition](https://github.com/ageitgey/face_recognition)
Recognize and manipulate faces from Python.

#### Unsupervised clustering
[DeepCluster](https://github.com/facebookresearch/deepcluster)
Clustering for Unsupervised Learning of Visual Features.

#### Model interpretation
[tf-explain](https://github.com/sicara/tf-explain)
Interpretability methods as Tensorflow 2.0 callbacks to ease neural network's understanding.

 <a name="datasets"></a>
# DATASETS
---

#### [The penguin dataset](https://www.robots.ox.ac.uk/~vgg/data/penguins/)
- X images (28GB), 40 different locations
- Annotations : X-Y coordinates on each penguin (json or MAT)

#### [Oregon Wildlife image collection](https://www.kaggle.com/virtualdvid/oregon-wildlife)
- 14013 images, 20 species, (4,36 GB)
- Annotations : name of the class (images sorted by folder)
- 5 classes already preprocessed with GapCV (?)

#### [Caltech camera Trap dataset](https://beerys.github.io/CaltechCameraTraps/)
- 243,187 (104 GB) images with class annotation 
- 57,864 images with bounding box annotation
- Annotations in [COCO format ](https://github.com/Microsoft/CameraTraps/blob/master/data_management/README.md#coco-cameratraps-format) (json)

#### [North American Camera Trap Images (NACTI)](http://lila.science/datasets/nacti)
- 3.7M images (1,3 TB)
- labels for 28 animal categories, primarily at the species level
- Annotations in [COCO format ](https://github.com/Microsoft/CameraTraps/blob/master/data_management/README.md#coco-cameratraps-format) (json)
- Along with [Tabak et al, MEE 2018](papers/mee-tabak2018_cameratrap_tensorflow.pdf)

#### [Snapshot Serengeti](http://lila.science/datasets/snapshot-serengeti)
- 6.7M images
- Labels for 55 animal categories, primarily at the species level
- 78 000 images with bounding box
- Annotations in [COCO format ](https://github.com/Microsoft/CameraTraps/blob/master/data_management/README.md#coco-cameratraps-format) (json)
- Along with [Swanson et al, Sci. Data 2015](papers/scidata-swanson2015_snapshot_serengeti.pdf)

#### [Wildlife Image and Localization Dataset (WILD)](http://lila.science/otherdatasets) 
- A new ground-truthed dataset for the tasks presented in this [paper](papers/proc-parham2018_deeplearn_animal.pdf), called WILD; WILD is comprised of photographs taken by biologists, wildlife rangers, citizen scientists [13], and conservationists.
- 5,784 images, 28 species (1,4 GB)
- Annotations : Bounding box in Pascal VOC format
- Link to download not working

#### [The Aerial Elephant Dataset](https://zenodo.org/record/3234780#.XX-ENaaxXmg)
- From this [paper]((http://openaccess.thecvf.com/content_CVPRW_2019/papers/DOAI/Naude_The_Aerial_Elephant_Dataset_A_New_Public_Benchmark_for_Aerial_CVPRW_2019_paper.pdf))
- 2101 images (16 GB) containing a total of 15 511 elephants. It is split into training and test subsets with 1649 images containing 12455 elephants in the training set and 452 images containing 3056 elephants in the test set.
- Annotations : ?

#### [iWildCam2019](https://www.kaggle.com/c/iwildcam-2019-fgvc6/overview) 
- Kaggle competition (finished) with data from CaltechCameraTraps, iNaturalist 2017/2018, and simulated data generated from Microsoft AirSim. 
- 196,157 images (43 GB) from 138 different locations in Southern California, 14 classes.
- Annotations : class (.csv)


#### [LILA](http://lila.science/datasets/)
- Many labeled camera trap dataset are hosted and available on this website. 
- Also look at [others](http://lila.science/otherdatasets) for more datasets.

#### [Reconyx Camera Trap](https://dataverse.scholarsportal.info/dataset.xhtml?persistentId=doi:10.5683/SP/TPB5ID)
- Used in [Schnieder et al, arxiv 2019](papers/arxiv-schneider2018_camera_trap.pdf)
- 7,193 camera trap images from two locations in Panama and the Netherlands, capturing colour images during the day, and gray-scale at night.
- Only a subset of 946 images include labeled bounding box coordinates

#### [FishNet](https://www.fishnet.ai/description)

* ~35K images taken from monitoring cameras on fishing boats
* 24 object classes (fish species and human)
* Annotations : bounding box in .csv format.

<a name="miscellaneous"></a>

# AND ALSO...
---

[Awesome Deep Ecology](https://github.com/patrickcgray/awesome-deep-ecology)
A curated list of deep learning resources for computer vision.

[Wildlife Insight](https://wildlifeinsights.org/about)
(non free) Wildlife Insights is combining field and sensor expertise, cutting edge technology and advanced analytics to enable people everywhere to share wildlife data and better manage wildlife populations. 

[A new wave of open-source tools for analysing animal behaviour and posture](https://www.nature.com/articles/d41586-019-02942-5)

[Deep learning for videos & action recognition](http://blog.qure.ai/notes/deep-learning-for-videos-action-recognition-review) 
