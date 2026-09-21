# Assistente virtual de currículo

Chat que responde sobre minha trajetória profissional, construído com Streamlit e um
modelo de linguagem. O contexto vem de `me/summary.txt`; nenhuma informação é inventada.

**Demo:** [em breve]

## Como funciona

- O resumo profissional é injetado no system prompt a cada requisição.
- Duas ferramentas (function calling): registro de contato de quem deixa e-mail, e
  registro de perguntas que o assistente não soube responder.
- O provedor de LLM é configurável por variável de ambiente — funciona com qualquer
  endpoint compatível com a API da OpenAI (Gemini, Groq, OpenRouter, OpenAI).

## Rodar localmente

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1      # Windows
pip install -r requirements.txt
copy .env.example .env          # edite e cole a chave
streamlit run app.py
```

## Deploy

Streamlit Community Cloud, apontando para este repositório. As credenciais vão em
Settings -> Secrets (ver `secrets.exemplo.toml`).

## Stack

Python, Streamlit, OpenAI SDK, Google Gemini.
