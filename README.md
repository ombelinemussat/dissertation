# dissertation
Code and data for dissertation

The notebooks should be run in the following order:
- final_scraping_thejournal.ipynb -> scrapes the different pages of thejournal.ie
      - The following datasets are obtained:
        for the articles -> "articles_1_10.csv", "articles_11_20.csv", "articles_21_30.csv",
          "articles_31_40.csv", "articles_41_50.csv", "articles_51_55.csv",
          "articles_56_60.csv", "articles_61_68.csv"
        for the comments ->  "comments_1_10.csv", "comments_11_20.csv", "comments_21_30.csv",
        "comments_31_40.csv", "comments_41_50.csv", "comments_51_55.csv",
        "comments_56_60.csv", "comments_61_68.csv"
        They will be used in the next notebook.
- merging_dataset.ipynb -> merges all the datasets together to form one dataset with articles from 2016 to 2024
      - The following datasets are obtained: with all the articles -> "articles_2016_2024.csv", with all the comments: "comments_2016_2024.csv"
        They will be used in the next notebook.
- data_cleaning.ipynb
      - The following datasets are obtained: with all the cleaned articles -> "cleaned_articles_2016_2024.csv", with all the cleaned comments: "cleaned_comments_2016_2024.csv"
        They will be used in the next notebook.
- Lexicoder.ipynb
      - The following datasets are obtained: the articles and sentiment analysis -> "articles_with_lexicoder_sentiment.csv", the comments and sentiment analysis: "comments_with_lexicoder_sentiment.csv"
        The articles data will be used in the next notebook.
- LDA.ipynb
      - The following dataset is obtained: "articles_with_LDA.csv"
        It will be used in the next notebook.
- get_authors.ipynb
      - The following dataset is obtained: "final_df_without_commentsentiment.csv"
        It will be used in the next notebook.  
- link_tone_articles_comments.ipynb
      - The datasets "final_df_without_commentsentiment.csv" and "comments_with_lexicoder_sentiment.csv" are needed in this notebook
      - The following dataset is obtained: "final_df.csv"
        It will be used in the next notebook.  
- regressions.ipynb

In addition to this main analysis, the following notebooks should be run as well:

To see if there is a difference between the negativity of Brexit articles and other articles:
- scraping_other_articles.ipynb
      - To look at which year to scrape, the dataset "final_df.csv" is needed in this notebook
      - The following dataset is obtained: "articles_2400_2422.csv"
        It will be used in the next notebook.
- cleaning_other_subjects.ipynb
      - The following dataset is obtained: "cleaned_articles_other_subjects.csv"
        It will be used in the next notebook.  
- Lexicoder_other_subjects.ipynb
      - This notebook requires the datasets: "cleaned_articles_other_subjects.csv" and "final_df.csv"

To see if there is a variation of negativity over time within Brexit articles :
- plot_neg_over_time.ipynb
      - This notebook requires the dataset: "articles_with_lexicoder_sentiment.csv"

Other Sentiment Analysis methods:
- VADER.ipynb
      - This notebook requires the dataset: "cleaned_articles_2016_2024.csv"
- hugging_face_sa.ipynb
      - This notebook requires the dataset: "cleaned_articles_2016_2024.csv"
