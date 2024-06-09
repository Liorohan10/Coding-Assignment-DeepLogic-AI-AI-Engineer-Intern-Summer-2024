# AI-Powered Document Processing Pipeline

## Tech Stacks Used

### 1. **AWS Textract**
   - **Purpose:** Optical Character Recognition (OCR) to extract text from documents, including both printed and handwritten text.
   - **Usage:** Converts scanned documents, PDFs, and images containing text into machine-readable text.

### 2. **AWS Bedrock**
   - **Purpose:** Provides foundation models for natural language processing tasks.
   - **Usage:** Used for embedding text and generating responses, leveraging models like Amazon Titan for text embedding and generation.

### 3. **LangChain**
   - **Purpose:** Framework for working with text data and embeddings, facilitating the integration and management of LLMs.
   - **Usage:** Handles text loading, splitting, and interaction with embeddings, making it easier to manage and utilize document chunks.

### 4. **Pinecone**
   - **Purpose:** Vector database for storing and querying vector embeddings.
   - **Usage:** Stores embeddings generated from document text and performs similarity searches to find relevant document chunks based on user queries.

## Approach

### 1. **Document Preprocessing with OCR**
   - **PDF to Image Conversion:** Converts PDF documents into images to facilitate text extraction.
   - **Text Extraction with AWS Textract:** Utilizes AWS Textract to extract text from the images, handling various document types and text formats.

### 2. **Text Processing and Embedding**
   - **Document Loading and Splitting:** Uses LangChain to load document content and split it into manageable chunks for processing.
   - **Text Embedding with AWS Bedrock:** Embeds the text chunks using Amazon Titan models via AWS Bedrock, generating high-quality embeddings for each chunk.

### 3. **Storing and Retrieving Embeddings**
   - **Vector Storage in Pinecone:** Stores the generated embeddings in Pinecone, enabling efficient similarity searches.
   - **Similarity Search:** Queries Pinecone to retrieve the most relevant document chunks based on user input.

### 4. **Interactive User Interface**
   - **Prompt Template Creation:** Defines a prompt template to structure the interaction between the user and the system.
   - **Response Generation with AWS Bedrock:** Invokes a language model from AWS Bedrock to generate coherent and contextually accurate responses based on the retrieved document chunks.

By combining these technologies and approaches, the project creates a robust pipeline for processing and understanding documents, extracting key information, and enabling seamless user interactions through a chatbot interface in the local command prompt

