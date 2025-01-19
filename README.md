# Music & Mental Health Analysis

As a musician and someone who listens and loves to music a lot, I always questioned myself about the effects some genres had on my overall thoughts and mental health. I came across [this](https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results/data) dataset on Kaggle and thought it would be a perfect opportunity to conduct data analysis and uncover insights on the subject. This project aims to explore the relationship between music genres and mental health issues. Using Python, I will load, transform, and analyze the data, create visualizations, and perform hypothesis testing to determine which genres are statistically associated with higher levels of anxiety, OCD, insomnia, and depression.

In the dataset, respondents answer generic questions focused on musical background and listening habits. Respondents rank how often they listen to 16 music genres, where they can select: Never, Rarely, Sometimes, and Very frequently.Respondents rank Anxiety, Depression, Insomnia, and OCD on a scale of 0 to 10, where: 0 - I do not experience this. 10 - I experience this regularly, constantly/or to an extreme.

## Technologies Used:


    Language: Python
    Python Libraries:
    Pandas: Used for data cleaning, manipulation and analysis
    Matplotlib & Seaborn: Used for visualizations.
    Scipy.stats: Used to perform hypothesis tests
    Jupyter Notebook: Used or interactive data exploration.

    The repository contains:

• mxmh_survey_results.csv.csv: The dataset used.

• Notebook.ipynb: A jupyter notebook containing the full analysis.

# OVERVIEW:

## 1- Exploratory Data Analysis:

First, the dataset was loaded and checked for inconsistent or missing values. A large number of missing values were found on the BPM column, they were replaced using the grouped median BPM of each genre, because the BPM values don't follow a normal distribution, hence the use of the median. Other missing values were present in the dataset but in insignificant numbers. These were removed from the dataframe to avoid affecting the overall analysis.

### Insights:

**Distribution of Favorite Music Genres**

![Image](https://github.com/user-attachments/assets/845d4457-e2a3-45af-9417-a715594e09e6)

The majority of participants answered that Rock is their favorite genre, followed by Pop, Metal, Classical and Video game music, in the top 5. The least favorite genre is Latin, followed by Gospel, Lofi, Jazz and K-pop.

**Favorite genre and Music effects**

Only the very minority of listeners have stated that music worsens their mental conditions. The only genres with participants who think that are: Classical, Pop, Rap, Rock and Video game music.

**Number of users by Primary Streaming Service**

![Image](https://github.com/user-attachments/assets/2ccba8e1-2741-4d96-bf58-1c27d5358108)

**While working, Exploratory, Foreign languages and Music effects percentages**

![Image](https://github.com/user-attachments/assets/b05ef4b7-d5bc-45d5-9fa8-0c9491fb4d96)

**Intrumentalist and Composer percentages**

![Image](https://github.com/user-attachments/assets/2a30cb15-e281-48bf-9459-0bec12734f79)

**Favorite genre grouped by each condition's median**

![Image](https://github.com/user-attachments/assets/9197bc60-7a74-4ad7-94ea-813ffb8c6028)

If we consider just these values alone, participants with Folk as their favorite genre display the highest anxiety levels of all, with a median of 8, Rap and Gospel have the lowest anxiety, with a 4.5 median. Rock, Hip Hop, K-pop, Lofi and Rock have a median of 7 anxiety. When it comes to OCD, only rap stands out with a median of 3, adn Gospel with 0, while other genres having a very similar median overall. The highest insomnia levels goes to Lofi, with a median insomnia of 6, while Gospel and Metal have a median of 5, the lowest are: R&B with 0, and K-pop and Metal with 1. As for depression, the genre with the highest median is Lofi (8), followed by Hip Hop (7), the lowest ones are Gospel (1), Rap and K-pop (3).

**Median values of each condition**

Anxiety:      6.0
OCD:          2.0
Insomnia:     3.0
Depression:   5.0

**Mean values of each condition**

Anxiety:       5.8
OCD:           2.6
Insomnia:      3.7
Depression:    4.8

**Favorite genres where anxiety is above the median**

Country, Folk, Hip hop, Jazz, K pop, Lofi, and Rock.
