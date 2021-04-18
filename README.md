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

**HYPE**

Since it is not possible to reproduce the results exactly as in the paper (because not all subjects wanted to donate data to the broader research community), we re-executed the scripts with the available dataset tha can be obtained after filling in the form above.

| **predicted\_variable** | **experiment\_type** | **k** | **MAE\_GBM\_MEAN** | **MAE\_GBM\_STD**  | **MAE\_LGBM\_MEAN** | **MAE\_LGBM\_STD** | **MAE\_RF\_MEAN**  | **MAE\_RF\_STD**   | **MAE\_LR\_MEAN**  | **MAE\_LR\_STD**   | **MAE\_DUMMY\_MEAN** | **MAE\_DUMMY\_STD** |
| ----------------------- | -------------------- | ----- | ------------------ | ------------------ | ------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ | -------------------- | ------------------- |
| **DBP**                 | biking               | 2     | 7.293550534546307  | 2.8787367096341656 | 7.391252334136137   | 2.3467447428642467 | 7.572409838935574  | 3.0155597414035578 | 6.991582016622066  | 3.1742611133636816 | 7.506030701754385    | 2.05878506653711    |
| **DBP**                 | 24 Hours             | 2     | 11.375351272182638 | 2.9669968480865307 | 11.172062920392026  | 2.96208558328551   | 11.147668536341357 | 2.640232169181638  | 11.85872946766777  | 2.802756600308569  | 11.806660613038815   | 3.5723128979166106  |
| **SBP**                 | biking               | 2     | 9.620825808218244  | 1.9173913973941197 | 9.513003095975233   | 0.7133487048013492 | 9.760416666666668  | 1.8843508958288824 | 10.692218932677363 | 3.2997889067182573 | 9.513003095975233    | 0.7133487048013492  |
| **SBP**                 | 24 Hours             | 2     | 14.759570184233535 | 3.93754088209812   | 15.134568974372126  | 4.188432981970437  | 15.612944756575374 | 4.225143474013567  | 15.660378259869423 | 4.60564118583747   | 15.435089876989352   | 4.161358479573512   |

# More Information about this Project

Morassi Sasso, Ariane (2020): https://figshare.com/projects/AIME_2020/85166
