# Base de Conhecimento

## Dados Utilizados

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações e explicações |
| `produtos_financeiros.json` | JSON | Base para explicações dos produtos financeiros disponíveis |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente e usar essas informações de forma didática e para sugestões|

> [!TIP]
> **Dataset público:**  [Hugging Face](https://huggingface.co/datasets).

---

## Adaptações nos Dados

Foram adicionados ao arquivo `produtos_financeiros.json` os seguintes produtos financeiros:
- Tesouro Prefixado;
- Tesouro IPCA + NTN-B;
- Poupança;
- Fundos Imobiliários.

Para uma maior base de dados para as sugestões e explicações do agente.

---

## Estratégia de Integração

### Como os dados são carregados?

Os dados serão carregados via código da seguinte forma:

```python
import pandas as pd
import json

# Arquivos CSV:
historico = pd.read_csv('data/historico_atendimento.csv')
transacoes = pd.read_csv('data/transacoes.csv')

# Arquivos Json:
with open('data/perfil_investidor.json', 'r', encoding='utf-8') as f:
  perfil = json.load(f)

with open('data/produtos_financeiros.json', 'r', encoding='utf-8') as f:
  produtos = json.load(f)
```

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?



---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
