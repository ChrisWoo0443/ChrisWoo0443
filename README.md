# Hi there, I'm Chris! 

---

### About Me
- **Education:** University of California, Riverside - Bachelors in Computer Science with Business Applications
- **Interests:** 

---

### Skills & Tools
- **Languages:** 
- **Frameworks/Libraries:** 
- **Tools:** 

---

### Recent Projects
- **[AIRA - AI Research Assistant](https://github.com/ChrisWoo0443/AIRA)** - AIRA is a full-stack app that turns your documents into a searchable, chat-based research assistant. Upload PDFs and text files, then ask questions in natural language. A FastAPI backend handles ingestion, embeddings, and RAG; a React frontend provides the UI; and Ollama runs the LLM locally.
- **[MITR - Mutual Information Transformer Regularization](https://github.com/ChrisWoo0443/hiva-ijca-mitr)** - 
- **[Content Manager](https://github.com/ChrisWoo0443/content_manager)** - 

---

### 🤝 Recent Contributions & PRs
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

### 🌐 Connect with Me
[<img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/chris-woo04)
[<img src="https://img.shields.io/badge/Resume-EB1919?style=for-the-badge&logo=read-the-docs&logoColor=white" />](YOUR_RESUME_LINK)

---

### 📊 GitHub Stats
<p align="center">
  <img src="https://streak-stats.demolab.com/?user=ChrisWoo0443&theme=radical&hide_border=true" alt="GitHub Streak" />
</p>

<p align="center">
  <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=ChrisWoo0443&layout=compact&theme=radical&hide_border=true" alt="Top Languages" />
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=ChrisWoo0443&theme=radical" alt="Language Stats Alternative" />
</p>
