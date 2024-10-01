# Recommendations With IBM Project

For this project, I will analyze user interactions with articles on the IBM
Watson Studio platform and develop recommendation systems to suggest new
articles that align with their interests. By applying key concepts from
recommendation systems, such as collaborative filtering and content-based
filtering, the goal is to create personalized suggestions that enhance the user
experience and increase engagement with the platform.

## Project Setup

### Clone this repository

```shell
(base)$: git clone git@github.com:mafda/recommendations_with_ibm.git
(base)$: cd recommendations_with_ibm
```

### Configure environment

- Create the conda environment

    ```shell
    (base)$: conda env create -f environment.yml
    ```

- Activate the environment

    ```shell
    (base)$: conda activate recommendations_ibm
    ```

- Download the dataset from [this
  link](https://drive.google.com/drive/folders/15nFBCV2GE0UQobtuG2enFlVDhu9Bhno6?usp=share_link),
  create `data` folder and copy the `articles_community.csv` and
  `user-item-interactions.csv` datasets here.

    ```shell
    (recommendations_ibm)$: mkdir data
    ```

## Project Structure

```shell
.
├── README.md
├── data
│   ├── articles_community.csv
│   └── user-item-interactions.csv
├── environment.yml
├── src
│   ├── project_tests.py
│   └── recommendations_with_ibm.ipynb
└── test
    ├── top_10.p
    ├── top_20.p
    ├── top_5.p
    └── user_item_matrix.p
```

## Project Components

**I. Exploratory Data Analysis**

Before making recommendations of any kind, you will need to explore the data you
are working with for the project. Dive in to see what you can find. There are
some basic, required questions to be answered about the data you are working
with throughout the rest of the notebook. Use this space to explore, before you
dive into the details of your recommendation system in the later sections.

**II. Rank Based Recommendations**

To get started in building recommendations, you will first find the most popular
articles simply based on the most interactions. Since there are no ratings for
any of the articles, it is easy to assume the articles with the most
interactions are the most popular. These are then the articles we might
recommend to new users (or anyone depending on what we know about them).

**III. User-User Based Collaborative Filtering**

In order to build better recommendations for the users of IBM's platform, we
could look at users that are similar in terms of the items they have interacted
with. These items could then be recommended to the similar users. This would be
a step in the right direction towards more personal recommendations for the
users. You will implement this next.

**IV. Content Based Recommendations (EXTRA - NOT REQUIRED)**

Given the amount of content available for each article, there are a number of
different ways in which someone might choose to implement a content based
recommendations system. Using your NLP skills, you might come up with some
extremely creative ways to develop a content based recommendation system. You
are encouraged to complete a content based recommendation system, but not
required to do so to complete this project.

**V. Matrix Factorization**

Finally, you will complete a machine learning approach to building
recommendations. Using the user-item interactions, you will build out a matrix
decomposition. Using your decomposition, you will get an idea of how well you
can predict new articles an individual might interact with (spoiler alert - it
isn't great). You will finally discuss which methods you might use moving
forward, and how you might test how well your recommendations are working for
engaging users.

## References

- [Data Scientist Nanodegree
  Program](https://www.udacity.com/course/data-scientist-nanodegree--nd025)

---

made with 💙 by [mafda](https://mafda.github.io/)
