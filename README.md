# Meeting-Summarizer
MVP -> Production Ready
# 🤖 Gemini Meeting Summarizer Workflow (n8n)

A workflow built in [n8n](https://n8n.io) to automatically process Gemini meeting summaries, extract deliverables using OpenAI, route to human approval, and create tasks in Monday.com.

---

## ⚙️ Features

- ✅ Pulls Google Docs content from Gemini summary emails
- ✅ Uses OpenAI to extract actionable deliverables
- ✅ Sends approval email to Elaine with summary context
- ✅ Adds approved tasks to Monday.com
- ✅ Logs rejections (planned via Supabase)
- ✅ Scalable & modular n8n design

---

## 🧩 Workflow Overview

> File: `workflow.json`

- `Fetch Meeting Emails`
- `Extract Doc Content`
- `AI: Extract Tasks` → `Parse Tasks` → `Split: One Task`
- `Send Task for Approval`
- `Decision: Approved?`
  - ✅ → `Add Task to Monday`
  - ❌ → `Log Task Status (rejected)` _(in progress)_

---

## 🚀 Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/TBDG/meeting-summarizer-workflow.git
