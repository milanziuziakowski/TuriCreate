# Amazon Baby Reviews — Modern Sentiment Classification

This repository contains a focused, modern sentiment classification demo for Amazon baby product reviews. It replaces legacy TuriCreate artifacts with a lean, maintainable pipeline using scikit-learn and Hugging Face Transformers.

Contents kept in this cleaned snapshot (branch: infra-data-stand):

- amazon_baby_sentiment_modern.ipynb — End-to-end notebook with TF-IDF baselines and optional DistilBERT inference.
- README.md — This file (overview, how to run, notes on AWS vs Azure as of 2024–2025).
- requirements.txt — pinned Python packages used by the notebook.
- .gitignore — Python defaults.
- LICENSE — preserved if it existed in the original repo.
- ARCHIVE/README.md — points to the `pre-cleanup-backup` branch with recovery instructions.

Quickstart
----------

1. Create and activate a virtual environment:

   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate

2. Install dependencies:

   pip install -r requirements.txt

3. Run the notebook (`amazon_baby_sentiment_modern.ipynb`) in JupyterLab or Colab. The notebook includes sample data and instructions to use your own Amazon reviews CSV.

CSV format expected
-------------------

- Columns: `name`, `review`, `rating`
- `rating` should be numeric (1–5). The notebook removes neutral (3) and treats rating >= 4 as positive.

AWS vs Azure (short summary, 2024–2025)
-------------------------------------

- AWS: Bedrock for managed generative AI, SageMaker for end-to-end ML, Trainium/Inferentia custom chips, S3 + Iceberg for data lakes, Aurora DSQL for serverless SQL. Strong model marketplace and hardware options.
- Azure: Azure OpenAI / AI Studio for generative AI, Azure Machine Learning for lifecycle management, high-performance ND-series GPU VMs, and deep Microsoft 365/Copilot integrations. Strong enterprise governance and productivity integrations.

Both clouds are competitive: choose AWS for model/hardware diversity and Azure for Microsoft ecosystem integration.

References
----------
- https://www.aboutamazon.com/news/aws/amazon-nova-ai-canvas-reel-aws-reinvent
- https://awsinsider.net/articles/2025/01/09/catch-up-with-whats-new-for-ai-in-2025.aspx
- https://blog.consoleconnect.com/whats-new-with-aws-for-2025
