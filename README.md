# 🏡 HomeMatch: Personalized Real Estate Agent using AI

**HomeMatch** is an AI-powered real estate recommendation system that helps users find homes tailored to their preferences. It leverages natural language processing (NLP), vector similarity search, and LLMs to enable conversational search over property listings.

## 🔍 Features

- ✅ Search real estate listings using natural language
- ✅ Extract and store semantic embeddings for efficient retrieval
- ✅ Personalize results with context-aware filtering
- ✅ Interactive chatbot interface using OpenAI + LangChain
- ✅ Stores vectorized listings in **ChromaDB**

## 📁 Dataset

The project uses a curated dataset of U.S. real estate listings in JSON format:

- `real_estate_listings.json`: Contains property metadata including:
  - `address`, `city`, `price`, `beds`, `baths`, `area`, `description`, etc.

## 🛠️ Tech Stack

- **Python**
- **Jupyter Notebook**
- **OpenAI API** (for embeddings and chat)
- **LangChain** (conversational agent framework)
- **ChromaDB** (vector database for retrieval)
- **FAISS** (alternative for vector indexing)
- **Gradio** *(optional)* – for building an interactive frontend

## ⚙️ How It Works

1. **Data Preprocessing**:
   - Parses and cleans real estate data
   - Converts it into a structured `Document` format

2. **Embeddings**:
   - Uses OpenAI's `text-embedding-ada-002` to embed listing descriptions
   - Stores vectors in ChromaDB for fast similarity search

3. **Conversational Retrieval Chain**:
   - Powered by LangChain's `ConversationalRetrievalChain`
   - Maintains chat history and contextual responses

4. **Interactive Q&A**:
   - Ask questions like:
     > “Find me a 3-bedroom house in Miami under $500,000 with a pool”
   - Get listings that match the criteria with rich detail

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/HomeMatch-AI.git
cd HomeMatch-AI
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set your OpenAI API key

```python
import os
os.environ["OPENAI_API_KEY"] = "your-key-here"
```

### 4. Run the notebook

Launch the `Personalized - Real Estate Agent.ipynb` notebook and step through each cell.

## 📷 Sample Output

Example query:
> "Show me a 2-bedroom condo in New York near Central Park"

Sample response (from chatbot):
```
🏠 2 Bed, 1 Bath Condo
📍 New York, NY (Central Park area)
💵 $480,000
📏 950 sq ft
📝 Description: A cozy modern condo steps away from Central Park with hardwood floors and updated kitchen.
```

## 💡 Future Enhancements

- Add voice-to-text search
- Integrate with live MLS data
- Add user profile preference learning
- Use **RAG (Retrieval-Augmented Generation)** for richer responses


---

Would you like this in a downloadable file or added to your project folder?
