<p align="center"><img src="https://raw.githubusercontent.com/opaq-computer/brand/main/logo/opaq-logo-512.png" width="96" alt="Opaq" /></p>

<h1 align="center">Opaq OpenAPI spec</h1>

<p align="center">The machine-readable description of the <a href="https://opaq.computer">Opaq</a> API: OpenAI-compatible and Anthropic-compatible private inference, paid from a sealed balance.</p>

- **Spec:** [`openapi.json`](openapi.json) (OpenAPI 3.1), also served live at [opaq.computer/openapi.json](https://opaq.computer/openapi.json)
- **For language models:** [opaq.computer/llms.txt](https://opaq.computer/llms.txt)
- **Human docs:** [opaq.computer/docs](https://opaq.computer/docs)

## Endpoints

| Method | Path | |
|---|---|---|
| `GET` | `/v1/models` | Live catalog with prices per 1M tokens. No key. |
| `POST` | `/v1/chat/completions` | OpenAI Chat Completions, streaming, tools, vision |
| `POST` | `/v1/messages` | Anthropic Messages, streaming |
| `POST` | `/v1/messages/count_tokens` | Token estimate for a Messages payload |

Base URL `https://opaq.computer`. Auth: `Authorization: Bearer opaq_sk_...` (or `x-api-key`).

## Generate a client

```bash
npx @openapitools/openapi-generator-cli generate -i https://opaq.computer/openapi.json -g python -o ./opaq-client
```

[Website](https://opaq.computer) · [Docs](https://opaq.computer/docs) · [Security](https://opaq.computer/security) · [Changelog](https://opaq.computer/changelog) · [X](https://x.com/OpaqPrivacy)
