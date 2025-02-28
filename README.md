# Gadget Store Chatbot

This chatbot answers questions about products and FAQs using CSV data and a large language model (LLM). It reads product details from `products.csv` (name, category, price, stock, features) and FAQ pairs from `faqs.csv` (question, answer). The chatbot uses the Ollama LLM with the `deepseek-r1:1.5b` model, embedding model and langchain to understand and respond to queries.

**Setup:** 
Install Python 3.7+, required libraries (`pip install pandas streamlit langchain-ollama colab-xterm`), and Ollama with the `deepseek-r1:1.5b` model. 
Place `products.csv` and `faqs.csv` in the same directory as your python script, ensuring the files follow the specified column structure.

**Usage:** 
Run the python script. Type your question and press enter to receive a response. 
Type 'exit', 'quit', or 'bye' to end the session.

**Code:** 
The `generate_answer` function loads data from CSV files, formats it, and sends it with the user query to the LLM using a prompt template. 
The `chatbot` function manages the command-line interface.

**Potential improvements:** 
Implement vector database for better context retrieval, create a web UI with `streamlit`, integrate a database, add robust error handling and more sophisticated prompt engineering.

**Libraries:** 
`pandas`, `langchain-ollama`, `streamlit`, and `psycopg2`. 