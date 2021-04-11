# MileStone2 - Creating medeival portraits from modern pictures using GAN

## Status Report:

We decided to work on two separate notebooks, as we're developing two independent models, that are piped together (to see if it works, we've ran them both in the following sequence: 1. MileStone2_face_det  2. Milestone2_gan).
We could not upload the training files to github due to their size (and therefore the directory is not set properly in the repo either), so in order to replicate our work, the source files need to be downloaded from the following drive (and the directory structure should be set too) :
https://drive.google.com/drive/u/0/folders/1O9ZS7PPEc8SXzKDZ8U9kF87hU8xlFO3B

The directory is built as shown here:
  
    content/drive/MyDrive/work
      |-gan_output
      |-resource
          |-invalid_images.txt
          |-face_detection.zip
          |-painting.zip
          |-painting
          |-input
              |-train
              |-test
              |-val
          |-face_detector.xml 
          |-gan_input_images
The first part of the model works on the face_detection.zip data's dev set (this file is unzipped in the input folder) and exports it's output to the gan_input images folder.
The second part of the model works on the gan_input images, the painting folder (unzipped painting.zip) and the input folder, and exports it's output to the gan_output folder.

As a matter of honesty, we would like to disclaim, that we could not finish this submission in time (although the github link for the submisson has ben uploaded before midnight, we have finished the codes long after, as the task has proven to be difficult for us). We're aware that this makes the submission invalid, but we've still finished it, in case if it could still be reviewed.

## changes of plan since the first submission, and other notes to MileStone2:
  * The face detection is no longer going to be a trained model, we're using cv2-s pretrained face detector, which still needs to be fine tuned.
  * The first part of the model only operates on the test set of the model as it is proven to be enough for the GAN (we're planning to use this for evaluation only). (the rest of the data is used for training the GAN and the GAN only).
  * We are certain that the notebooks uploaded here would not work on a local machine without setting the environment properly. Therefore we uploaded them as the image of the google collab's notebooks we have worked on (so that the results of the cells can be seen as proof of success).
  * We've become aware that our data is not 100% clean for our task (too small images etc). We are planning to improve on that later on.
  * As mentioned above, we could not upload the whole data, but we've uploaded a small fraction of the results that we have achieved by running the models (so that our results can be seen in the submission).

