# AIME 2020

This repository relates to section `3.2` in our paper:

*HYPE: Predicting Blood Pressure from Photoplethysmograms in a Hypertensive Population*

[Paper] (https://link.springer.com/chapter/10.1007/978-3-030-59137-3_29)

Best Student Paper at the [AIME 2020](http://aime20.aimedicine.info/) conference.

For the code related to secion `3.3` please refer to this repository: [PPG-to-BP-Prediction-convnets](https://github.com/suparno89/PPG-to-BP-Prediction-convnets)

----
For running the notebooks:

```
pipenv install
pipenv shell
pipenv run jupyter notebook
```

The notebooks process raw PPG data and predict blood pressure for 2 different datasets:

`HYPE`: extract_features_and_predict_bp_from_ppg_hype.ipynb

`EVAL`: extract_features_and_predict_bp_from_ppg_eval.ipynb

# Datasets Information

**EVAL**: https://www.kaggle.com/mkachuee/noninvasivebp (original)

However, we processed it and used the following file as the input to our notebook: https://doi.org/10.6084/m9.figshare.12649691


**HYPE**: Interested? Please fill the following form: https://forms.gle/M8DDtuMeWGfT3k4y5

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
