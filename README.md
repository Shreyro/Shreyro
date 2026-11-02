<div align="center">

<img src="./assets/header-sakura.svg" width="100%" alt="Shreya Roshan: AI Engineer, Machine Learning, Data Science"/>

<img src="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=20&duration=3000&pause=1000&color=F184D7&center=true&vCenter=true&width=720&lines=Turning+raw+data+into+decisions;Training+models+that+hold+up+in+production;Building+LLM+systems+you+can+verify;From+notebook+to+monitored+service" alt="Typing summary"/>

<p>
  <a href="https://www.linkedin.com/in/shreya-roshan/"><img src="https://img.shields.io/badge/LinkedIn-Connect-e86dcd?style=flat-square&logo=linkedin&logoColor=white&labelColor=252638"/></a>
  <a href="https://github.com/Shreyro?tab=repositories"><img src="https://img.shields.io/badge/Repositories-Explore-ac4cad?style=flat-square&logo=github&logoColor=white&labelColor=252638"/></a>
  <img src="https://img.shields.io/badge/Open%20to-AI%20%2F%20ML%20%2F%20Data%20roles-8a489a?style=flat-square&labelColor=252638"/>
  <img src="https://komarev.com/ghpvc/?username=Shreyro&label=Profile%20views&color=684180&style=flat-square&labelColor=252638"/>
</p>

</div>

### About me

I'm an AI/ML engineer and data scientist who cares about the part after the notebook: making models **measurable, reproducible and trustworthy** once they meet real data. My work spans classical ML and statistics, deep learning for medical imaging, and LLM applications that cite their evidence.

- 🌸 **Currently:** building automated MLOps infrastructure and evidence-grounded LLM agents
- 🩺 **Research interest:** healthcare AI, including MRI-based Parkinson's detection
- 💬 **Open to:** AI/ML engineering, data science and applied research roles

<div align="center"><img src="./assets/divider-sakura.svg" width="100%"/></div>

### What I do

<div align="center">
<img src="./assets/pillars.svg" width="100%" alt="Data Science, Machine Learning, and AI and GenAI capabilities"/>
</div>

<div align="center"><img src="./assets/divider-sakura.svg" width="100%"/></div>

### Featured projects

<sub>Click a card to open the repository. Expand the sections below for architecture and details.</sub>

<p align="center">
  <a href="https://github.com/Shreyro/ModelForge"><img src="./assets/projects/modelforge.svg" width="49%" alt="ModelForge: MLOps platform"/></a>
  <a href="https://github.com/Shreyro/Data_Detective"><img src="./assets/projects/datadetective.svg" width="49%" alt="Data Detective: analytics agent"/></a>
</p>
<p align="center">
  <a href="https://github.com/Shreyro/papertrail"><img src="./assets/projects/papertrail.svg" width="49%" alt="PaperTrail: RAG research assistant"/></a>
  <a href="https://github.com/Shreyro/Parkinson-s-MRI-Analysis"><img src="./assets/projects/parkinsons.svg" width="49%" alt="Parkinson's detection: medical computer vision"/></a>
</p>

<details>
<summary><b>ModelForge: how the MLOps pipeline fits together</b></summary>
<br/>

A modular platform that trains, evaluates, versions, serves and monitors models, demonstrated on the Breast Cancer Wisconsin dataset.

```mermaid
flowchart LR
  D[(Dataset)] --> P[Leakage-free<br/>pipeline]
  P --> T[Train + tune]
  T -->|metrics & artifacts| M[(MLflow)]
  M --> A[FastAPI<br/>inference]
  A --> E[Evidently<br/>drift reports]
  E -.->|retrain signal| T
  G[GitHub Actions] -.->|pytest on every push| P
```

- **Leakage-free data:** stratified splits, scalers fitted only on training data
- **Experiment tracking:** ROC-AUC, precision and recall logged and versioned in MLflow
- **Serving:** FastAPI with Pydantic validation and health probes, containerised with Docker
- **Monitoring:** automated Evidently AI data-drift reports
</details>

<details>
<summary><b>Data Detective: an analytics agent that shows its work</b></summary>
<br/>

Ask a business question in plain English. The agent writes **validated** SQL, runs it read-only on DuckDB, draws charts, and checks every number in its explanation against the query output.

```mermaid
flowchart LR
  Q[Question] --> B[Planner: LLM<br/>or offline rules]
  B -->|SQL| V[Validator<br/>sqlglot allow-list]
  V -->|rejected| B
  V -->|ok| X[(DuckDB<br/>read-only)]
  X --> Ev[Evidence E1…En]
  Ev --> N[Narrator]
  N --> G[Groundedness check]
  Ev --> C[Plotly charts]
```

- **Two modes, one interface:** LLM-planned or deterministic offline, so CI needs no API key
- **Defence in depth:** SELECT-only, table allow-list, forced LIMIT, EXPLAIN bind-check, query timeout
- **Root-cause analysis:** seasonally adjusted anomaly detection that drills down by channel and region
</details>

<details>
<summary><b>PaperTrail: retrieval-augmented generation you can audit</b></summary>
<br/>

