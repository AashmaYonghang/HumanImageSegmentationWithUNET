# HumanImageSegmentationWithUNET

Image segmentation is used if we want to know the shape of objects. It is basically a classification problem where we need to assign a class to each pixel of the image.

In this project, each pixel is classified as human or background. Datasets are augmented using 
Albumentation library.
>Note: Unlike augmentation for classification datasets where only input images are augmented and label remains intact. In segmentation problem, same augmentation has to be applied to both input images and output labelling images.

Segmentation model used is U-Net which is given by segmentation_models_pytorch (smp) library. No activation is set for the model. The output logits along with mask(segmented output image) are used to calculate  nn.BCEWithLogitsLoss()
and DiceLoss(supported by smp library).
















