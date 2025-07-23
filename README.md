# Recommender-systems-ML-project

## Dataset
This original data set contained files like movies-(name,ID) rating-(user id,movie id,rating) tags-(tag user give,user id,movie id,time stamp,tag)

That data was modified into the current form by the course instructor:

```
📁 data/
│   ├── 📄 content_bygenre_df.csv
│   ├── 📄 content_item_train.csv
│   ├── 📄 content_item_train_header.txt
│   ├── 📄 content_item_vecs.csv
│   ├── 📄 content_movie_list.csv
│   ├── 📄 content_top10_df.csv
│   ├── 📄 content_user_to_genre.pickle
│   ├── 📄 content_user_train.csv
│   ├── 📄 content_user_train_header.txt
│   ├── 📄 content_y_train.csv
│   ├── 📄 small_movie_list.csv
│   ├── 📄 small_movies_b.csv
│   ├── 📄 small_movies_R.csv   <--- This is the data used for collaborative filtering
│   ├── 📄 small_movies_W.csv
│   ├── 📄 small_movies_X.csv
│   └── 📄 small_movies_Y.csv
```

## Problem statement
- **Broad statement:** We need to recommend movies to users using collaborative filtering and content-based filtering.

## Collaborative filtering and content-based filtering
| Aspect                       | Collaborative Filtering                                             | Content‑Based Filtering                                  |
| ---------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------- |
| **Core idea**                | Use patterns in **other users’** behavior to recommend.             | Use **item features** and your own history to recommend. |
| **Data needed**              | User–item interactions (ratings, clicks, purchases).                | Item metadata/features (genres, keywords, attributes).   |
| **Recommendation signal**    | “Users who liked items A & B also liked item X.”                    | “You liked items with features F & G; here are more.”    |
| **Cold‑start problem**       | New **users** (no interactions) **and** new **items** (no ratings). | New **users** (no profile/history yet).                  |
| **Diversity of suggestions** | High—can surface unexpected items liked by similar users.           | Limited—stays close to your existing feature profile.    |
| **Scalability**              | Can become heavy with many users/items (large matrix).              | Scales with item features; usually lighter per user.     |