<div align="center">

<img src="./assets/header.svg" width="100%" alt="Shreya Roshan — AI Engineer"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&width=700&lines=Shipping+ML+systems+that+survive+production+%F0%9F%9A%80;Agents+that+show+their+evidence+%F0%9F%94%8E;RAG+with+citations+you+can+actually+check+%F0%9F%93%84;Computer+vision+for+healthcare+%F0%9F%A7%A0" alt="Typing intro"/>

<p>
  <a href="https://www.linkedin.com/in/shreya-roshan/"><img src="https://img.shields.io/badge/LinkedIn-Let's%20connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0d0221"/></a>
  <a href="https://github.com/Shreyro?tab=repositories"><img src="https://img.shields.io/badge/Repos-Explore-8b5cf6?style=for-the-badge&logo=github&logoColor=white&labelColor=0d0221"/></a>
  <a href="https://github.com/Shreyro?tab=followers"><img src="https://img.shields.io/github/followers/Shreyro?label=Followers&style=for-the-badge&color=22d3ee&labelColor=0d0221&logo=github"/></a>
  <img src="https://komarev.com/ghpvc/?username=Shreyro&label=Profile%20Views&color=c084fc&style=for-the-badge&labelColor=0d0221"/>
</p>

</div>

## ✦ About me

<table>
<tr>
<td width="58%" valign="top">

```python
class ShreyaRoshan:
    role    = "AI Engineer & Researcher"
    focus   = ["ML", "MLOps", "GenAI", "Medical Computer Vision"]
    mission = "Bridge experimental ML and production-grade engineering"

    def now(self):
        return [
            "🔨 Building automated MLOps infrastructure",
            "🔎 Making LLM agents traceable & grounded",
            "🩺 Applying deep learning to healthcare",
        ]

    def open_to(self):
        return ["AI/ML engineering roles", "research collabs",
                "chats about production ML ☕"]
```

</td>
<td width="42%" valign="top">

**🎯 What I care about**

- 🧪 **Reproducibility.** Every experiment is tracked and versioned.
- 🛡️ **Guardrails.** Validated SQL, verified citations, drift alerts.
- 📏 **Measurement.** If it isn't evaluated, it isn't done.
- 🚢 **Shipping.** Docker, CI/CD, APIs, not just notebooks.

</td>
</tr>
</table>

## ✦ Featured projects

<p align="center"><sub>👆 Click any card to open the repo · expand the sections below for the details</sub></p>

<p align="center">
  <a href="https://github.com/Shreyro/ModelForge"><img src="./assets/cards/modelforge.svg" width="49%" alt="ModelForge"/></a>
  <a href="https://github.com/Shreyro/Data_Detective"><img src="./assets/cards/datadetective.svg" width="49%" alt="Data Detective"/></a>
</p>
<p align="center">
  <a href="https://github.com/Shreyro/papertrail"><img src="./assets/cards/papertrail.svg" width="49%" alt="PaperTrail"/></a>
  <a href="https://github.com/Shreyro/Parkinson-s-MRI-Analysis"><img src="./assets/cards/parkinsons.svg" width="49%" alt="Parkinson's Detection"/></a>
</p>

<details>
<summary><b>⚡ ModelForge: how the MLOps pipeline fits together</b></summary>
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
- **Serving:** FastAPI with Pydantic validation and health-check probes, containerised with Docker
- **Monitoring:** automated Evidently AI data-drift reports

