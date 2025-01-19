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

The majority of participants answered that Rock is their favorite genre, followed by Pop, Metal, Classical and Video game music, in the top 5. The least favorite genre is Latin, followed by Gospel, Lofi, Jazz and K-pop.

![Image](https://github.com/user-attachments/assets/845d4457-e2a3-45af-9417-a715594e09e6)

**Favorite genre and Music effects**

Only the very minority of listeners have stated that music worsens their mental conditions. The only genres with participants who think that are: Classical, Pop, Rap, Rock and Video game music.

**Number of users by Primary Streaming Service**

![Image](https://github.com/user-attachments/assets/2ccba8e1-2741-4d96-bf58-1c27d5358108)

**While working, Exploratory, Foreign languages and Music effects percentages**

![Image](https://github.com/user-attachments/assets/b05ef4b7-d5bc-45d5-9fa8-0c9491fb4d96)

**Intrumentalist and Composer percentages**

![Image](https://github.com/user-attachments/assets/2a30cb15-e281-48bf-9459-0bec12734f79)

**Favorite genre grouped by each condition's median**

If we consider just these values alone, participants with Folk as their favorite genre display the highest anxiety levels of all, with a median of 8, Rap and Gospel have the lowest anxiety, with a 4.5 median. Rock, Hip Hop, K-pop, Lofi and Rock have a median of 7 anxiety. When it comes to OCD, only rap stands out with a median of 3, adn Gospel with 0, while other genres having a very similar median overall. The highest insomnia levels goes to Lofi, with a median insomnia of 6, while Gospel and Metal have a median of 5, the lowest are: R&B with 0, and K-pop and Metal with 1. As for depression, the genre with the highest median is Lofi (8), followed by Hip Hop (7), the lowest ones are Gospel (1), Rap and K-pop (3).

![Image](https://github.com/user-attachments/assets/9197bc60-7a74-4ad7-94ea-813ffb8c6028)

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

**Favorite genres where OCD is above the median**

Latin and Rap.

**Favorite genres where insomnia is above the median**

EDM, Folk, Gospel, Jazz, Latin, Lofi, Metal, Rock, and Video game music.

**Favorite genres where depression is above the median**

EDM, Hip hop, Lofi, Metal, and Rock.

**Instrumentalists conditons's means**

![Image](https://github.com/user-attachments/assets/8ad5c943-6976-41af-ad67-aedbb143ee06)

**Composer conditons's means**

![Image](https://github.com/user-attachments/assets/1c17beaa-fef0-4145-af4c-c7bf0d356d5d)

**Concentration of age and hours per day**

This graph shows that the highest concentration in hours per day is between 0-5h, and the highest concentration of age is between 14-25.

![image](https://github.com/user-attachments/assets/e3f70c6e-45f5-4b07-ae95-9d5b823fbb06)

**Total participants of each age group**

![image](https://github.com/user-attachments/assets/0bec8970-1a33-4065-918b-f87476e4dd67)

**Age group by contitions's medians**

Seniors have a lower median of every condition compared to the other age groups. However this could be statistically not accurate, since seniors are such a low percentage between participants, demanding hypothesis testing to see if the differences are actually relevant.

![Captura de tela 2025-01-19 153556](https://github.com/user-attachments/assets/107e0602-b502-4c40-b3dc-eb87c29c113a)

**Total primary streaming service usage by age**

![Captura de tela 2025-01-16 213142](https://github.com/user-attachments/assets/8dd8b087-8e22-4548-ae18-6ac41110935c)

**Distribution of Music Genre Listening Frequencies**

The most listened to genre is rock, with 45.1% of the participants declaring they listen to it very frequently, and only 12.1% who never listen to it. Gospel is genre that is the least listened to overall, with only 1.9% of participants who listen to it very frequently, and 72% who never listen to it, followed by latin, with 4.3% who very frequently listen to it, and 60% who never listen to it.

![Captura de tela 2025-01-16 213142](https://github.com/user-attachments/assets/ac6c563d-2bda-4ec3-bf34-a9cbf14ca484)

**Correlation between Age, Hours per day, Anxiety, Depression, Insomnia, and OCD**

This shows that there is a correlation between depression and anxiety (0.52), depression and insomnia (0.38) anxiety and ocd (0.34), anxiety and insomnia (0.28), insomnia and OCD (0.20), and depression and OCD (0.19). This means that these variables are dependent, which changes the types of hypothesis tests we can do with the data.

![image](https://github.com/user-attachments/assets/9d14f194-7a01-4fb6-8b8c-632e4ac05eed)

**Correlation between frequency and conditions**

We can see that there is a strong correlation between listening to hip Hop and Rap, Hip Hop and R&B, R&B and Rap, and Rock and Metal. That makes sense since these genres can be very similar sometimes.

![image](https://github.com/user-attachments/assets/232fa57a-d486-4d19-b3d0-7a44316c5224)

**Spread of Insomnia, OCD, Depression and Anxiety**

A shapiro-wilk normality test was conducted to check if the distributions are normal, since the p-values are significantly below the significance level of 0.05, we conclude that none of the distributions follow a normal distribution. Therefore, the median is a more suitable statistic for comparison, and nonparametric tests are the appropriate choice for hypothesis testing.

![image](https://github.com/user-attachments/assets/73b9753f-7e1c-402b-b2f3-b8525c4c211f)

**What conditions have a statiscally higher median on each favorite genre**

A Mann-Whitney U test was conducted to determine which favorite genres exhibit values higher than the overall median condition and to assess whether the difference is statistically significant. Here are the results: 

Where the median is significantly greater than the overall median: 

![Captura de tela 2025-01-19 154327](https://github.com/user-attachments/assets/a4830a83-a865-4bb4-89bd-5cbf2f047d54)

Where the median is significantly less than the overall median:

![Captura de tela 2025-01-19 154358](https://github.com/user-attachments/assets/0e3cbb7a-744b-4cfc-8445-30cccdde27a2)


