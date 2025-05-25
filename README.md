# Tracking the Global Pulse: The First Multilingual Twitter Dataset from the FIFA World Cup
🎉Welcome to the **Qatar 2022 World Cup Twitter Dataset** companion notebook! 🎉  

The notebook "fifa-wc-qatar22-examples-of-queries.ipynb" is designed to help researchers and practitioners **understand, explore, and query** the dataset efficiently. It includes:

✅ Clear **variable definitions**  
✅ Example **real-world queries**  
✅ Helpful **tips for filtering tweets by type, language, and user features**

---
## 🧾 Dataset Snapshot

Each row in `Qatar22WC.csv` represents a **single tweet**, enriched with **user-level and tweet-level metadata** for in-depth social media analysis.
---
### 👤 User-Level Metadata

- `age_of_the_user_account`: Age of the user's Twitter account in days.
- `tweet_count`: Total number of tweets posted by the user.
- `location`: User-defined location provided by the user.
- `follower_count`: Number of followers the user has.
- `following_count`: Number of accounts the user is following.
- `follower_to_Following`: Ratio of followers to following.
- `favouite_count`: Total number of tweets liked by the user.
- `verified`: Boolean flag — `1` if the user is verified, `0` otherwise.
- `Avg_tweet_count`: Average number of tweets per day (i.e., `tweet_count ÷ age_of_the_user_account`).
- `list_count`: Number of public Twitter lists that include the user.

---

### 🐦 Tweet-Level Metadata

- `Tweet_Id`: Unique identifier for the tweet.
- `day`, `month`, `year`: Date when the tweet was posted.
- `hou`, `min`, `sec`: Time of the tweet (hour, minute, second).
- `is_reply_to_tweet`: ID of the tweet being replied to (if applicable); `NaN` if not a reply.
- `is_quote`: `1` if the tweet is a quote tweet; otherwise `0`.
- `retid`: ID of the retweeted tweet (if any); `0` or `NaN` means it is not a retweet.
- `lang`: Language of the tweet (e.g., `'ar'` for Arabic, `'en'` for English).
- `hashtags`: List of hashtags used in the tweet (stored as a string).
- `is_image`: `1` if the tweet includes an image.
- `is_video`: `1` if the tweet includes a video.
---
## 🔎 Popular Query Types

💬 Looking for quick insights? Here are some **query ideas** to get you started:

| 🔍 Filter Type         | 🧠 What It Retrieves                                               |
|------------------------|--------------------------------------------------------------------|
| **Tweet Type**         | Original tweets, retweets, quote tweets, or replies                |
| **Verified Users**     | Tweets only from verified users (`verified == "1"`)                  |
| **Language Filtering** | Tweets in Arabic, English, French, etc. (`lang == 'ar'`, etc.)     |
| **Hashtag Matching**   | Tweets that mention specific games or events using hashtags        |
| **Media Content**      | Tweets that include images or videos (`is_image == "1"`, etc.)    |

---


## 📌 Dataset Access

📂 **Download the dataset here**:  👉 [Qatar 2022 World Cup Twitter Dataset](https://data.mendeley.com/datasets/gw3mcnbkwr/1)
---

## 🧾 Citation

If you use this dataset in your research or project, please cite the following work:

> Daouadi, K. E., Boualleg, Y., Guehairia, O., & Taleb-Ahmed, A. (2025).  
> *Tracking the Global Pulse: The First Public Twitter Dataset from the FIFA World Cup*.  
> *Journal of Computational Social Science*.
---
### 📘 BibTeX:
```bibtex
@article{daouadi2025worldcup,
  title={Tracking the Global Pulse: The First Public Twitter Dataset from the FIFA World Cup},
  author={Daouadi, Kheir Eddine and Boualleg, Yaakoub and Guehairia, Oussama and Taleb-Ahmed, Abdelmalik},
  journal={Journal of Computational Social Science},
  year={2025}
}
