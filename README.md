## 1. 3D Deep Learning on Medical Images: A Review
[Singh et al., Machine Learning for Biomedical Imaging and Sensing 2020](https://www.mdpi.com/1424-8220/20/18/5097)
*Why chose this one? - The only review paper  focusing on medical and 3d imaging in last 4 years*

This paper focus on the important related works of medical image segmentation using 3D CNN.

3D UNet:

1. [Chen et al., BRATS 2018 good result](https://link.springer.com/chapter/10.1007/978-3-030-11726-9_32)
BRATS 2018, 0.893(WT), 0.830(TC), 0.742(EC)
2. [Kayalibay et al., 2017](https://arxiv.org/abs/1701.03056)
Data BRATS 2015, 0.850 (WT), 0.872(TC), 0.610(EC)
good for Jaccard loss function
disadvantages:computationally expensive
3. [Isensee et al., 2017](https://link.springer.com/chapter/10.1007/978-3-319-75238-9_25)
BRATS 2017, 0.850(WT), 0.740(TC), 0.640(EC)
4. [Peng et al., 2019](https://onlinelibrary.wiley.com/doi/full/10.1002/ima.22368?casa_token=hQggptWMrigAAAAA%3AuUs-a_guqP__Wl5dx8mDvEMYe_VhrBvVhGD-PkpSpiowaU80cyzkCXoeAdPJM4VfYEEVdJnqwTqMj0A)
BRATS 2015, 0.850(WT), 0.720(TC), 0.610(EC)

Also it introduce what is 3D CNN, and 3D medical image preprocessing:
(1) artifact removal, (2) normalization, (3) slice timing correction (STC), (4) image registration and (5) bias field correction.
STC and image registration are very important in the case of 3D medical images (especially MR and CT images)

[note of details](./papers_note/1.md)

## 2. UNETR: Transformers for 3D Medical Image Segmentation

[Hatamizadeh et al., WACV 2022](https://openaccess.thecvf.com/content/WACV2022/html/Hatamizadeh_UNETR_Transformers_for_3D_Medical_Image_Segmentation_WACV_2022_paper.html)
*Why chose this one? - Influential work, generally not bad; New technique; Seems easy to reproduce*:
*This paper has been cited 400+ times since it was published in 2022 and uses the transformer technique, which has worked very well in these two years. And it has a lot of implementation, Github stars > 6,000*
[Implementation link](https://paperswithcode.com/paper/unetr-transformers-for-3d-medical-image)
This paper introduce a UNet combined Transformer method. It got the-state-of-art performance on Multi Atlas Labeling Beyond The Cranial Vault (BTCV) dataset and Medical Segmentation Decathlon (MSD) dataset.

### Motivation:
Troditional UNets performance in learning long-range dependencies is limited localized receptive fields. -- Transformer good at this one



### Main idea:
Encode by transformer
Decode by convolutional (not transformer reason: transformers are unable to properly capture localized information)
![Main idea](./figures/Mainidea.png)
[note of details](./papers_note/2.md)


## Next plan:
One person need work on troditional 3D UNet.
I would like to reproduce UNETR performance on lab. But due to bank holiday it will open on next Tuesday.

## 3 SAM
![Main idea](./figures/Mainidea.png)
