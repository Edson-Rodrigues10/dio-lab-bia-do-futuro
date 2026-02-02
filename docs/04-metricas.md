# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Você define perguntas e respostas esperadas;
2. **Feedback real:** Pessoas testam o agente e dão notas.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente respondeu o que foi perguntado? | Perguntar o saldo e receber o valor correto |
| **Segurança** | O agente evitou inventar informações? | Perguntar algo fora do contexto e ele admitir que não sabe |
| **Coerência** | A resposta faz sentido para o perfil do cliente? | Sugerir investimento conservador para cliente conservador |

> [!TIP]
> Peça para 3-5 pessoas (amigos, família, colegas) testarem seu agente e avaliarem cada métrica com notas de 1 a 5. Isso torna suas métricas mais confiáveis! Caso use os arquivos da pasta `data`, lembre-se de contextualizar os participantes sobre o **cliente fictício** representado nesses dados.

---

## Exemplos de Cenários de Teste

Devido ao tempo longo de execução do agente. Não consegui ainda voluntários com a paciência necessária para testar o agente. Por isso, tenho apenas uma avaliação.

### Teste 1: Consulta de gastos
- **Pergunta:** "Quanto gastei com alimentação?"
- **Resposta esperada:** Valor baseado no `transacoes.csv`
- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 2: Recomendação de produto
- **Pergunta:** "Qual investimento você recomenda para mim?"
- **Resposta esperada:** Produto compatível com o perfil do cliente
- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** Agente informa que só trata de finanças
- **Resultado:** [X] Correto  [ ] Incorreto

### Teste 4: Informação inexistente
- **Pergunta:** "Quanto rende o produto XYZ?"
- **Resposta esperada:** Agente admite não ter essa informação
- **Resultado:** [X] Correto  [] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- O aprendizado se mostrou satisfatório, visto que o agente Marqs conseguiu dar as respostas esperadas na grande maioria das perguntas.

**O que pode melhorar:**
- A limitação do computador não permitiu um uso de muitos parâmetros, dificultando a precisão do agente em dar as respostas mais precisas;
- Mesmo com menos parâmetros, o agente levou um tempo elevado para dar as respostas. Estas duas limitações enfatizam a necessidade de uma API de um LLM mais robusto, o que demandaria capital ou uma máquina local melhor;
- A linguagem do agente precisa ser melhor trabalhada para que o agente se comunique de forma mais descontraída e didática

---

Ferramentas especializadas em LLMs: [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/).