➡️ [View repo](https://github.com/Shreyro/ModelForge)
</details>

<details>
<summary><b>🔎 Data Detective: an analytics agent that shows its work</b></summary>
<br/>

Ask a business question in plain English. The agent writes **validated** SQL, runs it read-only on DuckDB, draws charts, and checks every number in its explanation against the query output.

```mermaid
flowchart LR
  Q[Question] --> B[Brain: Claude<br/>or offline rules]
  B -->|SQL| V[Validator<br/>sqlglot allow-list]
  V -->|rejected| B
  V -->|ok| X[(DuckDB<br/>read-only)]
  X --> Ev[Evidence E1…En]
  Ev --> N[Narrator]
  N --> G[Groundedness check]
  Ev --> C[Plotly charts]
```

- **Two brains, one interface:** works with Claude, or a deterministic offline brain, so CI needs no API key
- **Defence in depth:** SELECT-only, table allow-list, forced LIMIT, EXPLAIN bind-check, query timeout
- **Detective logic:** seasonally-adjusted anomaly detection that drills down to the root cause

➡️ [View repo](https://github.com/Shreyro/Data_Detective)
</details>

<details>
<summary><b>📄 PaperTrail: RAG you can audit</b></summary>
<br/>

Search research papers, ask questions and get **page-level citations**, with unsupported claims and wrong-page citations flagged.

```mermaid
flowchart LR
  PDF[Papers / arXiv] --> C[Page-aware<br/>chunks]
  C --> I[Hybrid index<br/>FAISS + BM25 + RRF]
  Q[Question] --> I
  I --> L[Claude answers<br/>with doc p.N cites]
  L --> V[Verifier<br/>claim-by-claim]
  V --> R[supported · partial ·<br/>unsupported · wrong page]
```

- **Hallucinated-citation guard:** every cited page is checked against what was actually retrieved
- **Claim verification:** each sentence is judged against its cited page, with a verbatim quote check
- **Evaluation:** retrieval quality, answer correctness and citation accuracy on a gold test set

➡️ [View repo](https://github.com/Shreyro/papertrail)
</details>

<details>
<summary><b>🧠 Parkinson's detection: MRI + spiral/wave analysis</b></summary>
<br/>

Two complementary approaches to early Parkinson's screening:

| Project | Approach | Repo |
|---|---|---|
| **MRI analysis** | Compares pretrained CNN architectures on MRI scans via transfer learning | [Parkinson-s-MRI-Analysis](https://github.com/Shreyro/Parkinson-s-MRI-Analysis) |
| **Spiral & wave test** | Classifies hand-drawn spirals/waves, served with an interactive Gradio interface | [Spiral-Wave-Parkinson-s](https://github.com/Shreyro/Spiral-Wave-Parkinson-s) |

</details>

<details>
<summary><b>🗂️ More projects</b></summary>
<br/>

| Project | What it is | Stack |
|---|---|---|
| [ShreyGPT](https://github.com/Shreyro/ShreyGPT) | Chatbot with an interactive interface | Python · LLMs |
| [NLP](https://github.com/Shreyro/NLP) | Collection of NLP projects | Jupyter · Transformers |
| [Machine-Vision](https://github.com/Shreyro/Machine-Vision) | Collection of computer-vision projects | Jupyter · OpenCV |
| [Spam-classification](https://github.com/Shreyro/Spam-classification) | Text classification for spam detection | scikit-learn |
| [portfolio-webpage](https://github.com/Shreyro/portfolio-webpage) | Personal portfolio site | HTML · CSS |

</details>

## ✦ Tech stack

<div align="center">

**🤖 ML & AI**<br/>
<img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,sklearn,opencv&theme=dark" />

**⚙️ Backend & MLOps**<br/>
<img src="https://skillicons.dev/icons?i=fastapi,flask,docker,githubactions,linux,git&theme=dark" />

**☁️ Cloud & Data**<br/>
<img src="https://skillicons.dev/icons?i=gcp,aws,azure,postgres,mysql,bigquery&theme=dark" />

**📊 Analytics & Web**<br/>
<img src="https://skillicons.dev/icons?i=powerbi,tableau,js,html,css,vscode&theme=dark" />

<br/>

![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?style=flat-square&logo=looker&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-F97316?style=flat-square&logo=gradio&logoColor=white)
![Claude](https://img.shields.io/badge/Claude%20API-D97757?style=flat-square&logo=anthropic&logoColor=white)

</div>

## ✦ GitHub activity

<div align="center">

<img src="https://github-readme-stats-fast.vercel.app/api?username=Shreyro&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true&bg_color=0d0221&title_color=c084fc&icon_color=22d3ee" height="170"/>
<img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=Shreyro&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d0221&title_color=c084fc" height="170"/>

<img src="https://streak-stats.demolab.com/?user=Shreyro&theme=tokyonight&hide_border=true&background=0d0221&ring=8b5cf6&fire=22d3ee&currStreakLabel=c084fc" width="70%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Shreyro&bg_color=0d0221&color=c084fc&line=8b5cf6&point=22d3ee&area=true&area_color=8b5cf6&hide_border=true" width="100%"/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake.svg"/>
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/Shreyro/Shreyro/output/github-contribution-grid-snake-dark.svg" width="100%"/>
</picture>

</div>

## ✦ Let's build something

<div align="center">

I'm open to **AI/ML engineering roles**, **research collaborations**, and conversations about **production ML**.

<a href="https://www.linkedin.com/in/shreya-roshan/"><img src="https://img.shields.io/badge/Say%20hi%20on%20LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://github.com/Shreyro"><img src="https://img.shields.io/badge/Follow%20on%20GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8b5cf6,50:3b82f6,100:22d3ee&height=110&section=footer" width="100%"/>

</div>
