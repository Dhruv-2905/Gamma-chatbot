# Gemma Model Document Q&A

This project is a Streamlit application that allows users to ask questions about documents and get responses based on the content of the documents. The application uses the LangChain library, Google Generative AI embeddings, and FAISS for vector storage and retrieval.

## Features

- Load and process PDF documents.
- Embed documents using Google Generative AI embeddings.
- Retrieve relevant document chunks based on user queries.
- Answer questions using the ChatGroq language model.

## Requirements

- Python 3.x
- Streamlit
- LangChain
- FAISS
- PyPDF2
- Dotenv

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Dhruv-2905/Gamma-chatbot.git
    cd Gamma-chatbot
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    Create a `.env` file in the project root and add your API keys:
    ```
    GROQ_API_KEY=your_groq_api_key
    GOOGLE_API_KEY=your_google_api_key
    ```

5. Ensure your PDF documents are placed in the `./us_census` directory.

## Usage

1. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

2. Open your web browser and navigate to `http://localhost:8501`.

3. Click on "Documents Embedding" to process the documents.

4. Enter your question in the text input field and click enter to get responses based on the documents.

## Project Structure

├── app.py # Main Streamlit application script
├── requirements.txt # List of dependencies
├── .env # Environment variables file
├── us_census/ # Directory containing PDF documents
├── README.md # Project documentation
└── LICENSE # License file (optional)


## Code Overview

### `app.py`

- **Import Libraries**: Imports necessary libraries and modules.
- **Load Environment Variables**: Loads API keys from the `.env` file.
- **Streamlit Interface**: Sets up the Streamlit interface with a title, text input, and buttons.
- **Vector Embedding Function**: Processes PDF documents, creates document embeddings, and stores them in a vector database.
- **Document Q&A Functionality**: Retrieves relevant document chunks based on user queries and provides answers using the ChatGroq language model.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.
