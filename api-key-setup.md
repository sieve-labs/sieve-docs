# Setting Up Your API Key

Sieve uses AI to classify your images. To do this it needs access to an AI provider — a service that runs the vision model. You connect your own account with your own key, so Sieve never sees your images on its own servers.

This page explains how to get a key for each supported provider and enter it into Sieve.

---

## Which provider should I choose?

| Provider | Cost | Best for |
|----------|------|----------|
| OpenRouter | Free tier available | Getting started, no credit card needed |
| Ollama | Free, runs locally | Private or sensitive images, offline use |
| OpenAI | Paid | High accuracy, willing to pay |
| Anthropic | Paid | High accuracy, willing to pay |
| Google Gemini | Free tier with limits | Already have a Google account |

**If you are unsure, start with OpenRouter.** It is free, takes two minutes to set up, and works well for most use cases.

**If your images are sensitive** — patient data, proprietary research, unpublished results — use Ollama. It runs entirely on your own machine and your images never leave your device at all.

---

## OpenRouter (recommended for getting started)

OpenRouter gives you access to several powerful vision models for free without requiring a credit card.

1. Go to [openrouter.ai](https://openrouter.ai) and create a free account
2. Once logged in, go to **Keys** in the left sidebar
3. Click **Create Key**, give it a name like `sieve`, and copy the key
4. Open Sieve, go to **Settings → API Key**
5. Select **OpenRouter** as your provider
6. Paste your key and save

The default model in Sieve for OpenRouter is `qwen/qwen2.5-vl-72b-instruct:free` which is a strong free vision model. You can change the model in Settings if you want to try others.

> **Free tier limits:** OpenRouter's free models allow around 20 requests per minute and 200 per day. For most users this is more than enough. If you are processing very large batches you may hit the daily limit — in that case either wait until the next day or switch to a paid model.

> **Screenshot placeholder — API key entry screen**

---

## Ollama (local, offline, private)

Ollama runs an AI model directly on your computer. No internet connection is needed after setup, and your images never leave your device under any circumstances.

**This is the right choice if:**
- You work with sensitive, confidential, or patient images
- Your institution has data policies that prevent using cloud services
- You want complete privacy and control

**Setup:**

1. Install Ollama from [ollama.com](https://ollama.com)
2. Open a terminal and pull the vision model:
```bash
ollama pull llava
```
3. Ollama runs automatically in the background once installed
4. Open Sieve, go to **Settings → API Key**
5. Select **Ollama** as your provider
6. No API key is needed — just save

> **Note on speed:** Ollama runs on your own hardware, so classification will be slower than cloud providers, especially on older machines. On a modern laptop with a decent GPU, expect a few seconds per image. On older hardware it may take 10–20 seconds per image.

---

## OpenAI

1. Go to [platform.openai.com](https://platform.openai.com) and create an account
2. Add a payment method and purchase some credits (even $5 will last a long time for image classification)
3. Go to **API Keys** and create a new key
4. Open Sieve, go to **Settings → API Key**
5. Select **OpenAI** as your provider
6. Paste your key and save

Sieve uses `gpt-4o` for OpenAI which has strong vision capabilities.

---

## Anthropic

1. Go to [console.anthropic.com](https://console.anthropic.com) and create an account
2. Add a payment method and purchase credits
3. Go to **API Keys** and create a new key
4. Open Sieve, go to **Settings → API Key**
5. Select **Anthropic** as your provider
6. Paste your key and save

Sieve uses `claude-sonnet-4-6` for Anthropic.

---

## Google Gemini

1. Go to [aistudio.google.com](https://aistudio.google.com) and sign in with your Google account
2. Click **Get API Key** and create a new key
3. Open Sieve, go to **Settings → API Key**
4. Select **Gemini** as your provider
5. Paste your key and save

Gemini has a free tier but with rate limits. If you hit them frequently, consider switching to OpenRouter or Ollama.

---

## Where is my key stored?

Your API key is stored locally on your device using secure encrypted storage. It is never sent to any Sieve server because Sieve has no servers. The key is only used to make direct API calls from your device to your chosen provider.

---

## Changing your provider or key

Go to **Settings → API Key** at any time to change your provider or update your key.

Next: [How Classification Works](how-classification-works.md)
