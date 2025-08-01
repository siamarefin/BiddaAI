# BiddaAI

BiddaAI is a simple, multilingual Retrieval-Augmented Generation (RAG) system built with Next.js. It can understand and respond to queries in both English and Bengali, using a local PDF document as its knowledge base.

## ✨ Features

- **Multilingual Support**: Responds to both English and Bengali queries.
- **Retrieval-Augmented Generation**: Fetches relevant information from a PDF document to provide grounded answers.
- **Chat Memory**: Maintains short-term conversation history.
- **REST API**: Exposes a simple API for interaction.

## 🛠️ Tech Stack

- **Framework**: [Next.js](https://nextjs.org/)
- **LLM & Embeddings**: [Google Gemini](https://ai.google.dev/)
- **Orchestration**: [LangChain.js](https://js.langchain.com/)
- **Vector Store**: [ChromaDB](https://www.trychroma.com/) (running locally)
- **PDF Parsing**: [pdf-parse](https://www.npmjs.com/package/pdf-parse)

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en) (v18.17 or later)
- [Git](https://git-scm.com/)
- A Google AI Studio API Key. You can get one [here](https://makersuite.google.com/app/apikey).

### Installation

1.  **Clone the repository:**

    ```bash
    git clone <your-repo-url>
    cd BiddaAI
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Create a file named `.env.local` in the root of your project and add your Google API key:

    ```env
    GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"
    ```

4.  **Add Knowledge Base:**
    Place your PDF file (e.g., `HSC26_Bangla_1st_paper.pdf`) inside a `data` directory in the project root.

5.  **Ingest Data:**
    Run the ingestion script to process your PDF, create vector embeddings, and store them locally in the Chroma vector store. This only needs to be done once, or whenever the source document changes.

    ```bash
    npm run ingest
    ```

6.  **Run the development server:**
    ```bash
    npm run dev
    ```

Open http://localhost:3000 with your browser to see the result.
