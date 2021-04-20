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

Since it is not possible to reproduce the results exactly as in the paper (because not all subjects wanted to donate data to the broader research community), we re-executed the scripts with the available dataset tha can be obtained after filling in the form above. This should be the output of the notebook `extract_features_and_predict_bp_from_ppg_hype.ipynb` *best_results*.

| **predicted\_variable** | **experiment\_type** | **k** | **MAE\_GBM\_MEAN** | **MAE\_GBM\_STD**  | **MAE\_LGBM\_MEAN** | **MAE\_LGBM\_STD** | **MAE\_RF\_MEAN**  | **MAE\_RF\_STD**   | **MAE\_LR\_MEAN**  | **MAE\_LR\_STD**   | **MAE\_DUMMY\_MEAN** | **MAE\_DUMMY\_STD** |
| ----------------------- | -------------------- | ----- | ------------------ | ------------------ | ------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | -------------------- | ------------------- |
| **DBP**                 | biking               | 2     | 7.365180903644222  | 1.42574344320291   | 7.21388547160967    | 2.259170432109669  | 7.49047516025641   | 2.385761269361017  | 6.691526603660485  | 2.025474079015161  | 7.506030701754385    | 2.05878506653711    |
| **DBP**                 | 24 Hours             | 2     | 11.5772218928547   | 3.1116787079480326 | 11.54209696370962   | 3.621001359548013  | 11.76160708301905  | 2.9003063911298184 | 11.996429049764314 | 2.70707928100798   | 11.806660613038815   | 3.5723128979166106  |
| **SBP**                 | biking               | 2     | 9.209821009146644  | 0.8215670742067462 | 9.513003095975233   | 0.7133487048013492 | 9.158020833333332  | 0.9904225115081378 | 9.641164020032551  | 1.86864511011486   | 9.513003095975233    | 0.7133487048013492  |
| **SBP**                 | 24 Hours             | 2     | 14.951463663378464 | 3.654009135379758  | 14.90451764992514   | 3.911656397308085  | 16.029188339271318 | 4.136835655951774  | 15.5155481643245   | 4.1905929259631245 | 15.435089876989352   | 4.161358479573512   |

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
