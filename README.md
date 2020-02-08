# Don't-call-me-turkey-
Find the turkey in the sound bite

# Data Description
In this competition you are tasked with finding the turkey sound signature from pre-extracted audio features. A simple binary problem, or is it? What does a turkey really sound like? How many sounds are similar? Will you be able to find the turkey or will you go a-fowl?

# File Description
This dataset is based on AudioSet’s data available here https://research.google.com/audioset/. It contains video IDs and time bounds for youtube clips, as well as 128-dimensional audio-based features created with VGGish based on these clips. You must predict if the sound clip from which audio_embedding originates contains a turkey sound.

AudioSet's dataset is under a Creative Commons Attribution 4.0 International (CC BY 4.0) license, while their ontology is under a Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license. Our data includes data from both, modified to fit a competition format.

train.json - the training set

test.json - the test set

sample_submission.csv - a sample submission file in the correct format

# Data Description
vid_id - YouTube video ID associated with this sample.
start_time_seconds_youtube_clip - Where in the YouTube video this audio feature starts.

end_time_seconds_youtube_clip - Where in the YouTube video this audio feature ends.

audio_embedding - Extracted frame-level audio feature, embedded down to 128 dimensions per frame using AudioSet’s VGGish tools available here: https://github.com/tensorflow/models/tree/master/research/audioset

is_turkey - The target: whether or not the original audio clip contained a turkey. Label is a soft label, based on whether or not AudioSet’s ontology labeled this clip with “Turkey”, and may count turkey calls and other related content as being “turkey”. is_turkey is 1 if the clip contains a turkey sound, and 0 if it does not.

# Evaluation Metric
Submissions are evaluated on AUC-ROC score between the predicted classes and the observed targets.

# LB Sore = 0.955

