# Action Repository — GitHub Events Sender

This repository is configured to automatically send repository activity events to an external webhook endpoint using GitHub Actions.

It is part of a webhook pipeline consisting of:

1. action-repo → generates events
2. webhook-repo → receives and stores events
3. MongoDB → stores data
4. UI → displays activity

---

## 🚀 What this repository does

Whenever one of the following events occurs, a GitHub Action sends the event payload to the webhook server:

- Push to any branch
- Pull Request created
- Pull Request merged

The webhook endpoint stores the data and makes it available for display in a UI.

---

## 🔗 Webhook Flow

GitHub Action  
→ Sends HTTP POST request  
→ Webhook server receives event  
→ MongoDB stores event  
→ UI polls and displays activity  


