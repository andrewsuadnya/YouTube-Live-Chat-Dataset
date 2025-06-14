# YouTube Live Chat Datasets from High-Volume and Mid-Volume Streams

This repository contains structured datasets of YouTube **live chat messages** collected from three different live streams with varying levels of viewer engagement. The datasets are useful for analyzing real-time audience behavior, sentiment, and chat dynamics under different conditions — from high-volume influencer streams to official press briefings.

## 📦 Dataset Overview

| Stream Title                                              | Channel              | Viewers (Est.) | Messages | File Outputs                                  |
|-----------------------------------------------------------|----------------------|----------------|----------|-----------------------------------------------|
| IShowSpeed IRL Stream in Hong Kong 🇭🇰                     | IShowSpeed           | ±100,000       | 28,026   | `producer1.csv`<br>`producer1.json` |
| White House Press Briefing                                | LiveNOW from FOX     | ±20,000        | 6,686    | `producer2.csv`<br>`producer2.json` |
| Update on Man Executed in Arizona                         | LiveNOW from FOX     | ±9,000         | 7,460    | `producer3.csv`<br>`producer3.json` |

Each file contains only **regular live chat messages** and **excludes SuperChats** to focus on organic, unpaid public interaction.

## 📑 Data Fields

All datasets share a consistent schema with the following fields:

| Column        | Description                                       |
|---------------|---------------------------------------------------|
| `video_id`    | YouTube video ID of the live stream               |
| `author`      | Display name of the chat message sender           |
| `message`     | Content of the chat message                       |
| `published_at`| UTC timestamp when the message was published      |

## 🧪 Use Cases

These datasets are suitable for a variety of research and development tasks, including:

- Real-time sentiment analysis
- Detection of spam and toxic language
- Understanding audience behavior at different viewer scales
- Modeling chat activity dynamics across stream types (entertainment vs. news)

## ⚙️ Technical Details

- **Data Source**: YouTube Data API v3 (liveChatMessages endpoint)
- **Delivery Mode**: Real-time ingestion into Kafka, then exported to structured logs

## 📝 Notes

- All data collected is publicly visible via YouTube live chat and used here for educational and non-commercial research purposes.
- Timestamps are recorded in ISO 8601 format and in UTC for consistency.
- Some messages may contain emojis, slang, or sarcasm which can be useful for linguistic or sentiment studies.

## 🔒 License & Terms

This dataset is provided for **academic and non-commercial use only**. Users must comply with YouTube’s [Terms of Service](https://www.youtube.com/t/terms) and ensure appropriate handling of user-generated content.

---

**Maintained by**: Andrew Suadnya
**Date of Collection**: March 2025
