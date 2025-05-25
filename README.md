# 📊 Qatar 2022 World Cup Twitter Dataset: Query Examples & Full Codebook

Welcome to the **Qatar 2022 World Cup Twitter Dataset** companion notebook! 🎉  
This notebook is designed to help researchers, data scientists, and practitioners **understand, explore, and query** the dataset efficiently. It provides:

- ✅ Clear **variable definitions**  
- ✅ Example **real-world queries**  
- ✅ Practical **tips for filtering tweets by type, language, and user features**

---

## 📌 Dataset Access

📂 **Download the dataset here**:  
👉 [Qatar 2022 World Cup Twitter Dataset](https://your-dataset-url-here.com)  
*(Replace this with your actual URL)*

---

## 🧾 Citation

If you use this dataset in your research or project, please cite the following work:

> Daouadi, K. E., Boualleg, Y., Guehairia, O., & Taleb-Ahmed, A. (2025).  
> *Tracking the Global Pulse: The First Public Twitter Dataset from the FIFA World Cup*.  
> *Journal of Computational Social Science*.

### 📘 BibTeX:
```bibtex
@article{daouadi2025worldcup,
  title={Tracking the Global Pulse: The First Public Twitter Dataset from the FIFA World Cup},
  author={Daouadi, Kheir Eddine and Boualleg, Yacine and Guehairia, Oussama and Taleb-Ahmed, Abdelmalik},
  journal={Journal of Computational Social Science},
  year={2025}
}
🧵 Dataset Overview
Each row in the Qatar22WC.csv file represents a single tweet, enriched with comprehensive user-level and tweet-level metadata, enabling rich social media analysis.

👤 User-Level Metadata
Variable	Description
age_of_the_user_account	Age of the user's Twitter account in days
tweet_count	Total number of tweets posted by the user
location	User-defined location
follower_count	Number of followers
following_count	Number of accounts the user follows
follower_to_Following	Ratio of followers to following
favouite_count	Total number of tweets liked by the user
verified	1 if the user is verified, 0 otherwise
Avg_tweet_count	Average tweets per day (tweet_count ÷ account_age)
list_count	Number of public Twitter lists the user appears in

🐦 Tweet-Level Metadata
Variable	Description
Tweet_Id	Unique identifier for the tweet
day, month, year	Date of the tweet
hou, min, sec	Time of the tweet (hour, minute, second)
is_reply_to_tweet	ID of the tweet being replied to; NaN if not a reply
is_quote	1 if the tweet is a quote tweet, 0 otherwise
retid	ID of the retweeted tweet; "0" or NaN if not a retweet
lang	Language of the tweet (e.g., 'ar', 'en', 'fr')
hashtags	List of hashtags used (stored as a string)
is_image	1 if the tweet contains an image
is_video	1 if the tweet contains a video

🔎 Example Query Types
Here are some popular use cases and queries to help you get started:

🔍 Filter Type	💡 Description
Tweet Type	Select original tweets, retweets, replies, or quotes
Verified Users	Filter tweets from verified users (verified == "1")
Language Filtering	Choose tweets by language (lang == 'ar', lang == 'en', etc.)
Hashtag Matching	Find tweets mentioning specific events or matches via hashtags
Media Content	Identify tweets that contain images (is_image == "1") or videos (is_video == "1")

🧪 Example Query
Find tweets in Arabic posted by verified users that include images:

python
Copier
Modifier
df[(df['verified'] == "1") & (df['lang'] == 'ar') & (df['is_image'] == "1")]
