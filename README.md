# LiteLLM Gateway

A minimal LiteLLM gateway that provides an OpenAI-compatible API endpoint. This gateway can proxy requests to various LLM providers including GitHub Copilot.

## Deploy on Railway

1. Click the button below to deploy to Railway:

   [<img src="https://railway.app/button.svg" alt="Deploy on Railway">](https://railway.app/new/template?template=https://github.com/your-username/litellm-gateway)

2. Set the `MASTER_KEY` environment variable in Railway dashboard

3. Deploy and get your public URL

## API Usage

The gateway provides an OpenAI-compatible endpoint at `/v1/chat/completions`.

### Example curl request

```bash
curl -X POST https://your-railway-app.railway.app/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer CHANGE_ME_SECRET_KEY" \
  -d '{
    "model": "copilot",
    "messages": [
      {"role": "user", "content": "Hello!"}
    ]
  }'
```

Replace `CHANGE_ME_SECRET_KEY` with your actual master key and `your-railway-app.railway.app` with your Railway app URL.
