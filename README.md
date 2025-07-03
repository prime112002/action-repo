# Action Repo - Trigger GitHub Webhooks

This repository is used to simulate GitHub events like `push`, `pull_request`, and `merge` which are sent to the webhook endpoint in the `webhook-repo`.

## 📘 Purpose

To test webhook delivery and observe how events are received and displayed in the UI served by the webhook Flask app.

## ✅ Branches Created

- `main` (default)
- `dev`
- `feature-x`

## 🎯 How to Trigger Webhook Events

### 1. Push Event

```bash
git checkout dev
echo "Testing webhook" >> push.txt
git add .
git commit -m "Push event trigger"
git push origin dev
```

### 2. Pull Request

- Create a pull request from `dev` to `main` on GitHub UI.

### 3. Merge Event

- After PR creation, merge it via GitHub UI to trigger the `merge` webhook.

## 🔗 Webhook Configuration

Webhook URL:  
```
https://<your-ngrok-id>.ngrok-free.app/webhook
```

Events Enabled:
- Push
- Pull Request

SSL verification: ✅ Enabled

## 💡 Note

This repo contains no backend or UI. It simply exists to simulate GitHub activity which is captured by the webhook endpoint.

---

## 📮 License

This project was created as part of a developer assessment task.
