# Hi there, I'm Chris! 

---

### About Me
- **Education:** University of California, Riverside - Bachelors of Science in Computer Science with Business Applications
- **Interests:** AI/LM, Food/Cooking, Cars, Games, 

---

### Skills & Tools
- **Languages:** Python, C++, SQL, Java, JavaScript, and TypeScript.
- **Frameworks/Libraries:** PyTorch, TensorFlow, Hugging Face Transformers, FastAPI, React, scikit-learn, and LlamaIndex.
- **Tools:** Docker, Linux, PostgreSQL, Redis, Milvus, ChromaDB, Pandas, NumPy, OpenCV, and Tesseract.
  
---

### Recent Projects
- **[AIRA - AI Research Assistant](https://github.com/ChrisWoo0443/AIRA)** - AIRA is a full-stack app that turns your documents into a searchable, chat-based research assistant. Upload PDFs and text files, then ask questions in natural language. A FastAPI backend handles ingestion, embeddings, and RAG; a React frontend provides the UI; and Ollama runs the LLM locally.
- **[MITR - Mutual Information Transformer Regularization](https://github.com/ChrisWoo0443/hiva-ijca-mitr)** - Developed MITR (Mutual Information Transformer Regularization) in the hopes to improve the training efficiency and generalization of encoder-only models like DistilBERT. By implementing the Contrastive Log-Ratio Upper Bound (CLUB) estimator, I created a custom loss function that penalizes redundant information between consecutive hidden layers. The project was evaluated on the SQuAD v2.0 dataset, testing the model's ability to handle complex reading comprehension and unanswerable questions. This approach forces the transformer to maintain more independent, diverse representations, reducing the "information bottleneck" during backpropagation. The results analyze how penalizing mutual information affects task accuracy and representation diversity in deep NLP architectures.
- **[Content Manager](https://github.com/ChrisWoo0443/content_manager)** - Developing a full-stack project management platform for creators designed to streamline content planning, scripting, and collaboration. Built with a Next.js 14 frontend and a FastAPI backend, the app features a Markdown-based document editor with image support and a PostgreSQL-backed organization system similar to Notion or Google Drive. Currently in active development, the project utilizes uv for high-performance Python package management and focuses on scalable system architecture.

---

### Recent Contributions & PRs
<details>
  <summary><b>Implement Vector Store Management tools [diri-cyrex]</b></summary>
  <br>
  
  **Link:** [PR #37](https://github.com/Team-Deepiri/diri-cyrex/pull/37)
  
  **Description:**
  There were conflicting api routes which is why I decided to just restart
deepiri-cyrex-dev does take a second to load but that is most likely due to me being on cpu only (will switch to cuda after)

app/integrations/milvus/*:
- Milvus store was refactored into its own directory
- connection.py: better connection and error handling.
- store.py: all of the functionality for old milvus_store to add/delete/view/list/etc.
- schema.py: collection schemas
- exceptions.py: error handling for milvus to help find out whats wrong
  
FastApi routers:
- app/routes/collection_management_api.py
- app/routes/documents.py

app/core/system_initializer.py:
- connects and creates the collections if not already created when system starts

cyrex-interface/src/App.tsx:
- added a view for collections and documents. Can now add and delete documents from collections.
</details>

<details>
  <summary><b> Weak default JWT Secerets [diri-cyrex]</b></summary>
  <br>
  
  **Link:** [PR #43](https://github.com/Team-Deepiri/diri-cyrex/pull/43)
  
  **Description:**
  Issue 3: Weak Default JWT Secret in Python

implemented recommended fix:
def __init__(self):
    self.logger = logger
    jwt_secret = getattr(settings, 'JWT_SECRET', None) or os.getenv('JWT_SECRET')
    
    if not jwt_secret:
        raise ValueError(
            'JWT_SECRET must be set in environment variables. '
            'This is required for security. Set JWT_SECRET before starting the application.'
        )
    
    if len(jwt_secret) < 32:
        raise ValueError(
            f'JWT_SECRET must be at least 32 characters long. '
            f'Current length: {len(jwt_secret)}'
        )
    
    self._jwt_secret = jwt_secret
    self._api_key_header = 'x-api-key'
    self._auth_header = 'authorization'
    self._initialized = False

added auth test and config
</details>

<details>
  <summary><b> Reorganized Testing UI [diri-cyrex]</b></summary>
  <br>
  
  **Link:** [PR #25](https://github.com/Team-Deepiri/diri-cyrex/pull/25)
  
  **Description:**
  Updated Cyrex testing UI for oraganization.
  Added sidebar for easy navigation.
  Reorganized pages 

</details>

---

### Connect with Me
[<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/chris-woo04)
[<img src="https://img.shields.io/badge/Resume-EB1919?style=for-the-badge&logo=read-the-docs&logoColor=white" />](https://github.com/ChrisWoo0443/ChrisWoo0443/blob/main/ResumeFeb2026.pdf)

