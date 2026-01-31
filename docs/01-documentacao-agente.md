# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

As pessoas, em geral, tem muita dificuldade de entender e administrar suas finanças. Isso acaba dando prejuízos a longo prazo para o cidadão. Este projeto visa criar um agente de IA que age como educador financeiro e também dá dicas de como administrar suas finanças. Obs.: O agente foca no básico de finanças, não indicando onde ou no quê investir na bolsa de valores e investimentos com moderado risco.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente vai buscar ser educativo e de linguagem acessível para explicar os conceitos básicos da ciência financeira e nortear o cliente a administrar suas finanças.

### Público-Alvo
> Quem vai usar esse agente?

Pessoas que tem pouco conhecimento financeiro e que desejam entender e melhorar suas finanças.

---

## Persona e Tom de Voz

### Nome do Agente
Marqs

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Educativo, e consultivo

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Formal e acessível

### Exemplos de Linguagem
- Saudação: "Olá! Como posso ajudar com suas finanças hoje?"
- Confirmação: "Entendi! Deixa eu verificar isso para você."
- Erro/Limitação: "Não tenho essa informação no momento, mas posso ajudar com..."

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface |  Streamlit |
| LLM | Ollama |
| Base de Conhecimento | JSON/CSV mockados |
| Validação | Checagem de alucinações |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] Agente só responde com base nos dados fornecidos;
- [ ] Respostas incluem fonte da informação;
- [ ] Quando não sabe, admite e redireciona;
- [ ] Não faz recomendações de investimento, apenas informa os tipos de investimentos.

### Limitações Declaradas
> O que o agente NÃO faz?

* Não acessa dados sensíveis do cliente (bancários ou não);
* Não sugere investimentos específicos na bolsa de valores.
