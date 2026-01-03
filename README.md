AIDev Activity 
Implementation and Analysis of AI Coding Agent Collaboration

📘 Mining Software Repositories – MSR 2026
👩‍💻 Author: Nouha Aouachri
📅 Date: January 3, 2026

📌 Project Overview

This project presents the implementation and analysis of AIDev Activity , a large-scale empirical study investigating AI coding agent collaboration patterns using the AIDev dataset.

The analysis covers 859,377 AI-generated GitHub pull requests created between January and August 2025 by five AI coding agents, with a focus on:

Pull request acceptance behavior

Review and closure dynamics

Impact of pull request description length

Temporal adoption trends of AI coding agents

The project follows a fully reproducible data science pipeline, including dataset loading, metric computation, statistical testing, and visualization.

🎯 Research Questions

RQ1
Do AI coding agents differ in pull request acceptance rates and review dynamics?

RQ2
How do pull request characteristics (e.g., description length) affect acceptance?

RQ3
How does AI coding agent activity evolve over time?

📊 Dataset

The analysis uses the AIDev dataset, loaded directly from Hugging Face:

pd.read_parquet("hf://datasets/hao-li/AIDev/[table_name].parquet")

Tables Used

all_pull_request.parquet

all_repository.parquet

all_user.parquet

pr_reviews.parquet

pr_review_comments_v2.parquet

pr_commit_details.parquet

pr_task_type.parquet

Final Dataset Characteristics

Total PRs: 859,377

Time Range: January – August 2025

Agents: OpenAI Codex, Copilot, Cursor, Devin, Claude Code

Overall Acceptance Rate: 91.9%

⚠️ Important Note
Merged pull requests in AIDev are identified by a non-null merged_at timestamp, not by state == "merged":

pr_df['is_merged'] = pr_df['merged_at'].notna().astype(int)

🧪 Metrics Computed
RQ1 – Acceptance & Review Dynamics

Pull request acceptance rate

Time to close (hours)

Number of reviews

Approval vs. change request ratios

RQ2 – Pull Request Characteristics

Description length (character count)

Description length categories:

Very Short (<100)

Short (100–500)

Medium (500–2000)

Long (>2000)

RQ3 – Context & Temporal Patterns

Monthly pull request activity

Repository popularity (star count)

📈 Statistical Analysis

Chi-Square Test: Acceptance rate differences between agents

Kruskal–Wallis Test: Time-to-close comparison (non-parametric)

Effect Size Analysis: Practical impact interpretation

Key Findings

Acceptance rates vary significantly (68.5%–93.8%, p < 0.001)

Short descriptions (100–500 characters) achieve the highest acceptance rate (93.7%)

OpenAI Codex dominates pull request volume and acceptance after May 2025

📉 Visualizations

The analysis produces publication-quality visualizations, including:

Acceptance rate by agent

Merged vs. rejected pull requests

Time-to-close distributions

Impact of description length on acceptance

Temporal adoption trends of AI agents

All figures feature:

Clear labels and annotations

Appropriate color schemes

High-resolution output suitable for publication


▶️ How to Run the Analysis
1. Install Dependencies
pip install pandas numpy matplotlib seaborn scipy pyarrow

2. Run the Script
python simple_aidev_analysis.py

3. Outputs

Console: statistical summaries and test results

Figures: displayed interactively

CSV file: aidev_analysis_data.csv (859,377 rows)

⏱️ Expected runtime: less than 5 minutes

⚠️ Limitations

Commit-level PR size metrics unavailable (missing PR linkage)

Comment data not directly linked to pull requests

Strong agent imbalance (OpenAI Codex = 88.6% of PRs)

Correlational analysis only (no causal claims)

All limitations are explicitly documented and discussed in the accompanying report.

✅ Contributions & Impact

This project provides:

Researchers: Baseline metrics for AI coding agent studies

Developers: Evidence-based agent comparison

Tool Designers: Insights into effective pull request communication

📚 References

AIDev Dataset Paper: https://arxiv.org/abs/2507.15003

Hugging Face Dataset: https://huggingface.co/datasets/hao-li/AIDev

MSR 2026 Challenge: https://2026.msrconf.org/track/msr-2026-mining-challenge

Example Notebook: https://github.com/SAILResearch/AI_Teammates_in_SE3

🧾 License & Usage

This repository is intended for academic and research purposes under the MSR 2026 Mining Challenge.
Please cite the original AIDev dataset and this work when reusing results.
