<div align="center">

<img src="./assets/header.svg" width="100%" alt="System notice: a new Player has awakened. Shreya Roshan, AI Engineer, Data Scientist and ML Researcher"/>

<img src="https://readme-typing-svg.demolab.com?font=Cinzel&weight=700&size=22&duration=2600&pause=1000&color=E9B949&center=true&vCenter=true&width=760&lines=Arise.+Train.+Evaluate.+Deploy.;From+raw+data+to+production+decisions;Machine+Learning+%E2%80%A2+Data+Science+%E2%80%A2+GenAI;Every+claim+traced.+Every+model+tracked." alt="Arise. Train. Evaluate. Deploy."/>

<p>
  <a href="https://www.linkedin.com/in/shreya-roshan/"><img src="https://img.shields.io/badge/LinkedIn-Send%20a%20raven-4cc3ff?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=05060d"/></a>
  <img src="https://img.shields.io/badge/Status-Open%20to%20AI%2FML%20roles-5eead4?style=for-the-badge&logo=target&logoColor=white&labelColor=05060d"/>
  <a href="https://github.com/Shreyro?tab=repositories"><img src="https://img.shields.io/badge/Repos-Enter%20the%20archive-e9b949?style=for-the-badge&logo=github&logoColor=white&labelColor=05060d"/></a>
  <img src="https://komarev.com/ghpvc/?username=Shreyro&label=Visitors&color=8b5cf6&style=for-the-badge&labelColor=05060d"/>
</p>

<img src="./assets/divider.svg" width="100%"/>

</div>

## ⚜️ The Status Window
<sub>About me</sub>

<div align="center">
<img src="./assets/status.svg" width="100%" alt="Status window: Shreya Roshan, AI/ML Engineer and Data Scientist. Abilities: Machine Learning, Data Science & Analytics, MLOps, GenAI, Computer Vision, Data Engineering"/>
</div>

<details open>
<summary><b>📜 The recruiter's scroll (30-second summary)</b></summary>
<br/>

