🤖 AIDev Activity – Part 2
AI Coding Agent Collaboration Analysis

AIDev Activity – Part 2 is a large-scale empirical study analyzing how AI coding agents collaborate on GitHub.
It investigates acceptance behavior, review dynamics, and adoption trends across 859K+ AI-generated pull requests using the AIDev dataset.

📘 Mining Software Repositories – MSR 2026
👩‍💻 Author: Nouha Aouachri
📅 January 2026

📌 Project Overview

Most software engineering studies focus on human developers.
AIDev Activity – Part 2 shifts the focus to AI-generated pull requests, providing insights into how modern AI coding tools behave in real-world repositories.

The system leverages:

AIDev dataset (Hugging Face) for large-scale PR data 📦

Automated preprocessing & filtering of completed pull requests

Acceptance & review metrics to compare AI agents ✅

Statistical analysis to validate observed differences 📊

High-quality visualizations to reveal trends and patterns 📈

✨ Features

🤖 Multi-Agent Analysis – OpenAI Codex, Copilot, Cursor, Devin, Claude Code

✅ PR Acceptance Metrics – merged vs rejected pull requests

⏱️ Review & Closure Dynamics – time-to-close and review counts

📝 PR Description Analysis – impact of description length on acceptance

📈 Temporal Adoption Trends – monthly activity and agent dominance

📊 Statistical Validation – Chi-square and Kruskal–Wallis tests

🏗️ Analysis Pipeline

AIDev Dataset (Hugging Face)
↓
Data Filtering & Cleaning (Jan–Aug 2025)
↓
Metric Computation (Acceptance, Time-to-Close, Descriptions)
↓
Statistical Analysis
↓
Visualization & Insights

⚙️ Tech Stack

Language: Python 🐍

Data Processing: pandas, numpy

Statistics: scipy

Visualization: matplotlib, seaborn

Data Access: Hugging Face Datasets (Parquet)

Platform: GitHub & GitHub Pages

🚀 Getting Started
1️⃣ Clone the Repository
git clone https://github.com/NouhaAwachri/Mining-Software-Repositories-with-AIDev-dataset
cd Mining-Software-Repositories-with-AIDev-dataset

2️⃣ Install Dependencies
pip install pandas numpy matplotlib seaborn scipy pyarrow

3️⃣ Run the Analysis
python simple_aidev_analysis.py

📊 Output

📈 Statistical summaries printed in the console

📉 Publication-quality visualizations

📁 aidev_analysis_data.csv (859K+ pull requests)

⏱️ Expected runtime: < 5 minutes

⚠️ Limitations

Commit-level PR size metrics unavailable (missing PR linkage)

Comment data not directly linked to pull requests

Strong agent imbalance (OpenAI Codex ≈ 88.6%)

Correlational analysis only (no causal claims)

📊 Roadmap

✔️ Dataset loading & preprocessing

✔️ Acceptance and review metrics

✔️ Statistical testing

✔️ Visualization pipeline

⏳ Extended repository-level analysis

⏳ Cross-dataset validation

📚 References

AIDev Dataset Paper: https://arxiv.org/abs/2507.15003

Hugging Face Dataset: https://huggingface.co/datasets/hao-li/AIDev

MSR 2026 Challenge: https://2026.msrconf.org/track/msr-2026-mining-challenge

🧾 License & Usage

This project is intended for academic and research purposes under the MSR 2026 Mining Challenge.
Please cite the AIDev dataset and this repository when reusing results.
