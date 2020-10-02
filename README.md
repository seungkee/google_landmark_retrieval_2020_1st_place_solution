# google_landmark_retrieval_1st_place_solution

This is the 1st place solution code for google landmark retrieval 2020.

Competition link (https://www.kaggle.com/c/landmark-retrieval-2020)

Kaggle Discussion post link (https://www.kaggle.com/c/landmark-retrieval-2020/discussion/176037) 

Detailed solution description arxiv link (https://arxiv.org/ftp/arxiv/papers/2009/2009.05132.pdf)

HARDWARE ENVIRONMENT : Colab TPUs

DATA : Google Landmarks Dataset v2(https://github.com/cvdfoundation/google-landmark). TF Records was used for faster training.

TRAINING(./notebooks)
1. Run 'v2clean_train.ipynb' until validation loss converge.
   Congifuration: IMAGE_SIZE=[512,512], EFF_VER=7, BATCH_SIZE=8*8=64
2. Take efficientnet backbone from step 2, and run 'v2total_train.ipynb' until validation loss converge.
   Configuration : NOT_CLEAN_WEIGHT=1.0, IMAGE_SIZE=[512,512],EFF_VER=7, BATCHSIZE=8*8=64
3. Run 'v2total_train.ipynb' again, with larger image sizes.([640,640], [736,736])
4. Run 'v2total_train.ipynb' again, with NOT_CLEAN_WEIGHT = 0.5