| | |
|---|---|
| **Role** | AI / ML Engineer · Data Scientist · ML Researcher |
| **Core strengths** | Predictive modelling, deep learning, statistical analysis, LLM systems (RAG and agents), MLOps |
| **What sets me apart** | I build ML that is *measurable and trustworthy*: tracked experiments, validated SQL, cited answers, drift monitoring and CI-tested pipelines |
| **Domains** | Healthcare AI (MRI analysis, Parkinson's screening), business analytics, research tooling |
| **Currently** | Building automated MLOps infrastructure and evidence-grounded LLM agents |
| **Looking for** | AI/ML engineering, data science and applied research roles, plus research collaborations |

</details>

<div align="center"><img src="./assets/divider.svg" width="100%"/></div>

## ⚔️ Cleared Gates
<sub>Featured projects · click a gate to enter the repo, open the scrolls below for the architecture</sub>

<p align="center">
  <a href="https://github.com/Shreyro/ModelForge"><img src="./assets/gates/gate-modelforge.svg" width="49%" alt="ModelForge: end-to-end MLOps platform"/></a>
  <a href="https://github.com/Shreyro/Data_Detective"><img src="./assets/gates/gate-datadetective.svg" width="49%" alt="Data Detective: autonomous analytics agent"/></a>
</p>
<p align="center">
  <a href="https://github.com/Shreyro/papertrail"><img src="./assets/gates/gate-papertrail.svg" width="49%" alt="PaperTrail: evidence-first research assistant"/></a>
  <a href="https://github.com/Shreyro/Parkinson-s-MRI-Analysis"><img src="./assets/gates/gate-parkinsons.svg" width="49%" alt="Parkinson's detection: medical computer vision"/></a>
</p>

<details>
<summary><b>🗡️ ModelForge: the MLOps forge</b></summary>
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
- **Experiment tracking:** ROC-AUC / precision / recall logged and versioned in MLflow
- **Serving:** FastAPI with Pydantic validation and health probes, containerised with Docker
- **Monitoring:** automated Evidently AI data-drift reports

➡️ [Enter the gate](https://github.com/Shreyro/ModelForge)
</details>

<details>
<summary><b>🔎 Data Detective: the analyst who never lies</b></summary>
<br/>

Ask a business question in plain English. The agent writes **validated** SQL, runs it read-only on DuckDB, draws charts, and checks every number in its explanation against the query output.

```mermaid
flowchart LR
  Q[Question] --> B[Brain: LLM<br/>or offline rules]
  B -->|SQL| V[Validator<br/>sqlglot allow-list]
  V -->|rejected| B
  V -->|ok| X[(DuckDB<br/>read-only)]
  X --> Ev[Evidence E1…En]
  Ev --> N[Narrator]
  N --> G[Groundedness check]
  Ev --> C[Plotly charts]
```

- **Two brains, one interface:** LLM-planned or deterministic offline mode, so CI needs no API key
- **Defence in depth:** SELECT-only, table allow-list, forced LIMIT, EXPLAIN bind-check, query timeout
- **Detective logic:** seasonally-adjusted anomaly detection that drills down to the root cause

➡️ [Enter the gate](https://github.com/Shreyro/Data_Detective)
</details>

<details>
<summary><b>📖 PaperTrail: the archive that cites its sources</b></summary>
<br/>

Search research papers, ask questions and get **page-level citations**, with unsupported claims and wrong-page citations flagged.

```mermaid
flowchart LR
  PDF[Papers / arXiv] --> C[Page-aware<br/>chunks]
  C --> I[Hybrid index<br/>FAISS + BM25 + RRF]
  Q[Question] --> I
  I --> L[LLM answers<br/>with doc p.N cites]
  L --> V[Verifier<br/>claim-by-claim]
  V --> R[supported · partial ·<br/>unsupported · wrong page]
```

- **Hallucinated-citation guard:** every cited page is checked against what was actually retrieved
- **Claim verification:** each sentence is judged against its cited page, with a verbatim quote check
- **Evaluation:** retrieval quality, answer correctness and citation accuracy on a gold test set

➡️ [Enter the gate](https://github.com/Shreyro/papertrail)
</details>

<details>
<summary><b>🩺 Parkinson's detection: the healer's gate</b></summary>
<br/>

Two complementary approaches to early Parkinson's screening:

| Project | Approach | Repo |
|---|---|---|
| **MRI analysis** | Compares pretrained CNN architectures on MRI scans via transfer learning | [Parkinson-s-MRI-Analysis](https://github.com/Shreyro/Parkinson-s-MRI-Analysis) |
| **Spiral & wave test** | Classifies hand-drawn spirals/waves, served with an interactive Gradio interface | [Spiral-Wave-Parkinson-s](https://github.com/Shreyro/Spiral-Wave-Parkinson-s) |

</details>

<details>
<summary><b>🗝️ Lesser dungeons: more projects</b></summary>
<br/>

| Project | What it is | Stack |
|---|---|---|
| [ShreyGPT](https://github.com/Shreyro/ShreyGPT) | Chatbot with an interactive interface | Python · LLMs |
| [NLP](https://github.com/Shreyro/NLP) | Collection of NLP projects | Jupyter · Transformers |
| [Machine-Vision](https://github.com/Shreyro/Machine-Vision) | Collection of computer-vision projects | Jupyter · OpenCV |
| [Spam-classification](https://github.com/Shreyro/Spam-classification) | Text classification for spam detection | scikit-learn |
| [portfolio-webpage](https://github.com/Shreyro/portfolio-webpage) | Personal portfolio site | HTML · CSS |

</details>

<div align="center"><img src="./assets/divider.svg" width="100%"/></div>

## 🔮 Skill Tree
<sub>Data science, AI and ML capabilities, each backed by a project</sub>

| Ability | What I do | Proof |
|---|---|---|
| 📊 **Data Science & Analytics** | EDA, statistical analysis, anomaly detection, KPI and root-cause analysis, dashboards | [Data Detective](https://github.com/Shreyro/Data_Detective) |
| 🧠 **Machine Learning** | Feature engineering, classification and regression, model comparison, leakage-free validation | [ModelForge](https://github.com/Shreyro/ModelForge) · [Spam-classification](https://github.com/Shreyro/Spam-classification) |
| 👁️ **Deep Learning & Vision** | CNNs, transfer learning, medical imaging, OpenCV | [Parkinson's MRI](https://github.com/Shreyro/Parkinson-s-MRI-Analysis) · [Machine-Vision](https://github.com/Shreyro/Machine-Vision) |
| ✨ **GenAI & LLMs** | RAG, hybrid retrieval, tool-using agents, LLM evaluation and grounding checks | [PaperTrail](https://github.com/Shreyro/papertrail) · [Data Detective](https://github.com/Shreyro/Data_Detective) |
| 💬 **NLP** | Text classification, embeddings, conversational interfaces | [NLP](https://github.com/Shreyro/NLP) · [ShreyGPT](https://github.com/Shreyro/ShreyGPT) |
| ⚙️ **MLOps & Engineering** | Experiment tracking, model serving, drift monitoring, Docker, CI/CD, testing | [ModelForge](https://github.com/Shreyro/ModelForge) |

## 🐉 The Rider's Armory
<sub>Tech stack</sub>

<div align="center">

**🧠 ML & Deep Learning**<br/>
<img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,sklearn,opencv&theme=dark" />

**📊 Data & Analytics**<br/>
<img src="https://skillicons.dev/icons?i=postgres,mysql,bigquery,powerbi,tableau&theme=dark" />

**⚙️ MLOps & Backend**<br/>
<img src="https://skillicons.dev/icons?i=fastapi,flask,docker,githubactions,linux,git&theme=dark" />

**☁️ Cloud**<br/>
<img src="https://skillicons.dev/icons?i=gcp,aws,azure&theme=dark" />

<br/>

![Pandas](https://img.shields.io/badge/Pandas-05060d?style=flat-square&logo=pandas&logoColor=4cc3ff)
![NumPy](https://img.shields.io/badge/NumPy-05060d?style=flat-square&logo=numpy&logoColor=4cc3ff)
![MLflow](https://img.shields.io/badge/MLflow-05060d?style=flat-square&logo=mlflow&logoColor=4cc3ff)
![Databricks](https://img.shields.io/badge/Databricks-05060d?style=flat-square&logo=databricks&logoColor=e9b949)
![DuckDB](https://img.shields.io/badge/DuckDB-05060d?style=flat-square&logo=duckdb&logoColor=e9b949)
![Plotly](https://img.shields.io/badge/Plotly-05060d?style=flat-square&logo=plotly&logoColor=e9b949)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-05060d?style=flat-square&logo=looker&logoColor=e9b949)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-05060d?style=flat-square&logo=huggingface&logoColor=8b5cf6)
![LLM APIs](https://img.shields.io/badge/LLM%20APIs-05060d?style=flat-square&logo=openai&logoColor=8b5cf6)
![Streamlit](https://img.shields.io/badge/Streamlit-05060d?style=flat-square&logo=streamlit&logoColor=8b5cf6)
![Gradio](https://img.shields.io/badge/Gradio-05060d?style=flat-square&logo=gradio&logoColor=8b5cf6)

</div>

<div align="center"><img src="./assets/divider.svg" width="100%"/></div>

## 🏰 Training Grounds
<sub>GitHub activity</sub>

<div align="center">

<img src="https://github-readme-stats-fast.vercel.app/api?username=Shreyro&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&bg_color=05060d&title_color=e9b949&icon_color=4cc3ff&text_color=d6e4f5&ring_color=e9b949" height="170"/>
<img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=Shreyro&layout=compact&hide_border=true&bg_color=05060d&title_color=e9b949&text_color=d6e4f5" height="170"/>

<img src="https://streak-stats.demolab.com/?user=Shreyro&hide_border=true&background=05060d&ring=e9b949&fire=4cc3ff&currStreakNum=d6e4f5&sideNums=d6e4f5&currStreakLabel=e9b949&sideLabels=7f93b3&dates=7f93b3&stroke=1a2340" width="72%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Shreyro&bg_color=05060d&color=d6e4f5&title_color=e9b949&line=4cc3ff&point=e9b949&area=true&area_color=4cc3ff&hide_border=true" width="100%"/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake.svg"/>
  <img alt="Contribution graph being devoured" src="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg" width="100%"/>
</picture>

</div>

<div align="center">

<br/>

<a href="https://www.linkedin.com/in/shreya-roshan/"><img src="./assets/quest.svg" width="100%" alt="New quest: Recruit the Player. Accept by messaging on LinkedIn"/></a>

<sub>⚜️ Accept the quest: click it to message me on LinkedIn ⚜️</sub>

</div>
