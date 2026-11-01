# 📚 Semantic Book Recommender

A book recommendation system that uses semantic search to help readers discover books based on natural-language descriptions, categories, and emotional preferences.

## ✨ Overview

Traditional book recommendation systems often rely on predefined genres or keywords. This project explores a semantic approach, allowing users to describe the kind of story they're looking for and retrieve books with similar meanings.

The system uses OpenAI embeddings and ChromaDB to perform similarity-based retrieval, combined with category filtering and emotion-based ranking.

## 🚀 Features

- **Semantic Search:** Discover books using natural-language descriptions rather than exact keywords.
- **Category Filtering:** Narrow recommendations by book category.
- **Emotion-Based Filtering:** Explore books based on emotional tones such as Happy, Surprising, Angry, Suspenseful, and Sad.
- **Interactive Dashboard:** Search and browse recommendations through a Gradio interface.
- **Book Preprocessing:** Explore book descriptions, categories, and emotional characteristics through Jupyter notebooks.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core development |
| Pandas & NumPy | Data processing |
| OpenAI API | Text embeddings |
| LangChain | Document processing and integration |
| ChromaDB | Vector storage and similarity search |
| Gradio | Interactive user interface |
| Jupyter Notebook | Data exploration and analysis |

## 📂 Project Structure

```text
Semantic-Book-Recommender/
│
├── books_cleaned.csv
├── books_with_categories.csv
├── books_with_emotions.csv
├── tagged_description.txt
├── cover-not-found.jpg
│
├── data-exploration.ipynb
├── setiment_analysis.ipynb
│
├── gradio-dashboard.py
├── main.py
│
├── .gitignore
└── README.md
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/asma-gud/Semantic-Book-Recommender.git

cd Semantic-Book-Recommender
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

On macOS / Linux:

```bash
source .venv/bin/activate
```

On Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install pandas numpy python-dotenv gradio langchain-community langchain-openai langchain-text-splitters langchain-chroma
```

### 4. Configure your OpenAI API key

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_api_key_here
```

Make sure your `.env` file is not committed to GitHub.

### 5. Run the application

```bash
python gradio-dashboard.py
```

Open the local Gradio URL displayed in your terminal to access the dashboard.

## 🔍 How It Works

1. Book descriptions are prepared and represented as documents.
2. OpenAI embeddings transform the descriptions into numerical representations.
3. ChromaDB indexes the documents for similarity-based retrieval.
4. Users enter a natural-language description of the book they are looking for.
5. The system retrieves semantically similar books.
6. Category and emotional-tone preferences refine the recommendations.

