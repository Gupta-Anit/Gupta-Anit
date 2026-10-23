<div align="center">

# Hey, I'm Anit Gupta 👋

### Senior Data Engineer @ Paramount+ · Attribution, Audience & Identity Data · GenAI Data Platforms

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=3584E4&center=true&vCenter=true&random=false&width=720&lines=45%2B+production+pipelines+%C2%B7+20TB%2B%2Fday;Kafka+%E2%86%92+Flink+%E2%86%92+Iceberg+%E2%86%92+Trino;Attribution+%C2%B7+Identity+%C2%B7+Audience+Data;GenAI+Data+Agents+%26+LLM+Pipelines" alt="Typing SVG" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anit-gupta/)
[![Portfolio](https://img.shields.io/badge/Portfolio-gupta--anit.github.io-2443D6?style=for-the-badge&logo=googlechrome&logoColor=white)](https://gupta-anit.github.io/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anitg.4@gmail.com)
[![Location](https://img.shields.io/badge/📍_Miami_·_Fort_Lauderdale_·_Remote-4285F4?style=for-the-badge)](https://www.linkedin.com/in/anit-gupta/)

</div>

---

## About me

I build data platforms that are reliable, cost-efficient, and ready for AI. At **Paramount+** I own **45+ production pipelines processing 20TB+ a day** for a streaming service with **80M+ subscribers**, covering subscriber, content, and marketing data.

- 🎯 **Marketing measurement:** attribution and media mix modeling (MMM) inputs that guide marketing spend
- 🪪 **Audience and identity data:** privacy-safe delivery to marketing and partner platforms, with identity resolution and consent enforcement
- 🔎 **Data quality and observability:** anomaly detection and alerting that **cut investigation time by 85%**
- 💸 **Warehouse cost governance:** query-level monitoring and spend attribution by team
- 🤖 **GenAI data foundations:** a semantic layer, guardrails, and evals for analytics agents, plus LLM pipelines that replace manual classification work

> *Pipelines should be boring. The insights they unlock shouldn't be.*

---

## Agentic and GenAI work

Agents are only as good as the data, definitions and checks behind them, so my GenAI work is mostly data work:

- 🧭 **Semantic and context layers:** governed metric definitions plus the business context (meaning, ownership, freshness, caveats) that analytics agents read before they query
- 📚 **Open Knowledge Format (Google OKF):** data knowledge as linked Markdown + YAML files, versioned in Git and served to agents
- 🛡️ **Guardrails and evals:** checks that stop agents from inventing numbers, and eval sets answers must pass before changes ship
- 🤝 **Data Engineering Agents:** a proof-of-concept multi-agent framework on **Google ADK** and **A2A** for pipeline building and data quality checks
- 🧩 **Skill files, LangGraph and LangChain:** reusable team know-how for agents, and stateful multi-step agent workflows
- 🎬 **LLM content-trait pipeline:** in-house **Gemini 2.5** pipeline generating content traits for ~10,000 titles, replacing a third-party vendor

---

## Featured project

### 🌊 [streamscope](https://github.com/Gupta-Anit/streamscope): real-time analytics on a lakehouse, exactly-once under failure

A streaming pipeline that ingests live Wikipedia edit events, computes 1-minute event-time windows in **Flink SQL**, and commits them to **Apache Iceberg** for SQL and time-travel queries in **Trino**. Everything runs locally with one `docker compose up`.

```mermaid
flowchart LR
    A[Wikimedia<br/>EventStreams] --> B[Python producer<br/>bot filter]
    B --> C[(Kafka<br/>KRaft)]
    C --> D[Flink SQL<br/>1-min windows<br/>30s watermark]
    D --> E[(Iceberg on MinIO<br/>hourly partitions)]
    E --> F[Trino<br/>SQL + time travel]
```

- **Exactly-once:** replayable Kafka offsets in Flink checkpoints, plus Iceberg commits only on checkpoint completion
- **Chaos-tested:** killed the TaskManager mid-stream, recovered from checkpoint, **0 duplicate windows** afterward
- **Documented trade-offs:** JSON vs Avro, Flink SQL vs the DataStream API, catalog choice, partitioning, and a scaling plan

---

## Tech stack

<div align="center">

**Streaming and processing**<br/>
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Flink](https://img.shields.io/badge/Apache_Flink-E6526F?style=flat-square&logo=apacheflink&logoColor=white)
![Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Beam](https://img.shields.io/badge/Apache_Beam-FF6600?style=flat-square&logo=apache&logoColor=white)
![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

**Lakehouse, warehouse and orchestration**<br/>
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white)
![Iceberg](https://img.shields.io/badge/Apache_Iceberg-1E88E5?style=flat-square&logo=apache&logoColor=white)
![Trino](https://img.shields.io/badge/Trino-DD00A1?style=flat-square&logo=trino&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694A?style=flat-square&logo=dbt&logoColor=white)

**Cloud and infrastructure**<br/>
![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_Certified-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Languages, ML and GenAI**<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Scala](https://img.shields.io/badge/Scala-DC322F?style=flat-square&logo=scala&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?style=flat-square&logo=google&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

</div>

---

## More projects

| Project | What it shows |
|---|---|
| 🎯 [attribution-lab](https://github.com/Gupta-Anit/attribution-lab) | Clickstream sessionization and **six attribution models** side by side (first, last, linear, time-decay, position-based, Markov chain) on DuckDB, with live-event promo campaigns |
| 📈 [mmm-input-pipeline](https://github.com/Gupta-Anit/mmm-input-pipeline) | Messy ad-platform exports to **model-ready MMM inputs**: data contracts, idempotent loads, invoice reconciliation, adstock and saturation features |
| 🚨 [dq-sentinel](https://github.com/Gupta-Anit/dq-sentinel) | **Data quality anomaly detection** with same-weekday robust baselines and root-cause ranking by dimension; Slack-ready alerts |
| 🌞 [SolarWind_Prediction](https://github.com/Gupta-Anit/SolarWind_Prediction) | ConvLSTM deep learning on heliospheric simulation data (Predictive Science Inc.). Reached **94% structural similarity**, beating the physics-simulation baseline; served via a real-time inference API on AWS SageMaker |
| 🛒 [HackGT 2019: Predictive Analytics for Store Managers](https://github.com/Gupta-Anit/Predictive-Analytical-tools-for-Store-Managers--HackGT-2019) | Time-series sales forecasting on real-time NCR retail data, **89% accuracy** |
| 📚 [LSTM Text Summarizer](https://github.com/Gupta-Anit/LSTM-TEXT-SUMMARIZER) | Sequence-to-sequence LSTM with attention for abstractive summarization |
| ⚡ [Apache Spark: Stack Overflow dataset](https://github.com/Gupta-Anit/Apache_Spark_Stack_overflow_dataset) | PySpark transformations and analysis on the Stack Overflow dataset |

---

## Career at a glance

| Years | Role | Company |
|---|---|---|
| 2023 to now | **Senior Data Engineer** | Paramount (Paramount+) |
| 2021 to 2023 | Data Engineer | Paramount |
| 2020 to 2021 | Data Science Researcher | Predictive Science Inc. / Georgia State Data Mining Lab |
| 2016 to 2019 | Associate Software Developer, then Data Analyst | Amdocs |

**Education:** M.S. Data Science & Analytics, Georgia State University (4.0 GPA) · MBA in Data-Driven Decision Making, Westcliff University (in progress) · B.Tech, Punjab Technical University

---

## Beyond code

🏎️ Formula 1 marshal (Miami GP, Las Vegas GP) · 📷 travel and motorsport photography · 🗺️ road trips with my dog Elsa

<div align="center">

**Open to conversations about** streaming architecture, attribution and identity data, and GenAI data platforms.

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anit-gupta/)
[![Email](https://img.shields.io/badge/Email_me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anitg.4@gmail.com)

![Profile views](https://komarev.com/ghpvc/?username=Gupta-Anit&color=blueviolet&style=flat-square)

</div>
