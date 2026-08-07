<div align="center">

# Hosam Mahmoud Ibrahim

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=21&duration=3000&pause=900&color=5B8DEF&center=true&vCenter=true&width=700&height=48&lines=AI+Systems+Architect;Agentic+AI+%26+LLM+Engineer;Multi-agent+pipelines+%C2%B7+RAG+%C2%B7+Local+inference;Systems+that+run+with+no+external+APIs" alt="AI Systems Architect, Agentic AI and LLM Engineer" />

<br>

[![Book a call](https://img.shields.io/badge/Book_a_call-4372D4?style=for-the-badge&logo=calendly&logoColor=white)](https://calendly.com/sam_mahmoud)
[![Portfolio](https://img.shields.io/badge/Portfolio-121418?style=for-the-badge&logo=githubpages&logoColor=5B8DEF&labelColor=0B0C0E)](https://hosambadawi.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-121418?style=for-the-badge&logo=linkedin&logoColor=5B8DEF&labelColor=0B0C0E)](https://www.linkedin.com/in/hosam-mahmoud-ibrahim/)
[![Email](https://img.shields.io/badge/Email-121418?style=for-the-badge&logo=gmail&logoColor=5B8DEF&labelColor=0B0C0E)](mailto:hosam2mahmoud@gmail.com)

</div>

---

I design and ship **agentic AI systems** end to end: multi-agent pipelines, retrieval-augmented
generation, and self-hosted inference infrastructure. My open-source systems run entirely on
**local models**, with no external API dependency and no per-call vendor cost.

Currently architecting LLM-powered automation at **Capgemini**. M.Eng. in AI and Data Science,
University of Ottawa. AWS Certified Machine Learning Specialty.

```
Cairo, Egypt   ·   Open to AI architecture roles   ·   Arabic & English
```

---

## Flagship systems

### [Growth Engine](https://github.com/HosamBadawi/Growth-Engine) &nbsp;·&nbsp; nine-agent outbound automation

[![Stars](https://img.shields.io/github/stars/HosamBadawi/Growth-Engine?style=flat-square&color=121418&labelColor=0B0C0E&logo=github&logoColor=5B8DEF)](https://github.com/HosamBadawi/Growth-Engine/stargazers)
![Language](https://img.shields.io/github/languages/top/HosamBadawi/Growth-Engine?style=flat-square&color=121418&labelColor=0B0C0E)
![Code size](https://img.shields.io/github/languages/code-size/HosamBadawi/Growth-Engine?style=flat-square&color=121418&labelColor=0B0C0E)
![Last commit](https://img.shields.io/github/last-commit/HosamBadawi/Growth-Engine?style=flat-square&color=121418&labelColor=0B0C0E)

An autonomous B2B prospecting system. Nine specialised agents discover leads, research them, write
personalised outreach with a local LLM, send it under hard-coded deliverability rules, then watch
for replies and report on the funnel.

```
PROSPECTOR → ENRICHER → VERIFIER → RESEARCHER → WRITER
     → SENDER → REPLY WATCHER → REPORTER → DASHBOARD
```

Every stage is an independently testable unit passing state through a shared persistence layer.
The LLM layer is provider-agnostic with per-role model assignment, defaulting to local Ollama and
extending to OpenAI, Anthropic, Groq or any OpenAI-compatible endpoint, with daily caps and
automatic local fallback. Compliance is architectural, not bolted on: warm-up ramps, randomised
send jitter, restricted send windows, suppression lists, and a circuit breaker that halts a
campaign above a 3% bounce rate. Execution safety is three-tier, with two-key confirmation before
anything goes live.

`FastAPI` `APScheduler` `SQLAlchemy 2.0` `Alembic` `Ollama` `aiogram 3` `PostgreSQL` `Pytest`

### [YouTube Shorts Studio](https://github.com/HosamBadawi/Youtube-Shorts-Studio) &nbsp;·&nbsp; self-hosted multimodal video pipeline

[![Stars](https://img.shields.io/github/stars/HosamBadawi/Youtube-Shorts-Studio?style=flat-square&color=121418&labelColor=0B0C0E&logo=github&logoColor=5B8DEF)](https://github.com/HosamBadawi/Youtube-Shorts-Studio/stargazers)
![Language](https://img.shields.io/github/languages/top/HosamBadawi/Youtube-Shorts-Studio?style=flat-square&color=121418&labelColor=0B0C0E)
![Code size](https://img.shields.io/github/languages/code-size/HosamBadawi/Youtube-Shorts-Studio?style=flat-square&color=121418&labelColor=0B0C0E)
![Last commit](https://img.shields.io/github/last-commit/HosamBadawi/Youtube-Shorts-Studio?style=flat-square&color=121418&labelColor=0B0C0E)

Turns one long-form video into multiple publish-ready vertical Shorts, on hardware you already own.

```
INPUT → TRANSCRIBE → SEGMENT → MONTAGE → REFRAME
   → CAPTION → OVERLAY → METADATA → THUMBNAIL → UPLOAD
```

The interesting constraint was memory. Whisper, the LLM and the background-removal model all want
the GPU at once, so scheduling them through a shared VRAM budget lets the whole stack run on a
single 8 GB consumer card. The segmentation LLM returns sentence indices rather than timestamps,
which guarantees cuts land on semantic boundaries and removes the dominant failure mode of
timestamp-based approaches. Captions render right-to-left Arabic with word-level highlighting
synced to Whisper word timestamps.

`Whisper large-v3` `Ollama` `Command-R` `Qwen 2.5` `FastAPI` `OpenCV` `FFmpeg` `rembg` `yt-dlp`

### Multimodal Telegram AI Assistant &nbsp;·&nbsp; fully local, zero external APIs

A Dockerised assistant handling text conversation, image captioning, image transformation and
text-to-image generation entirely on local open-source models. n8n orchestrates the workflow and
PostgreSQL persists conversational memory, so context and personalisation survive across sessions.
Nothing leaves the machine, which makes it private by construction and free per message.

`LLaMA` `Gemma` `ComfyUI Flux` `n8n` `PostgreSQL` `Docker`

---

## Stack

<div align="center">

**Generative AI and LLMs**

![LLMs](https://img.shields.io/badge/LLMs-121418?style=flat-square&logoColor=5B8DEF&labelColor=0B0C0E)
![RAG](https://img.shields.io/badge/RAG-121418?style=flat-square&labelColor=0B0C0E)
![Ollama](https://img.shields.io/badge/Ollama-121418?style=flat-square&logo=ollama&logoColor=5B8DEF&labelColor=0B0C0E)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-121418?style=flat-square&logo=huggingface&logoColor=5B8DEF&labelColor=0B0C0E)
![QLoRA](https://img.shields.io/badge/QLoRA_%2F_LoRA_%2F_PEFT-121418?style=flat-square&labelColor=0B0C0E)
![Whisper](https://img.shields.io/badge/Whisper_large--v3-121418?style=flat-square&labelColor=0B0C0E)
![Vector DBs](https://img.shields.io/badge/Vector_databases-121418?style=flat-square&labelColor=0B0C0E)
![MCP](https://img.shields.io/badge/Model_Context_Protocol-121418?style=flat-square&labelColor=0B0C0E)

**Agentic systems and orchestration**

![LangChain](https://img.shields.io/badge/LangChain-121418?style=flat-square&logo=langchain&logoColor=5B8DEF&labelColor=0B0C0E)
![LangGraph](https://img.shields.io/badge/LangGraph-121418?style=flat-square&labelColor=0B0C0E)
![n8n](https://img.shields.io/badge/n8n-121418?style=flat-square&logo=n8n&logoColor=5B8DEF&labelColor=0B0C0E)
![Multi-agent](https://img.shields.io/badge/Multi--agent_pipelines-121418?style=flat-square&labelColor=0B0C0E)
![Tool calling](https://img.shields.io/badge/Tool_calling-121418?style=flat-square&labelColor=0B0C0E)
![Human in the loop](https://img.shields.io/badge/Human--in--the--loop-121418?style=flat-square&labelColor=0B0C0E)

**Infrastructure and MLOps**

![Docker](https://img.shields.io/badge/Docker-121418?style=flat-square&logo=docker&logoColor=5B8DEF&labelColor=0B0C0E)
![FastAPI](https://img.shields.io/badge/FastAPI-121418?style=flat-square&logo=fastapi&logoColor=5B8DEF&labelColor=0B0C0E)
![AWS](https://img.shields.io/badge/AWS-121418?style=flat-square&logo=amazonwebservices&logoColor=5B8DEF&labelColor=0B0C0E)
![Azure](https://img.shields.io/badge/Azure-121418?style=flat-square&logo=microsoftazure&logoColor=5B8DEF&labelColor=0B0C0E)
![Git](https://img.shields.io/badge/Git-121418?style=flat-square&logo=git&logoColor=5B8DEF&labelColor=0B0C0E)
![Pytest](https://img.shields.io/badge/Pytest-121418?style=flat-square&logo=pytest&logoColor=5B8DEF&labelColor=0B0C0E)
![CI/CD](https://img.shields.io/badge/CI%2FCD-121418?style=flat-square&logo=githubactions&logoColor=5B8DEF&labelColor=0B0C0E)

**Data and analytics**

![Python](https://img.shields.io/badge/Python-121418?style=flat-square&logo=python&logoColor=5B8DEF&labelColor=0B0C0E)
![SQL](https://img.shields.io/badge/SQL-121418?style=flat-square&logo=postgresql&logoColor=5B8DEF&labelColor=0B0C0E)
![R](https://img.shields.io/badge/R-121418?style=flat-square&logo=r&logoColor=5B8DEF&labelColor=0B0C0E)
![Scala](https://img.shields.io/badge/Scala-121418?style=flat-square&logo=scala&logoColor=5B8DEF&labelColor=0B0C0E)
![PyTorch](https://img.shields.io/badge/PyTorch-121418?style=flat-square&logo=pytorch&logoColor=5B8DEF&labelColor=0B0C0E)
![TensorFlow](https://img.shields.io/badge/TensorFlow-121418?style=flat-square&logo=tensorflow&logoColor=5B8DEF&labelColor=0B0C0E)
![Spark](https://img.shields.io/badge/Apache_Spark-121418?style=flat-square&logo=apachespark&logoColor=5B8DEF&labelColor=0B0C0E)
![Kafka](https://img.shields.io/badge/Apache_Kafka-121418?style=flat-square&logo=apachekafka&logoColor=5B8DEF&labelColor=0B0C0E)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-121418?style=flat-square&logo=postgresql&logoColor=5B8DEF&labelColor=0B0C0E)
![Power BI](https://img.shields.io/badge/Power_BI-121418?style=flat-square&logo=powerbi&logoColor=5B8DEF&labelColor=0B0C0E)

</div>

---

## GitHub

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=HosamBadawi&theme=github_dark" width="100%" alt="Profile summary" />

<img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=HosamBadawi&theme=github_dark" height="200" alt="Contribution stats" />
<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=HosamBadawi&theme=github_dark&utcOffset=3" height="200" alt="Most productive time of day" />

<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=HosamBadawi&theme=github_dark" height="200" alt="Repositories per language" />
<img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=HosamBadawi&theme=github_dark" height="200" alt="Most committed language" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=HosamBadawi&bg_color=121418&color=E9EBEE&line=5B8DEF&point=E9EBEE&area=true&area_color=5B8DEF&title_color=5B8DEF&border_color=22262D&custom_title=Contribution%20activity&radius=14&height=300" alt="Contribution activity graph" />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/HosamBadawi/HosamBadawi/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/HosamBadawi/HosamBadawi/output/github-contribution-grid-snake.svg">
  <img alt="Contribution grid snake animation" src="https://raw.githubusercontent.com/HosamBadawi/HosamBadawi/output/github-contribution-grid-snake.svg">
</picture>

</div>

---

## Research and engineering archive

Thirteen repositories from my M.Eng. and undergraduate work, each pairing the source code with the
reports, papers and presentations that document it.

| Repository | What it covers |
|---|---|
| [AI-For-Cybersecurity](https://github.com/HosamBadawi/AI-For-Cybersecurity) | CT-GAN intrusion detection, Kafka model streaming, DCGAN anomaly detection |
| [Language-Identification-System](https://github.com/HosamBadawi/Language-Identification-System) | Seven-language speech ID: dataset pipeline, MFCC/Mel modelling, Flask deployment |
| [Smart-Cities-Simulation](https://github.com/HosamBadawi/Smart-Cities-Simulation) | Crowdsensing pipeline: task generation, CGAN synthesis, anomaly detection, ns-3 |
| [NLP-Projects](https://github.com/HosamBadawi/NLP-Projects) | Authorship attribution, book clustering, ontology-driven chatbot |
| [Big-Data-Spark](https://github.com/HosamBadawi/Big-Data-Spark) | Distributed processing in Scala, PySpark and Spark SQL with streaming jobs |
| [Computer-Vision](https://github.com/HosamBadawi/Computer-Vision) | Transfer-learning classification plus KNN and filters built from scratch |
| [Machine-Learning-From-Scratch](https://github.com/HosamBadawi/Machine-Learning-From-Scratch) | Decision trees, boosting, KNN and OVR/OVO from first principles |
| [Data-Science-Analytics](https://github.com/HosamBadawi/Data-Science-Analytics) | Sentiment-driven price prediction, churn analysis in R, SQL analytics |
| [Deep-Learning](https://github.com/HosamBadawi/Deep-Learning) | Neural architectures on the UNR-IDD intrusion detection dataset |
| [Azure-Synapse-Streaming](https://github.com/HosamBadawi/Azure-Synapse-Streaming) | Cloud warehousing and real-time event processing on Azure |
| [Reinforcement-Learning-Projects](https://github.com/HosamBadawi/Reinforcement-Learning-Projects) | Agent trained to drive through environment interaction |
| [Social-Media-Scraper](https://github.com/HosamBadawi/Social-Media-Scraper) | Batch-downloads 100+ videos per run with automatic trimming |
| [Mongodb-Cassandra](https://github.com/HosamBadawi/Mongodb-Cassandra) | Document versus wide-column NoSQL data modelling |

---

## Experience

**AI and Automation Engineer** &nbsp;·&nbsp; Capgemini &nbsp;·&nbsp; 09/2025 to Present

Architect and deploy end-to-end AI automation systems connecting multiple business applications,
replacing manual processes with orchestrated, monitored pipelines. Design intelligent chatbots and
voice assistants for client-facing platforms, owning conversational flow, state handling and
interaction models. Integrate LLMs into chatbot architectures to improve contextual understanding
and grounding across multi-turn conversations. Maintain development, staging and production
environments, and author the technical documentation and workflow architecture diagrams that
enable handover and reuse.

**Data Analyst** &nbsp;·&nbsp; Capgemini &nbsp;·&nbsp; 06/2023 to 09/2025

Automated recurring manual Excel reporting with Python, reducing a six-hour process to seconds.
Developed SQL database solutions powering real-time Power BI dashboards, and analysed
heterogeneous data sources to surface the patterns, trends and anomalies behind data-driven
business strategy.

---

## Education and certifications

**M.Eng. Artificial Intelligence and Data Science** &nbsp;·&nbsp; University of Ottawa, Canada &nbsp;·&nbsp; 02/2022 to 02/2023 &nbsp;·&nbsp; Grade: Excellent

**B.Sc. Computer Science** &nbsp;·&nbsp; Misr University for Science and Technology &nbsp;·&nbsp; 09/2017 to 07/2021 &nbsp;·&nbsp; GPA 3.80 / 4.00

- **[AWS Certified Machine Learning Specialty](https://www.credly.com/badges/a1c5a87d-1286-436a-b2d9-20ee1e112e39/public_url)** &nbsp;·&nbsp; Amazon Web Services, May 2022
- **[AWS Certified Cloud Practitioner](https://www.credly.com/badges/462ad198-987b-40a2-94b1-7d13e44aa753/public_url)** &nbsp;·&nbsp; Amazon Web Services, February 2022
- **[Microsoft Power BI](https://drive.google.com/file/d/1tPefEymc6z444vzSek_xYKf08NnDO3Ex/view?usp=drive_link)** &nbsp;·&nbsp; October 2023
- **[Leadership and Management](https://drive.google.com/file/d/1NljrdlXeGmlDQW4HCRITsIG5lrjOD_mG/view)** &nbsp;·&nbsp; Dale Carnegie, May 2022

---

<div align="center">

## Let's talk about your AI systems

Scoping an agentic architecture, moving an LLM prototype into production, or cutting inference
cost by self-hosting. Pick a slot and let's get into it.

[![Book a call](https://img.shields.io/badge/Book_a_30--min_call-4372D4?style=for-the-badge&logo=calendly&logoColor=white)](https://calendly.com/sam_mahmoud)
[![Portfolio](https://img.shields.io/badge/hosambadawi.github.io-121418?style=for-the-badge&logo=githubpages&logoColor=5B8DEF&labelColor=0B0C0E)](https://hosambadawi.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-121418?style=for-the-badge&logo=linkedin&logoColor=5B8DEF&labelColor=0B0C0E)](https://www.linkedin.com/in/hosam-mahmoud-ibrahim/)
[![Email](https://img.shields.io/badge/hosam2mahmoud@gmail.com-121418?style=for-the-badge&logo=gmail&logoColor=5B8DEF&labelColor=0B0C0E)](mailto:hosam2mahmoud@gmail.com)

<br>

![Profile views](https://komarev.com/ghpvc/?username=HosamBadawi&color=4372D4&style=for-the-badge&label=PROFILE+VIEWS)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B0C0E,60:22345E,100:4372D4&height=110&section=footer" width="100%" alt="" />

</div>
