# Reddit Community Analysis

## Project Overview

This project analyzes the Reddit community's reaction and discussion to Taylor Swift's announcement of *1989 (Taylor's Version)* on August 9, 2023. Using data science techniques including network analysis, sentiment analysis, and community detection, we explore how different fan communities responded to this major music industry announcement.

## Research Questions

- How did the Reddit community react to the 1989 (Taylor's Version) announcement?
- What were the most discussed themes and topics?
- How did sentiment vary across different fan communities?
- What patterns emerged in community formation and user interactions?
- Which users were most influential in the discussions?

## Key Findings

### Community Engagement
- **52 posts** collected from 5 subreddits during the announcement period
- **4,528 comments** from 2,468 unique users
- **59.2% positive sentiment** across all comments
- **12 distinct communities** detected in the social network

### Most Discussed Themes
1. **The Color Blue** (214 mentions) - Album's signature color
2. **Clowning/Theories** (140 mentions) - Fan speculation and theories
3. **1989 Imagery** (77 mentions) - Seagulls and album aesthetics
4. **Hints/Easter Eggs** (42 mentions) - Taylor's cryptic clues

### Network Analysis
- **2,468 users** connected through shared post participation
- **334,659 connections** between users
- **Graph density of 0.1099** indicating a well-connected community
- **Largest community**: 809 members

## 🛠️ Technical Stack

### Required Packages
```bash
pip install networkx
pip install python-louvain
pip install vaderSentiment
pip install pandas
pip install seaborn
pip install matplotlib
pip install wordcloud
pip install praw
```

### Core Libraries
- **PRAW**: Reddit API wrapper for data collection
- **NetworkX**: Network analysis and graph operations
- **python-louvain**: Community detection algorithms
- **VADER**: Sentiment analysis for social media text
- **Pandas**: Data manipulation and analysis
- **Seaborn/Matplotlib**: Data visualization
- **WordCloud**: Text visualization


## 📈 Methodology

### Data Collection
- **Time Period**: August 9-16, 2023 (announcement + 5 days)
- **Subreddits**: r/TaylorSwift, r/TaylorSwiftPictures, r/popheads, r/Fauxmoi, r/popculturechat
- **Search Queries**: 12 different keywords including "1989 (Taylor's Version)", "vault tracks", "Taylor Swift announced"
- **Data Points**: Post metadata, comments, user interactions, timestamps

### Analysis Techniques

#### 1. Sentiment Analysis
- **Tool**: VADER (Valence Aware Dictionary and sEntiment Reasoner)
- **Output**: Compound sentiment scores (-1 to +1)
- **Categories**: Positive (≥0.05), Negative (≤-0.05), Neutral (-0.05 to 0.05)

#### 2. Network Analysis
- **Graph Construction**: Users connected if they commented on the same posts
- **Edge Weighting**: Number of shared posts between users
- **Centrality Measures**: Degree centrality to identify influential users
- **Community Detection**: Louvain algorithm for community identification

#### 3. Thematic Analysis
- **Keyword Tracking**: Predefined themes (clowning, easter eggs, color blue, imagery)
- **Word Cloud Generation**: Visual representation of common terms
- **Sentiment by Theme**: Correlation between topics and emotional responses

## Data Sources

### Subreddits Analyzed
- **r/TaylorSwift**: Main fan community
- **r/TaylorSwiftPictures**: Visual content and fan art
- **r/popheads**: General pop music discussion
- **r/Fauxmoi**: Celebrity gossip and news
- **r/popculturechat**: Pop culture discussions

### Data Fields Collected
- **Posts**: ID, title, text, score, comments, upvote ratio, timestamp, author, flair
- **Comments**: ID, body, score, author, timestamp, associated post
- **Metadata**: Creation dates, user information, engagement metrics

## 🔍 Analysis Results

### Sentiment Distribution
```
Positive: 59.2% (2,680 comments)
Neutral:  24.3% (1,101 comments)
Negative: 16.5% (747 comments)
```

### Top Influential Users
1. pink_princess08 (centrality: 0.6259)
2. CowboyLikeMegan (centrality: 0.5667)
3. Traditional-Egg-2656 (centrality: 0.5460)
4. coltsmetsfan614 (centrality: 0.4880)
5. fooledmeagain (centrality: 0.4820)

### Community Insights
- **Community 5**: 809 members, highest engagement
- **Community 4**: 728 members, very positive sentiment
- **Community 3**: 624 members, moderate sentiment
- **Community 2**: 539 members, balanced discussion
- **Community 0**: 516 members, diverse opinions

## Visualizations

The analysis includes several key visualizations:
- **Upvote Ratio Distribution**: How positively posts were received
- **Comment Length Distribution**: Depth of community engagement
- **Sentiment Analysis Charts**: Overall emotional tone
- **Network Community Visualization**: Social structure analysis
- **Theme-based Word Clouds**: Most discussed topics
- **Community Sentiment Comparison**: Emotional patterns across groups

## Key Insights

### 1. Overwhelmingly Positive Reception
The community showed 59.2% positive sentiment, indicating strong excitement about the announcement.

### 2. Active Fan Theories
"Clowning" (fan speculation) was a major theme, showing the community's engagement with Taylor's cryptic hints.

### 3. Strong Community Formation
The network analysis revealed 12 distinct communities, each with unique discussion patterns and sentiment profiles.

### 4. Visual Theme Dominance
The color blue and seagull imagery were heavily discussed, reflecting the album's aesthetic.

### 5. Cross-Community Engagement
Users frequently participated across multiple posts, creating a well-connected discussion network.


## License

This project is for educational and research purposes. Please respect Reddit's terms of service and API usage guidelines.

## Acknowledgments

- Reddit community members for their discussions
- PRAW developers for the Reddit API wrapper
- NetworkX and python-louvain teams for network analysis tools
- VADER sentiment analysis creators
- Taylor Swift fan communities for their engagement

