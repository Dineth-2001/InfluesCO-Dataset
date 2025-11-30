# InfluesCO Dataset

Recommending the Right Sri Lankan YouTube Influencer for Your Marketing Needs

This repository contains the dataset used in the InfluesCO project; a data-driven system designed to identify the most relevant Sri Lankan YouTube influencers for brand marketing campaigns.

The dataset includes cleaned and structured channel-level, video-level, and comment-level information collected using the YouTube Data API v3.

## 📁 Dataset Structure

The dataset is available in CSV and JSON formats.

Each record corresponds to one YouTube channel, containing:

- **Channel metadata**  
- **10 most recent videos** (video-level data)  
- **100 most recent comments** (comment-level data)  

### 📦 File Formats
#### 1. JSON Format

Each JSON record contains the following structure:

```json
{
  "_id": "UCTcATaNqlaCF4zkZp29BJRQ",
  "uploaded_at": { "$date": "2025-07-30T11:56:21.602Z" },
  "data": {
    "channel_info": { ... },
    "original_search_name": "Blok & Dino",
    "recent_videos": [ ... 10 video objects ... ],
    "comments": [ ... 100 comment objects ... ]
  }
}
```

#### 2. CSV Format

The CSV files provide flattened and analysis-ready versions of:

- **channels.csv**: channel-level aggregated features
- **videos.csv**: video-level fields for 10 recent videos
- **comments.csv**: comment-level features for 100 recent comments

## 🧱 Data Components
#### 1. Channel-Level Data

Includes metadata and engagement metrics:

- Channel title, description
- Country (LK)
- Keywords
- Topic categories
- Subscriber/view/video counts
- Branding settings
- Published dates
- Last updated timestamps

#### 2. Video-Level Data (10 most recent videos)

Each channel contains 10 video entries with:
- Video title, description
- Thumbnails
- Tags
- Categories
- Published dates
- Engagement metrics (views, likes, comments)
- Content details (duration, definition, etc.)
- Topic categories

#### 3. Comment-Level Data (100 most recent comments)

For each channel:
- Comment text (display & original)
- Author metadata
- Like counts
- Reply counts
- Published/updated timestamps
- Full comment thread structure

## 🎯 Purpose of This Dataset

This dataset was developed to support the InfluesCO research project, enabling:
- Influencer recommendation for brands
- Text and metadata embedding generation
- Graph-based similarity smoothing
- Clustering of Sri Lankan YouTubers
- Sentiment and engagement analysis

This repository enables reproducibility of the analytical pipeline described in the project report.

## 📚 How to Use the Dataset
#### 1. For Data Science / ML Work

You can use:
- Channel descriptions + titles + tags → text embeddings
- Engagement metrics → clustering, scoring
- Video/comment text → sentiment, topic modeling
- Multimodal features → recommendation models

#### 2. For Software Applications

Suitable for:
- Influence scoring engines
- Social media analytics tools
- Marketing-targeting systems
- Creator discovery/recommendation apps

## Sample Record (Simplified)

Below is a simplified illustration (full structure included in the dataset):

```json
{
  "_id": "UCTcATaNqlaCF4zkZp29BJRQ",
  "data": {
    "channel_info": { ... },
    "recent_videos": [ { ... video1 ... }, ... ],
    "comments": [ { ... comment1 ... }, ... ]
  }
}
```

### 📎 Notes

All data was collected using public YouTube API endpoints.

Only publicly available information is included.

📝 Citation

If you use this dataset in your work, please cite the InfluesCO project:

InfluesCO — Recommending the Right Sri Lankan YouTube Influencer for Your Marketing Needs (2025)
