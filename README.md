# capstone-crypto-analysis
Student Developer Initiative Program by Hacktiv8 X IBM Skillsbuild. Capstone Project on Sentiment and Topic Classification in Reddit’s r/CryptoMarkets Using the IBM Granite Model (granite-3.3-8b-instruct).

**📜 Project Overview**

The cryptocurrency market is known for its extreme volatility, where public sentiment on social media can significantly influence price movements. However, distinguishing meaningful signals from noise on platforms like Reddit is a major challenge due to the massive, unstructured volume of data. Valuable information is often buried within thousands of posts, comments, and speculative discussions.

This project addresses that challenge by leveraging the generative AI power of IBM Granite to conduct in-depth analysis of discussion data from the r/CryptoMarkets subreddit. The goal is to automatically classify market sentiment (Bullish, Bearish, Neutral) and map key discussion topics (Technical Analysis, Regulations, Altcoin News, etc.). The results provide actionable and measurable insights into the pulse of the cryptocurrency market community.

**🎯 Objectives**
- Implement the IBM Granite AI model for text classification tasks on social media data.
- Identify the dominant sentiments expressed by market participants on Reddit.
- Map and analyze the frequency of the most discussed topics.
- Generate insights to better understand community reactions to market dynamics.
  
**💾 Dataset & Tech Stack**

**Dataset**
- Source: Reddit Subreddit r/CryptoMarkets
- Description: A dataset containing over 37,000 unique posts, including the fields title (post title) and selftext (post content), which serve as the basis for analysis.
- Link: https://www.kaggle.com/datasets/leukipp/reddit-crypto-data or R_cryptomarkets.csv in this repo

**Tech Stack**
- Programming Language: Python 3.10
- Key Libraries: Pandas (Data Manipulation), Matplotlib & Seaborn (Visualization), Requests (API Calls)
- AI Platform: IBM Granite-granite-3.3-8b-instruct (via API)
- Development Environment: Google Colab

**⚙️ Methodology / Analysis Process**
This project was carried out through four systematic stages:

**1. Data Acquisition & EDA**
Raw data from r/CryptoMarkets was loaded into the working environment. Exploratory Data Analysis (EDA) was performed to understand the structure, distribution, and quality of the dataset, including handling of missing values.

**2. Data Preprocessing**
Text from the title and selftext columns was combined to provide richer context. Data cleaning steps included lowercasing, removing URLs, and filtering out irrelevant characters to ensure high-quality input for the AI model.

**3. Generative AI Analysis**
Each cleaned text entry was sent to the IBM Granite API endpoint. Two separate engineered prompts were applied to perform sentiment classification and topic classification.

**4. Insight Extraction & Visualization**
The model outputs were stored back into a dataframe. Aggregate analysis was then conducted to calculate the frequency of each sentiment and topic. Key findings were visualized using bar charts and pie charts for effective presentation.

## 🤖 The Role of IBM Granite

IBM Granite serves as the core analysis engine in this project. Its ability to understand context and nuances in language is leveraged through specific prompt engineering to extract relevant information from unstructured text.

### - Example Prompt for Sentiment Classification:
**Task:** Classify the sentiment of the following crypto market text into one of three categories: 'Bullish', 'Bearish', or 'Neutral'.

**Text:** "[TEXT_POST]"

**Sentiment Category:**

### - Example Prompt for Topic Classification:
**Task:** Classify the following crypto discussion text into one of these topics: 'Technical Analysis (TA)', 'Fundamental Analysis (FA)', 'Altcoin News', 'Regulation & Macroeconomics', or 'General Discussion/Meme'.

**Text:** "[TEXT_POST]"

**Topic:**

## 📊 Insight & Findings

- What is the overall sentiment distribution in r/CryptoMarkets?
- What topics dominate discussions during the data period?
- Is there a correlation between certain topics and specific sentiments? (Example: Do 'Regulation' discussions tend to be 'Bearish'?)
- [Other interesting findings...]

## 🚀 How to Run This Project
## Clone Repository
```bash
git clone https://github.com/gilhan94/capstone-crypto-analysis.git'''

Open in Google Colab: Upload the .ipynb file to Google Colab.
Setup API Key: Store your IBM API Key in Colab Secrets with the name IBM_API_KEY.
Run the Notebook: Execute the cells in the notebook sequentially.
