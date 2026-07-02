# 🎥 YouTube Sentiment Analysis

A scalable **YouTube Sentiment Analysis** web application built with **Python**, **Streamlit**, **YouTube Data API v3**, and **Natural Language Processing (NLP)**. The application scrapes comments from any YouTube video, analyzes their sentiment using the **NLTK VADER** sentiment analyzer, and presents the results through an interactive dashboard.

---

## 📖 Overview

This project enables users to analyze the overall sentiment of comments on any YouTube video by simply providing the video URL.

The application:
- Scrapes YouTube comments using the **YouTube Data API v3**
- Retrieves video and channel information
- Performs sentiment analysis using **NLTK VADER**
- Displays interactive visualizations using **Plotly**
- Allows downloading the scraped comments as a CSV file

---

## ✨ Features

### 📥 Data Scraping
- Fetches top-level comments from any YouTube video
- Saves comments into a downloadable CSV file
- Supports pagination for collecting multiple comments

### 📺 Channel & Video Insights
Displays useful metadata including:

#### Channel Information
- Channel logo
- Channel name
- Total subscribers
- Total uploaded videos
- Channel creation date
- Channel description

#### Video Statistics
- Video title
- Total views
- Total likes
- Total comments

---

### 😊 Sentiment Analysis

The application uses the **NLTK VADER (Valence Aware Dictionary and sEntiment Reasoner)** lexicon to classify every comment into one of the following categories:

- 🟢 Positive
- 🔴 Negative
- ⚪ Neutral

It also calculates:

- Total Positive Comments
- Total Negative Comments
- Total Neutral Comments

---

### 📊 Interactive Visualizations

The dashboard includes:

- 📈 Bar Chart
- 🥧 Pie Chart

Both charts are generated using **Plotly Express** and **Plotly Graph Objects**.

---

### 🌐 Web Interface

A clean and responsive web interface built using **Streamlit**.

---

# 📂 Project Structure

```
YouTube-Sentiment-Analysis/
│
├── app.py
├── Senti.py
├── YoutubeCommentScrapper.py
├── README.md
└── .streamlit/
    └── secrets.toml
```

### `app.py`

Main Streamlit application.

Responsibilities:
- UI Layout
- Sidebar inputs
- Display metrics
- Display charts
- Display channel information
- Download CSV

---

### `Senti.py`

Handles the complete NLP pipeline.

Responsibilities:
- Extract Video ID
- Sentiment Analysis
- VADER Polarity Score
- Plotly Charts
- Data Processing

---

### `YoutubeCommentScrapper.py`

Handles communication with the **YouTube Data API v3**.

Responsibilities:
- Fetch comments
- Fetch video metadata
- Fetch channel metadata
- Handle pagination
- Export CSV

---

# 🛠️ Technologies Used

- Python
- Streamlit
- YouTube Data API v3
- NLTK
- Pandas
- Plotly
- Google API Python Client
- Colorama

---

# 📦 Prerequisites

Install the following Python packages:

```bash
pip install streamlit google-api-python-client nltk pandas plotly colorama
```

The application automatically downloads the **VADER Lexicon** during the first run.

---

# 🚀 Installation

## 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <repository-directory>
```

---

## 2. Install Dependencies

```bash
pip install streamlit google-api-python-client nltk pandas plotly colorama
```

---

## 3. Configure API Key

Create a folder named:

```
.streamlit
```

Inside it, create:

```
secrets.toml
```

Add your YouTube API key:

```toml
API_KEY = "YOUR_YOUTUBE_API_KEY_HERE"
```

> **Note:** You need a Google Cloud Platform account with the **YouTube Data API v3** enabled.

---

## 4. Run the Application

```bash
streamlit run app.py
```

---

# 📖 Usage

1. Launch the Streamlit application.
2. Open it in your browser.
3. Paste a YouTube video URL into the sidebar.
4. The application will:
   - Fetch comments
   - Retrieve channel information
   - Retrieve video statistics
   - Perform sentiment analysis
   - Generate interactive charts
   - Create a downloadable CSV file

---

# 📊 Output

The application displays:

- Channel Information
- Video Statistics
- Sentiment Counts
- Positive Comments
- Negative Comments
- Neutral Comments
- Pie Chart
- Bar Chart
- Downloadable CSV

---

# 📈 Workflow

```
User Input (YouTube URL)
            │
            ▼
Extract Video ID
            │
            ▼
YouTube Data API
            │
            ▼
Fetch Comments
            │
            ▼
Save Comments to CSV
            │
            ▼
NLP (NLTK VADER)
            │
            ▼
Sentiment Classification
            │
            ▼
Positive | Neutral | Negative
            │
            ▼
Plotly Visualizations
            │
            ▼
Streamlit Dashboard
```

---

# 📸 Dashboard Features

- 🎥 Video Preview
- 👤 Channel Details
- 📊 Video Statistics
- 😊 Sentiment Analysis
- 📈 Interactive Charts
- 📥 CSV Download

---

# 🔮 Future Improvements

- Support multilingual sentiment analysis
- Emotion detection (Happy, Angry, Sad, etc.)
- Word cloud generation
- Comment filtering by date
- Spam detection
- Machine Learning-based sentiment classification
- User authentication
- Historical sentiment tracking

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push to your branch.
5. Open a Pull Request.

---

# 📄 License

This project is licensed under the **MIT License**.

---

# 👨‍💻 Author

Developed using **Python**, **Streamlit**, **YouTube Data API v3**, and **NLTK** for scalable YouTube comment sentiment analysis.
