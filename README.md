# 💬 Conversation Dataset Preprocessors

This repository contains multiple Python scripts and notebooks that **preprocess various raw conversational datasets** into a **unified JSON format**. Each script handles one dataset and outputs its own standardized file.

---

## 📦 What This Repo Does

- Converts diverse chat/email/message datasets into a consistent format.
- Assigns standardized:
  - **conversation IDs** (5-digit unique numbers)
  - **message IDs** (starting from 1 within each conversation)
- Filters out conversations with fewer than **8 messages**.
- Outputs cleaned data as `.json` files, one per dataset.

---

## 🧾 Output Format

Each script produces a JSON file following this **standard format**:

```json
{
  "10428": [
    {"from": "Client", "message_id": 1, "message": "Hi!"},
    {"from": "Agent", "message_id": 2, "message": "Hello!"},
    ...
  ],
  "56789": [
    {"from": "Agent", "message_id": 1, "message": "Good morning."},
    ...
  ]
}

