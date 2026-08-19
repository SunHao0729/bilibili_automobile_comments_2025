# Bilibili Auto Comment Dataset

Dataset for the paper *"Ranking before Reacting: Learning to Rank for Early Prediction of Controversy-causing Comments"*. Contains Bilibili (哔哩哔哩) automobile-related video comment data collected in 2025.

Each sample is a root comment and its nested reply tree under an automotive video. Controversy scores are derived from LLM-annotated stance labels (agree / disagree / neutral) on reply edges, defined as the proportion of disagree edges among all annotated edges. The dataset includes 4,434 comment threads across 137 videos, with 139,672 stance annotations and cross-post behavior sequences for 17,597 users.

All user, video, and comment identifiers have been anonymized. Text content is in Simplified Chinese.

## Files

- **`bilibili_auto_comments.jsonl`** — Main dataset. Each line is a comment thread with reply tree, controversy score, topic facet label, and 15-fold video-level train/val/test splits.
- **`stance_annotations.jsonl`** — LLM-generated stance labels (agree / disagree / neutral) for each reply edge, used to compute controversy scores.
- **`cross_post_user_sequences.jsonl`** — Chronological comment sequences of users active across multiple videos.
