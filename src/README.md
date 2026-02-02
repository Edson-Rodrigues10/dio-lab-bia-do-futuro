# Passo a passo para execução:
```bash
# 1 baixar o Ollama (ollama.com)
# 2 Baixar um modelo leve (ex: gpt-oss, gemma2)
ollama pull gemma2

```

# Código da Aplicação

O código-fonte completo está no arquivo `app.py`

## Como Rodar

```bash
# 1. Instalar dependências:
pip install streamlit pandas requests

#Verificar se o Ollama está funcionando:
ollama serve

# Rodar a aplicação
streamlit run .\src\app.py
```
