# fixed-length-audios-dataset

- [fixed-length-audios-dataset](#fixed-length-audios-dataset)
  - [Description](#description)
  - [Content available](#content-available)
    - [How were the files manipulated?](#how-were-the-files-manipulated)

## Description

This project brings together sets of audios separated by folders, with uniform lengths.
Certain tasks are made easier when the length of the audios is uniform, reducing the variance that may exist in the results and conclusions.

## Content available

At the moment, there are only two sets of audios:

- `30_seconds` --> 1000 audios with a duration of 30 seconds;
- `2_minutes` --> 1000 audios lasting 2 minutes;

The audios were obtained and transformed using the following public datasets:

- `30_seconds` --> Corresponds to a sample of audios made available by the following dataset: `https://github.com/mdeff/fma?tab=readme-ov-file`
- `2_minutes` --> Corresponds to a sample of audios made available by the following dataset: `https://huggingface.co/datasets/MLCommons/unsupervised_peoples_speech`

Regarding the process of transforming the audios, the following was done:

- `30_seconds` --> Most of the audios were already 30 seconds long, so no changes were made to these. In the case of 29 second audios (it's the only different case, apart from 30 seconds length), `Comfort Noise` was added so that they had a fixed duration of 30 seconds;
- `2_minutes` --> Audios with a longer duration were cut so that their duration was fixed and equal to 2 minutes. For audios with a shorter duration, `Comfort Noise` was added.
- For all scenarios, the characteristics of the audio remained the same (e.g. `sample rate`).

### How were the files manipulated?

The file manipulation process was applied using a tool created for this purpose and available in this repo --> `https://github.com/bundasmanu/audio-length-equalizer`;
