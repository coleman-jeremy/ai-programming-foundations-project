## AI Programming Foundations Project

This project is part of my Master's in AI capstone built around the Titanic dataset. I cleaned the data, explored some patterns around survival rates, and made a few visualizations to see what the numbers actually show.

## Dataset
Titanic - Machine Learning from Disaster  
https://www.kaggle.com/c/titanic/data

## How to Run

Install dependencies:
pip install -r requirements.txt

Then open and run the notebook:
jupyter notebook data_workflow.ipynb

## Bias and Data Quality

There is an issue with 177 missing age values, and filling those in with the median probably skews everything toward the 15-30 range since that was where most passengers fell anyway, so those filled in values aren't really based on anything real. It also raises the question of where the age data even came from in the first place, because it couldn't have all been from ticket manifests since asking a woman her age in 1912 wasn't really appropriate. So female ages in particular might not be that reliable. On top of that, when I looked into the 80 year old survivor it turned out his age in the dataset was actually how old he was when he died 32 years later, not how old he was on the ship. That's a known error and it makes you wonder how many others there are that we just didn't catch.

## Future Reflections

**How this workflow would change for ML:**
For a machine learning project the visualizations wouldn't be as important since those are really just for humans to look at. The cleaning would matter a lot more though and would need to go deeper than what we did here. Things like making sure every column that a model would actually use is clean and complete would be the priority.

**Preparing this data for a neural network:**
The main thing would be converting the text columns like sex and embarked into numbers since a neural network can't work with text values. After that the numerical columns would need to be scaled so that something like fare which can be in the hundreds doesn't outweigh something like age. The data would also need to be split into training and testing sets before feeding it into a model.

**Where agentic AI could help:**
Almost every IDE has some form of AI or agentic tools built into it at this point. If you loaded the dataset and dropped the project instructions in, an agentic system could run through the entire workflow on its own. It would handle the cleaning, the analysis, and the visualizations without much input except picking chart styles. You'd probably get a better output than what I got from this project, and then you could just review it and be done.
