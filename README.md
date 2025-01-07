# The King RAGent

The King RAGent is an AI-powered research assistant that leverages vector databases and external APIs to provide comprehensive answers to user queries. This application is built using Streamlit for the frontend and integrates various backend services for document processing and information retrieval.

## Features

- **PDF Upload and Processing**: Upload PDF documents to initialize the vector store.
- **AI-Powered Query Handling**: Use AI models to process and respond to user queries.
- **Web Search Integration**: Augment responses with web search results for enhanced accuracy.
- **Dry Run Mode**: Test the application without making actual API calls or database operations.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ragents.git
   cd ragent
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add your API keys and other necessary configurations.

## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run streamlit_app.py
   ```

2. Open your browser and navigate to the local URL provided by Streamlit.

## Dry Run Mode

The application now supports a `dry_run` mode, which allows you to test the app without making actual API calls or database operations. This is useful for development and testing purposes.

### How to Enable Dry Run Mode

- **Streamlit Interface**: Use the "🔧 Dry Run Mode" checkbox in the sidebar to toggle dry run mode on or off.
- **Backend Logic**: The `dry_run` parameter is propagated through the application, affecting the following components:
  - **VectorStore**: Skips database loading and returns mock data.
  - **call_claude_rag**: Returns a mock response instead of calling the Claude API.
  - **assess_confidence**: Returns a mock confidence level.
  - **synthesize_information**: Returns a mock synthesis of information.
  - **call_tavily_web_search**: Returns mock search results.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
