# Supported Providers

Sieve works with five AI providers. You supply your own key — Sieve just uses it to make calls on your behalf.

---

## Choosing the right provider

Here is a quick decision guide:

- **Just getting started and want something free** → OpenRouter
- **Images are sensitive or private** → Ollama
- **Best possible accuracy, willing to pay** → OpenAI or Anthropic
- **Already have a Google account** → Gemini

---

## OpenRouter

**Cost:** Free tier available, no credit card required for free models  
**Setup difficulty:** Easy  
**Best for:** Getting started, general use

OpenRouter is a gateway that gives you access to many AI models through a single API key. Sieve uses the free Qwen 2.5 VL 72B model by default — a large, capable vision model that handles most image types well.

**Free tier limits:**
- ~20 requests per minute
- ~200 requests per day

For most research workflows this is sufficient. If you regularly process large batches, you can add credits to your OpenRouter account and use the same key without limits.

**Changing the model:**  
In **Settings → Provider Settings**, you can enter any OpenRouter model string. Visit [openrouter.ai/models](https://openrouter.ai/models) and filter by vision-capable models to find alternatives.

**Sign up:** [openrouter.ai](https://openrouter.ai)

---

## Ollama

**Cost:** Free, runs on your device  
**Setup difficulty:** Moderate (requires installation)  
**Best for:** Private or sensitive images, offline use, institutions with data policies

Ollama runs a vision model locally on your own machine. Your images never leave your device at any point. There are no rate limits, no costs, and no internet connection required after the initial model download.

**Requirements:**
- A reasonably modern computer (last 5–7 years)
- ~4GB of free disk space for the model
- More RAM = better performance. 8GB minimum, 16GB recommended.

**Setup:**
1. Install Ollama from [ollama.com](https://ollama.com)
2. Open a terminal and run:
```bash
ollama pull llava
```
3. Select Ollama in Sieve settings — no API key required

**Speed:**  
Ollama is slower than cloud providers because it runs on your own hardware. On a modern laptop expect 5–15 seconds per image. On a machine with a dedicated GPU it will be significantly faster.

---

## OpenAI

**Cost:** Pay per use (very cheap for classification — roughly $0.003 per image with GPT-4o)  
**Setup difficulty:** Easy  
**Best for:** High accuracy, consistent results

OpenAI's GPT-4o is one of the strongest vision models available. If accuracy on difficult or ambiguous images is your priority, this is a good choice.

**Approximate cost for Sieve usage:**
- 1,000 images ≈ $3
- 10,000 images ≈ $30

**Sign up:** [platform.openai.com](https://platform.openai.com)

---

## Anthropic

**Cost:** Pay per use (roughly $0.005 per image with Claude Sonnet)  
**Setup difficulty:** Easy  
**Best for:** High accuracy, nuanced image understanding

Claude Sonnet has strong visual reasoning and handles unusual or complex images well. A good alternative to OpenAI if you prefer Anthropic's models.

**Sign up:** [console.anthropic.com](https://console.anthropic.com)

---

## Google Gemini

**Cost:** Free tier available with rate limits, paid beyond that  
**Setup difficulty:** Easy  
**Best for:** Users already in the Google ecosystem

Gemini has a usable free tier but the rate limits are stricter than OpenRouter's. If you hit limits frequently during a session, switch to OpenRouter for free access or Ollama for unlimited local access.

**Sign up:** [aistudio.google.com](https://aistudio.google.com)

---

## Can I switch providers later?

Yes. Go to **Settings → API Key** at any time to change your provider or key. Your label sets and previously sorted images are not affected.

---

## A note on data privacy per provider

When you use any cloud provider (OpenRouter, OpenAI, Anthropic, Gemini), your images are sent to that provider's servers for processing. Each provider has its own privacy policy governing how they handle API data.

If you are working with sensitive, confidential, or regulated data (patient images, unpublished research, proprietary materials), use **Ollama** — your images never leave your device.

Next: [Using Sieve for Anything](beyond-the-lab.md)
