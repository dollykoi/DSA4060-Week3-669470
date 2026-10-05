# DSA 4060 Week 3 – Content-Based Recommender Lab

This repository contains the Week 3 practical lab: a simple **content-based
recommender** built from structured movie features, following the workflow:

**Movie Features → User Preferences → Recommendation Scores → Top Recommendations**

## Student
- Name: Claire Mwarari
- Student number: 669470

## Repository contents

| File | Description |
|---|---|
| `content_based_lab.ipynb` | Complete, executed notebook with Markdown explanations for every step |
| `movies.csv` | The movie dataset (10 movies, 5 binary genre features) |
| `README.md` | This file |

## What the notebook does

1. **Explores** a small movie dataset (10 movies × 5 binary genre features:
   Action, Comedy, Drama, Romance, SciFi).
2. **Builds item profiles** — each movie is a binary feature vector.
3. **Builds a user profile** — features of rated movies are weighted by their
   ratings, summed, and normalized into preference proportions.
4. **Scores and ranks** every movie against the user profile, **removes already
   watched movies**, and generates **Top-N recommendations**.
5. Encapsulates the pipeline in a **reusable `recommend_movies()` function** and
   tests it on a second user.
6. Adds a **unique movie** ("Savannah Run", Comedy/Drama) and a **custom user**
   with Top-5 recommendations.
7. Concludes with **interpretation, limitations, and a reflection** on the
   final question (same movies + different ratings → different profiles →
   different recommendations).

## Key results

- **User A** (Action/SciFi viewer): Top 3 = *Space Warriors* (0.857),
  *City Detectives* (0.571), *Broken Hearts* (0.143).
- **User B** (Romance/Drama viewer): completely different Top 3, demonstrating
  personalization.
- **Custom user**: strongest preferences Action (0.375) and SciFi (0.208);
  Top 5 = *Future World*, *Space Warriors*, *City Detectives*,
  *Love in Nairobi*, *Savannah Run*.

## Limitations identified

Only five coarse features; rich metadata ignored; over-specialization
(filter bubble); new-user cold start; garbage-in-garbage-out metadata.

## How to run

Open `content_based_lab.ipynb` in Jupyter / Google Colab and run all cells.
The notebook is self-contained since it creates the dataset in-code, so no file
paths need to be changed.
