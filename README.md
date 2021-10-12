# AIME 2020

This repository relates to section `3.2` from our paper:

**HYPE: Predicting Blood Pressure from Photoplethysmograms in a Hypertensive Population** [(Link)](https://link.springer.com/chapter/10.1007/978-3-030-59137-3_29)

Best student paper at the [AIME 2020](https://arianesasso.me/2020/08/12/aime-2020/) conference.

For the code related to secion `3.3` please refer to this repository: [PPG-to-BP-Prediction-convnets](https://github.com/suparno89/PPG-to-BP-Prediction-convnets)

----
For running the notebooks:

```
pipenv install
pipenv shell
pipenv run jupyter notebook
```

Please add to your `config.json` file the paths to each dataset, e. g.:

```
"hype":"../../datasets/hype", # path to the hype dataset folder
"eval":"../../datasets/eval", # path to the processed eval dataset file referenced below
```

The notebooks process raw PPG data and predict blood pressure for 2 different datasets:

`HYPE`: extract_features_and_predict_bp_from_ppg_hype.ipynb

`EVAL`: extract_features_and_predict_bp_from_ppg_eval.ipynb

# Datasets Information

**EVAL**: https://www.kaggle.com/mkachuee/noninvasivebp (original)

However, we processed it and used the following file as the input to our notebook: https://doi.org/10.6084/m9.figshare.12649691


**HYPE**: Available to the scientific community through a data agreement. Please
fill in the following form: https://forms.gle/M8DDtuMeWGfT3k4y5

For generating the input for section `3.3` the above data needs to be processed
using `processing_hype_for_3_3/json_ppg_bp_window_hype.ipynb`

# Results Reproducibility

**HYPE Dataset**

Since it is not possible to reproduce the results exactly as in the paper (because not all subjects wanted to donate data to the broader research community), we re-executed the scripts with the available dataset tha can be obtained after filling in the form above. This should be the output of the notebook `extract_features_and_predict_bp_from_ppg_hype.ipynb` *best_results*:

| **predicted\_variable** | **experiment\_type** | **k** | **MAE\_GBM\_MEAN** | **MAE\_GBM\_STD** | **MAE\_LGBM\_MEAN** | **MAE\_LGBM\_STD** | **MAE\_RF\_MEAN**  | **MAE\_RF\_STD**   | **MAE\_LR\_MEAN**  | **MAE\_LR\_STD**   | **MAE\_DUMMY\_MEAN** | **MAE\_DUMMY\_STD** |
| ----------------------- | -------------------- | ----- | ------------------ | ----------------- | ------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | -------------------- | ------------------- |
| **DBP**                 | biking               | 2     | 7.613349978333324  | 3.106239967730272 | 7.360168155954208   | 2.117581898310436  | 8.061667542016806  | 3.3161004994965704 | 6.521003366875357  | 2.5584947009158774 | 7.506030701754385    | 2.05878506653711    |
| **DBP**                 | 24 Hours             | 2     | 11.0344698407823   | 2.445440419148344 | 10.744885158613748  | 2.243951294097582  | 10.790160681378364 | 2.109163817347919  | 12.093416128392777 | 3.038191731934865  | 11.806660613038815   | 3.5723128979166106  |
| **SBP**                 | biking               | 2     | 9.879023447928953  | 1.662372428004632 | 9.513003095975233   | 0.7133487048013492 | 9.461666666666668  | 1.384995487357271  | 9.689095624747068  | 1.734356132739077  | 9.513003095975233    | 0.7133487048013492  |
| **SBP**                 | 24 Hours             | 2     | 14.760112750212937 | 4.268165375156772 | 14.869205297071844  | 4.351786287295664  | 15.468070025013558 | 4.078999099212703  | 15.664020493627312 | 4.623100877961526  | 15.435089876989352   | 4.161358479573512   |

**EVAL Dataset**

When processing this file: https://doi.org/10.6084/m9.figshare.12649691 using `extract_features_and_predict_bp_from_ppg_eval.ipynb` the *best_results* should be:

| **predicted\_variable** | **experiment\_type** | **k** | **MAE\_GBM\_MEAN** | **MAE\_GBM\_STD** | **MAE\_LGBM\_MEAN** | **MAE\_LGBM\_STD** | **MAE\_RF\_MEAN**  | **MAE\_RF\_STD**  | **MAE\_LR\_MEAN**  | **MAE\_LR\_STD**   | **MAE\_DUMMY\_MEAN** | **MAE\_DUMMY\_STD** |
| ----------------------- | -------------------- | ----- | ------------------ | ----------------- | ------------------- | ------------------ | ------------------ | ----------------- | ------------------ | ------------------ | -------------------- | ------------------- |
| **DBP**                 | kaggle               | 2     | 7.865446544017316  | 2.267393274853124 | 7.57220318998406    | 2.3845234314216945 | 7.644171242199798  | 2.489483420588713 | 7.871258403903799  | 2.0669919349077728 | 7.664836489656983    | 2.184583329953216   |
| **SBP**                 | kaggle               | 2     | 16.18703094573625  | 4.355064754562451 | 16.005655885115857  | 4.625746788262742  | 16.745896699769194 | 4.784200038452515 | 16.707034825286065 | 4.32198051974363   | 15.54764126683809    | 4.9577070660961455  |

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
