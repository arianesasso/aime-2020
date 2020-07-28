# AIME 2020

This repository relates to section `3.2` and `3.3` from our paper:

*HYPE: Predicting Blood Pressure from Photoplethysmograms in a Hypertensive Population*

At the moment in pre-print: [medRxiv](https://www.medrxiv.org/content/10.1101/2020.05.27.20107243v1).

Soon to be published by the [AIME 2020](http://aime20.aimedicine.info/) conference.

For running this notebooks, you will need to install previously the custom library: 

[Devicely](https://github.com/hpi-dhc/devicely), everything else should happen with:
```
pipenv install
pipenv shell
pipenv run jupyter notebook
```

The notebooks process raw PPG data and predicts blood pressure from 2 different datasets:

`HYPE`: extract_features_and_predict_bp_from_ppg_hype.ipynb

`EVAL`: extract_features_and_predict_bp_from_ppg_eval.ipynb

# Datasets Information

**EVAL**: https://www.kaggle.com/mkachuee/noninvasivebp (original)

However, we processed it and used the following file as the input to our notebook: https://doi.org/10.6084/m9.figshare.12649691


**HYPE**: awaiting for approval to share.

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
