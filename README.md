# introDS_final_project (last update: Sep 12, 2021)

Members:

#1 18127154 - Võ Ngọc Minh - MeinHserhT

#2 18127155 - Vũ Công Minh - MinhVu2018

Mentors: <br>
Mr. Trần Trung Kiên <br>
Ms. Phan Thị Phương Uyên <br>

```
project
│   README.md
│   Slide.pptx 
│   Teamwork.pdf
│ 
└───data
│   │   full_name.txt
│   │   raw_description.txt
│   │   description.txt
│   │   preseason_elo.csv
│   │   preseason_data.csv
│   │   raw_data.csv
│   │   data.csv
│   
└───notebook
    │   Crawl Data.ipynb
    │   NBA Prediction.ipynb
```

Data files:
1. <b>full_name.txt:</b> NBA teams' name and their abbreviation.
2. <b>raw_description.txt:</b> stats' description for raw_data
3. <b>description.txt:</b> stats' description for cleaned_data
4. <b>preseason_elo.csv:</b> summary elo in preseason
5. <b>preseason_data.csv:</b> average teams' stats in <b>preseason</b>
6. <b>raw_data.csv:</b> detail data of each match from season 2016-2017 -> 2020-2021 
7. <b>data.csv:</b> detail cleaned_data

Jupyter notebook files:
1. 'Crawl Data.ipynb': Crawl data and save to files
2. 'NBA Prediction.ipynb': Clean, process raw_data to create cleaned_data and use it to train and predict outcomes.

How to use:
Step 1: Install libs and google chrome
Step 2: Run 'Crawl Data.ipynb', it will create data file {1,2,4,5,6}
Step 3: Run 'NBA Prediction.ipynb', it will create data file {3,7}
 
## 1. Data Sources
[basketball-reference](https://www.basketball-reference.com/)
[projects.fivethirtyeight.com](https://projects.fivethirtyeight.com/2016-nba-picks/)

## 2. References:
- https://towardsdatascience.com/predicting-the-outcome-of-nba-games-with-machine-learning-a810bb768f20
- https://stackoverflow.com/questions/35388647/how-to-use-gridsearchcv-output-for-a-scikit-prediction
- https://www.kaggle.com/hatone/mlpclassifier-with-gridsearchcv
- https://analyticsindiamag.com/guide-to-hyperparameters-tuning-using-gridsearchcv-and-randomizedsearchcv/
- https://www.analyticsvidhya.com/blog/2015/06/tuning-random-forest-model/
- https://www.kaggle.com/faressayah/decision-trees-random-forest-for-beginners

## 3. Summary
<b>Data size:</b> 6247 lines (games)
<b>Input_DataFrame:</b> [Date, H_Team_Name, H_ave_stats..., H_pre_elo A_Team_Name, A_ave_stats..., A_pre_elo]
<b>Output:</b> [is_Home_Win] (True/False)

<b>Result:</b>
> logistic_regression_score: 0.6364605543710021

> random_forest_score: 0.6332622601279317

> neural_network_score: 0.6471215351812367 

=> Currently, the best model is <b>Neural Network (MLP Classifier)</b>

Predict the 1st round of the upcoming NBA season (2021-2022)
```
Tue, Oct 19, 2021: MIL will win BRK
Tue, Oct 19, 2021: LAL will win GSW
Wed, Oct 20, 2021: CHO will lose IND
Wed, Oct 20, 2021: DET will lose CHI
Wed, Oct 20, 2021: NYK will win BOS
Wed, Oct 20, 2021: TOR will win WAS
Wed, Oct 20, 2021: MEM will win CLE
Wed, Oct 20, 2021: MIN will win HOU
Wed, Oct 20, 2021: NOP will lose PHI
Wed, Oct 20, 2021: SAS will win ORL
Wed, Oct 20, 2021: UTA will win OKC
Wed, Oct 20, 2021: POR will win SAC
Wed, Oct 20, 2021: PHO will win DEN
Thu, Oct 21, 2021: ATL will win DAL
```