Search research papers, ask questions and get **page-level citations**, with unsupported claims and wrong-page citations flagged.

```mermaid
flowchart LR
  PDF[Papers / arXiv] --> C[Page-aware<br/>chunks]
  C --> I[Hybrid index<br/>FAISS + BM25 + RRF]
  Q[Question] --> I
  I --> L[LLM answers<br/>with page citations]
  L --> V[Verifier<br/>claim-by-claim]
  V --> R[supported · partial ·<br/>unsupported · wrong page]
```

- **Hallucinated-citation guard:** every cited page is checked against what was actually retrieved
- **Claim verification:** each sentence is judged against its cited page, with a verbatim quote check
- **Evaluation:** retrieval quality, answer correctness and citation accuracy on a gold test set
</details>

<details>
<summary><b>Parkinson's detection: MRI and spiral/wave analysis</b></summary>
<br/>

| Project | Approach |
|---|---|
| [MRI analysis](https://github.com/Shreyro/Parkinson-s-MRI-Analysis) | Compares pretrained CNN architectures on MRI scans using transfer learning |
| [Spiral & wave test](https://github.com/Shreyro/Spiral-Wave-Parkinson-s) | Classifies hand-drawn spirals and waves, served through an interactive Gradio app |

</details>

<details>
<summary><b>More projects</b></summary>
<br/>

| Project | Description |
|---|---|
| [ShreyGPT](https://github.com/Shreyro/ShreyGPT) | Chatbot with an interactive interface |
| [NLP](https://github.com/Shreyro/NLP) | Natural language processing projects |
| [Machine-Vision](https://github.com/Shreyro/Machine-Vision) | Computer vision projects |
| [Spam-classification](https://github.com/Shreyro/Spam-classification) | Text classification for spam detection |

</details>

<div align="center"><img src="./assets/divider-sakura.svg" width="100%"/></div>

### Tech stack

<div align="center">

<sub><b>MACHINE LEARNING & AI</b></sub><br/>
<img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,sklearn,opencv&theme=dark"/>

<sub><b>DATA</b></sub><br/>
<img src="https://skillicons.dev/icons?i=postgres,mysql,bigquery,powerbi,tableau&theme=dark"/>

<sub><b>MLOPS & ENGINEERING</b></sub><br/>
<img src="https://skillicons.dev/icons?i=fastapi,flask,docker,githubactions,linux,git&theme=dark"/>

<sub><b>CLOUD</b></sub><br/>
<img src="https://skillicons.dev/icons?i=gcp,aws,azure&theme=dark"/>

<br/>

![pandas](https://img.shields.io/badge/pandas-252638?style=flat-square&logo=pandas&logoColor=f184d7)
![NumPy](https://img.shields.io/badge/NumPy-252638?style=flat-square&logo=numpy&logoColor=f184d7)
![MLflow](https://img.shields.io/badge/MLflow-252638?style=flat-square&logo=mlflow&logoColor=f184d7)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-252638?style=flat-square&logo=huggingface&logoColor=f184d7)
![Databricks](https://img.shields.io/badge/Databricks-252638?style=flat-square&logo=databricks&logoColor=f184d7)
![DuckDB](https://img.shields.io/badge/DuckDB-252638?style=flat-square&logo=duckdb&logoColor=f184d7)
![Plotly](https://img.shields.io/badge/Plotly-252638?style=flat-square&logo=plotly&logoColor=f184d7)
![Streamlit](https://img.shields.io/badge/Streamlit-252638?style=flat-square&logo=streamlit&logoColor=f184d7)
![Gradio](https://img.shields.io/badge/Gradio-252638?style=flat-square&logo=gradio&logoColor=f184d7)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-252638?style=flat-square&logo=looker&logoColor=f184d7)

</div>

<div align="center"><img src="./assets/divider-sakura.svg" width="100%"/></div>

### GitHub activity

<div align="center">

<img src="https://github-readme-stats-fast.vercel.app/api?username=Shreyro&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&bg_color=1d212a&title_color=f184d7&icon_color=e86dcd&text_color=ece4f3&ring_color=d152bd" height="170"/>
<img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=Shreyro&layout=compact&hide_border=true&bg_color=1d212a&title_color=f184d7&text_color=ece4f3" height="170"/>

<img src="https://streak-stats.demolab.com/?user=Shreyro&hide_border=true&background=1d212a&ring=d152bd&fire=f184d7&currStreakNum=ece4f3&sideNums=ece4f3&currStreakLabel=f184d7&sideLabels=b9a9c9&dates=b9a9c9&stroke=403256" width="72%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Shreyro&bg_color=1d212a&color=ece4f3&title_color=f184d7&line=d152bd&point=f184d7&area=true&area_color=8a489a&hide_border=true" width="100%"/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake.svg"/>
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg" width="100%"/>
</picture>

<br/><br/>

<a href="https://www.linkedin.com/in/shreya-roshan/"><img src="./assets/footer.svg" width="100%" alt="Let's build something together. Connect on LinkedIn"/></a>

</div>
