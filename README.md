# isic_melanoma_contest_task3_inception_v3

Disease classification model for ISIC 2018: Skin Lesion Analysis Towards Melanoma Detection – Task 3.

The original image set was modified as follows:

- added 155 AKIEC images and 223 DF images
- augmented the dataset by randomly rotating and zooming (80K total images)

Augmented images and images with identical legion identifiers* were NOT separated between training and validation sets. While this caused some data leakage, performance on the ISIC test data set was slightly better for this model compared to the best performing model trained with the augmented images separated between training and validation sets.

The model was trained for 2 epochs / 23 minutes on a GTA 1080ti GPU, resulting in the following performance:

					Loss	  Accuracy
			Training	0.0915	  0.9679
			Validation	0.0902	  0.9660

Model configuration and training details are shown on the attached Jupyter notebook.

The model achieved an average classification accuracy of 80% based on the ISIC contest validation data set of 193 images.

Final results for the ISIC 1,512 test images will be available when the contest concludes in early August 2018.

\* https://forum.isic-archive.com/t/task-3-supplemental-information/430
