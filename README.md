# Machine Learning Trading Bot

The aim of this program is to use machine learning to create an algorithmic trading bot. The program was created for one of the top five financial advisory firms in the world. They have been able to profit more recently by using computer algorhithms but they still have needed humans to program them. By using maching learning, they are hoping to be able to use algorithms that can learn and adapt without human intervention.

Scroll down for my conclusions and data analysis.

---

## Technologies

This application is compatible with Python 3.9.
The Pandas, Numpy, scikit-learn, pathlib libraries were used along with hvplot and matplotlib and must be installed in order to run the program correctly.


Pandas is used for data science and analysis and machine learning.

Numpy is used to provide scientific computing support to Python.

Scikit-learn is used to create visual representations of machine learning models.

Pathlib is used point Python to file paths.

HvPlot allows for the creation of interactive graphs and plots of data.

Matplotlib is another visualization library.


This program will work on Windows, MacOS and Linux with Python 3.9 installed. The program is a Juypter notebook file and will run best in Juypter Lab.

Documentation for the Pandas library can be found [here.](https://pandas.pydata.org/docs/)

Documentation for the Numpy library can be found [here.](https://numpy.org/doc/stable/)

Documentation for the Scikit-Learn library can be found [here.](https://scikit-learn.org/stable/user_guide.html)

Documentation for the Matplotlib library can be found [here.](https://matplotlib.org/stable/users/index)

Documentation for the pathlib library can be found[here.](https://docs.python.org/3/library/pathlib.html)

Documentation for hvplot can be found [here.](https://hvplot.holoviz.org)


---

## Installation Guide

Install the following dependencies before running the program.

To install the pathlib, pandas and matplotlib libraries type the following into your CLI:

```
python
pip install pandas
pip install numpy
pip install -U scikit-learn
pip install -U matplotlib
pip install hvplot
pip install pathlib
```
---

## Usage

To run the program open your code editor and navigate to the folder containing the file ```machine_learning_trading_bot.ipynb```.

Load the program and run the cells in sequence from top to bottom.

The output displays various points of detailed analysis of the data including visual plots and graphs so the user can get a well rounded view of the data.

---

## Conclusions From My Data Analysis

ADJUSTING THE SIZE OF THE TRAINING DATASET:

Below we can see the line graph using the baseline data from the program default - Short SMA 4 days, Long SMA 100 days and training data offset of 3 months.

!["Baseline"](/Screenshots/baseline_3mos.png)

In this next example, we can see what happens when we adjust the size of the training dataset. 

This plot shows strategy returns vs actual returns when we lower the size of the training dataset to 1 month.

!["Training Dataset 1 Month"](/Screenshots/training_data_1mo.png)

This plot shows strategy returns vs actual returns when we increase the size of the training dataset to 10 months.

!["Training Dataset 10 Months"](/Screenshots/training_data_10mos.png)

Conclusion:

It would appear that the model makes better predictions when it uses a smaller training dataset vs a larger one.

ADJUSTING THE SMA INPUT FACTORS:

Below we can see the plot when we adjusted following parameters - Short SMA 4 Days, Long SMA 200 Days and the size of the training dataset 2 months.

!["Short SMA 4 Long SMA 200 2 Mos"](/Screenshots/shortSMA_4_longSMA_200_2_Mos.png)

This plot shows what happens when we adjust the following parameters - Short SMA 50 Days, Long SMA 300 Days and the size of the training dataset 3 months.

!["Short SMA 50 Long SMA 300 3 Mos"](/Screenshots/shortSMA_50_longSMA_300_3_Mos.png)

And finally this plot shows what happens when we adjust the following parameters - Short SMA 50 Days, Long SMA 300 Days and the size of the training dataset 10 months.

!["Short SMA 50 Long SMA 300 3 Mos"](/Screenshots/ShortSMA50LongSMA30010Mos.png)

Conclusion:

It would appear that the strategy returns are higher and more accurately mimic the movement of the actual returns when they are trained to a smaller short SMA value and a the long SMA value is inbetween 100 and 300. Also, the conclusion from the previous analysis appears to hold true that the model makes better predictions with a smaller training dataset.

From all of the models ran, I would have to say the following model seemed to produce the best results - Short SMA 4 Days, Long SMA 200 Days and the size of the training dataset 2 months.

EVALUATE A NEW MACHINE LEARNING CLASSIFIER:

In this section we used the default parameters of the program and applied them to a new machine learning model. I chose the ```AdaBoostClassifier```.

Below we can see the graph produced when the data was ran.

!["AdaBoost Backtest"](/Screenshots/backtest.png)

Conclusion:

It would appear, when compared to the default model, that the AdaBoost is an inferior machine learning model. Especially over time from 2018 to the present, the model appears to consistently underperform the actual returns.

---

## Contributors

Developed by:

Graham Johnstone
Email: johnstonegr@gmail.com

---

## License
This code is published under the Creative Commons License, 2022.

