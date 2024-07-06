# Indian Panel Code (IPC) Query System Implementation Using [Pinecone](https://docs.pinecone.io/home) 🍍

This poject leverages the power of Pinecone, a vector database, to efficiently retrieve information related to the Indian Penal Code (IPC) sections.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Data Source](#data-source)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The IPC Query System is developed to facilitate easy access to legal information contained within the Indian Penal Code. By utilizing Pinecone's vector database, the system ensures quick and precise retrieval of sections based on user queries.

## Features

- Efficient querying of IPC sections
- High accuracy in retrieving relevant legal information
- Fast search capabilities using Pinecone's vector database

## Technologies Used

- Python
- Pinecone VectorDB
- Hugging Face APIs
- Embeddings: E5 (Small)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/ipc-query-system.git
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. View the IPC data by parsing the provided PDF:
    - Download the PDF from [IPC 1860](https://www.iitk.ac.in/wc/data/IPC_186045.pdf).
    - Use a PDF parsing library (e.g., PyMuPDF, pdfminer), I have used PyPDFDirectoryLoader from langchain's document_loaders.

2. Index the IPC data into Pinecone:
    ```python
    import pinecone
    pc = pinecone.Pinecone(api_key=PC_KEY)
    index_name = "<index-name>"
    index = pc.Index(index_name)
    ```

3. Start the query system:
    ```python
    streamlit app.py
    ```

4. Access the system via your web browser at `http://localhost:5000`.

5. Enter your query in the search bar to retrieve relevant IPC sections.

## Data Source

The data for this project is sourced from the Indian Penal Code (IPC) document available at [IPC 1860 PDF](https://www.iitk.ac.in/wc/data/IPC_186045.pdf).

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for review.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any queries or suggestions, please contact:

- Name: Akshat Sanghvi
- Email: jakshat569@gmail.com
- GitHub: [iiakshat](https://github.com/iiakshat/)
- LinkedIn: [Akshat Sanghvi](https://www.linkedin.com/in/akshat-sanghvi/)

---

Thank you for using the IPC Query System!
