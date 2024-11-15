# local_docs_RAG
An interactive Jupyter Notebook application that allows users to ask questions about selected documents and receive AI-generated answers based on the content of those documents.

<!-- If you have a demo GIF or screenshot, include it here -->

Table of Contents
Features
Getting Started
Prerequisites
Installation
Usage
Project Structure
Contributing
License
Acknowledgments
FAQ
Issues and Bug Reporting
Features
Document Processing: Automatically loads and processes documents from a specified directory.
Multi-Format Support: Supports PDF, TXT, DOCX, and DOC file formats.
Interactive Widgets: Utilizes ipywidgets for interactive document selection and question input within Jupyter Notebook.
AI-Powered Responses: Uses the Ollama language model to generate context-aware answers based on document content.
Conversation History: Maintains a history of interactions for context-aware follow-up questions.
User-Friendly Interface: Clean and straightforward interface for seamless user experience.
Getting Started
Prerequisites
Python 3.6 or higher
Jupyter Notebook or JupyterLab
Git (for cloning the repository)
Required Python Packages:
ipywidgets
ollama
pandas
python-docx
PyPDF2
textract
Installation
Clone the Repository

bash
Copy code
git clone https://github.com/your-username/document-qa-assistant.git
cd document-qa-assistant
Create a Virtual Environment (Recommended)

bash
Copy code
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
Install Dependencies

bash
Copy code
pip install -r requirements.txt
Enable Jupyter Notebook Extensions

bash
Copy code
jupyter nbextension enable --py widgetsnbextension
Usage
Prepare Your Documents

Place your documents in the data/ directory.
Ensure the PDF_DIR variable in the code is set to 'data/'.
Launch Jupyter Notebook

bash
Copy code
jupyter notebook notebooks/Document_QA_Assistant.ipynb
Interact with the Application

Select Documents: Use the provided widget to select one or more documents from the list.
Ask Questions: Enter your question in the text field and click "Ask Question".
View Responses: The assistant will display answers based on the content of the selected documents.
Conversation History: The output area will display all previous questions and answers for context.
Project Structure
scss
Copy code
document-qa-assistant/
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── src/
│   └── assistant.py
├── data/
│   ├── document1.pdf
│   ├── document2.txt
│   └── ...
├── notebooks/
│   └── Document_QA_Assistant.ipynb
└── docs/
    ├── demo.gif
    └── (Additional documentation)
src/: Contains the main source code for the assistant.
data/: Directory where you should place your documents.
notebooks/: Contains the Jupyter Notebook for running the application.
docs/: Additional documentation or resources, such as images or demo files.
Contributing
Contributions are welcome! Please follow these steps:

Fork the Repository

Create a New Branch

bash
Copy code
git checkout -b feature/your-feature-name
Make Changes and Commit

bash
Copy code
git commit -m "Add your descriptive commit message"
Push to Your Fork

bash
Copy code
git push origin feature/your-feature-name
Create a Pull Request

Go to the original repository on GitHub and click "New Pull Request".
License
This project is licensed under the MIT License.

Acknowledgments
Ollama for the language model.
ipywidgets for interactive widgets.
PyPDF2 for PDF processing.
textract for text extraction from various formats.
python-docx for DOCX file processing.
FAQ
Q1: What file formats are supported?

A: The application supports PDF, TXT, DOCX, and DOC file formats.

Q2: Do I need an internet connection to use the application?

A: Yes, if the Ollama language model is cloud-based. If you have a local installation of the model, internet connectivity may not be necessary.

Q3: Can I use a different language model?

A: The application is designed to use the Ollama language model, but you can modify the code to integrate other models that support similar APIs.

Q4: How can I add more document formats?

A: You can extend the extract_text_from_document function in the code to include additional file formats by implementing corresponding extraction functions.

Q5: Is the conversation history stored?

A: The conversation history is maintained during the session but is not saved to disk. Once you restart the notebook or reset the widgets, the history will be cleared.

Issues and Bug Reporting
If you encounter any issues or bugs, please open an issue on the GitHub repository with detailed information to help us resolve the problem.
