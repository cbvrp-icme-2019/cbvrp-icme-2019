# Content-based Video Relevance Prediction Challenge
### @ICME 2019, Shanghai, China

(This challenge is fully sponsored by Hulu.)

Video relevance computation is one of the most important tasks for personalized online streaming service. Given the relevance of videos and viewer feedbacks, the system can provide personalized recommendations, which will help the viewer discover more content of interest. In most online service, the computation of video relevance table is based on the viewers' implicit feedback, e.g. watch and search history. The system analyzes the viewer-to-video preference and computes the video-to-video relevance scores using collaborative filtering based methods. However, this kind of method performs poorly for “cold-start” problem - when a new video is added to the library, the recommendation system needs to bootstrap the video relevance score with very little historical viewer feedbacks. One promising approach to solve “cold-start” is analyzing video content itself to predict the relevance score, i.e. predicting the video-to-video relevance by analyzing the keyframes, audio, subtitles and metadata. With the relevance score, we can provide better recommendations for our viewers. The main task of this challenge is to solve the “cord-start” problem. According to the viewer behavior history and the video content, the participants need to predict the viewer click-through behavior on new TV-shows or new movies. The viewer feedbacks have been cleaned to avoid any privacy issues. Instead of delivering original video content, audio and visual features are extracted from the video and delivered as the representation of the video content. Specifically, there are two separated tracks for TV-shows and movies respectively.

## Task and Data

The data is composed of two parts. One part is viewer records, i.e. a data sample is a viewer record. For example, a record “MovieA, MovieB, MovieC -> MovieD” means a viewer has watched three movies A, B, C and then we recommend movie D to the viewer. If the viewer clicked the movie D, we consider this record as a positive sample, otherwise it is a negative sample. The other one is visual and audio features extracted from the TV-show/movie trailers. The features are extracted using CNN in a format of 2048 dimensional vectors of floats. For each track, there are respectively a training set, a validation set and a test set. In the test set, we will give a bunch of viewer records. The participants need to calculate a probability score indicating how much probably the viewer will click. The ground-truth for training set and validation set will be released to participants after registration. The details of the dataset are given as follows.

#### Track 1: TV-series

Pre-extracted features derived from nearly 3,570 TV-series video trailers. The whole set is divided into 3 subsets: training set, validation set, and testing set.

|           |  TV-series |   Records   |
| --------- |:---------: |:-----------:|
|   Train   |   2,839    |  5,221,221  |
|   Val     |    357     |   931,820   |
|   Test    |    374     |   794,120   |


#### Track 2: Movies

Pre-extracted features derived from over 9,574 movie video trailers. The whole set is divided into 3 subsets: training set, validation set, and testing set.

|           |   Movie   |   Records   |
| --------- |:---------:|:-----------:|
|   Train   |   7,303   |  1,123,786  |
|   Val     |   1,254   |   552,577   |
|   Test    |   1,017   |   822,343   |

For training set and validation set in both tracks, we also provide the ground truth (relevance lists) derived from implicit viewer feedbacks. The viewer feedbacks have been cleaned to avoid any privacy issues.

AUC (Area Under Curve) will be used as evaluation metric.


## Registration

To register for the challenge and get access to the dataset, please complete the [Online Agreement Form](https://freeonlinesurveys.com/s/lDBaYlvA). We will send you the download instructions by email after the challenge data available date (Jan 1, 2019).

## Submission

The participants should prepare a csv file for testing set (please refer to provided evaluation example to see the format of the submission file) and send the csv file to cbvrp-icme-2019@hulu.com. After receiving the submission csv file, we will evaluate the results and send back to the participants by email no later than July 1st.

## Schedule

|        Date       |                  Event               |
| ----------------- |:------------------------------------:|
|   Dec 15, 2018    | Registration open                    |
|   Jan 1, 2019     | Release train and validation data    | 
|   Feb 15, 2019    | Release test data                    |
|   Mar 15, 2019    | Deadline for result submission       |
|   Apr 1, 2019     | Notification of winners              |
|   Apr 8, 2019     | Deadline for paper submission        |
|   Apr 22, 2019    | Notification of paper acceptance     |
|   Apr 29, 2019    | Deadline for camera-ready papers     |


## Organizers

Peng Wang (peng.wang@hulu.com) Hulu LLC.\
Yan Bai (ryann.bai@hulu.com) Hulu LLC.\
Chunxu Xu (chunxu.xu@hulu.com) Hulu LLC.\
Saboya Yang (saboya.yang@hulu.com) Hulu LLC.\
Wei Feng (wei.feng@hulu.com) Hulu LLC.\
Xiaohui Xie (xiaohui.xie@hulu.com) Hulu LLC.
