# AIME 2020

This repository relates to section `3.2` in our paper:

**HYPE: Predicting Blood Pressure from Photoplethysmograms in a Hypertensive Population** [(Link)](https://link.springer.com/chapter/10.1007/978-3-030-59137-3_29)

Best student paper at the [AIME 2020](http://aime20.aimedicine.info/) conference.

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


**HYPE**: Available to the scientific community through a data agreement. Please fill in the following form: https://forms.gle/M8DDtuMeWGfT3k4y5

# Results Reproducibility

**HYPE Dataset**

Since it is not possible to reproduce the results exactly as in the paper (because not all subjects wanted to donate data to the broader research community), we re-executed the scripts with the available dataset tha can be obtained after filling in the form above. This should be the output of the notebook `extract_features_and_predict_bp_from_ppg_hype.ipynb` *best_results*:

| **predicted\_variable** | **experiment\_type** | **k** | **MAE\_GBM\_MEAN** | **MAE\_GBM\_STD** | **MAE\_LGBM\_MEAN** | **MAE\_LGBM\_STD** | **MAE\_RF\_MEAN**  | **MAE\_RF\_STD**   | **MAE\_LR\_MEAN**  | **MAE\_LR\_STD**   | **MAE\_DUMMY\_MEAN** | **MAE\_DUMMY\_STD** |
| ----------------------- | -------------------- | ----- | ------------------ | ----------------- | ------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | -------------------- | ------------------- |
| **DBP**                 | biking               | 2     | 7.613349978333324  | 3.106239967730272 | 7.360168155954208   | 2.117581898310436  | 8.061667542016806  | 3.3161004994965704 | 6.521003366875357  | 2.5584947009158774 | 7.506030701754385    | 2.05878506653711    |
| **DBP**                 | 24 Hours             | 2     | 11.0344698407823   | 2.445440419148344 | 10.744885158613748  | 2.243951294097582  | 10.790160681378364 | 2.109163817347919  | 12.093416128392777 | 3.038191731934865  | 11.806660613038815   | 3.5723128979166106  |
| **SBP**                 | biking               | 2     | 9.879023447928953  | 1.662372428004632 | 9.513003095975233   | 0.7133487048013492 | 9.461666666666668  | 1.384995487357271  | 9.689095624747068  | 1.734356132739077  | 9.513003095975233    | 0.7133487048013492  |
| **SBP**                 | 24 Hours             | 2     | 14.760112750212937 | 4.268165375156772 | 14.869205297071844  | 4.351786287295664  | 15.468070025013558 | 4.078999099212703  | 15.664020493627312 | 4.623100877961526  | 15.435089876989352   | 4.161358479573512   |

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
