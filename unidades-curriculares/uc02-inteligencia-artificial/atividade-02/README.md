---
uc: UC02 - Inteligência Artificial
atividade: atividade-02
titulo: Engenharia de Prompt Avançada - Hipótese de Problema
data-entrega: 2026-10-03
status: concluido
tags: [engenharia-de-prompt-avancada, decomposicao, encadeamento, metaprompt, few-shot, rubrica, hipotese-de-problema]
grupo: [Alisson Gustavo, Allyson George, Hericc Rocha, Vitor Vieira, Willami Durand]
---

# Atividade 02 — Engenharia de Prompt Avançada: Da Oportunidade à Hipótese de Problema

**Disciplina:** Inteligência Artificial (TADS040)
**Professor:** Rodrigo Rios
**Tema da aula:** Engenharia de Prompt Avançada — do pedido complexo ao processo testável (decomposição, few-shot, metaprompts, encadeamento, rubricas)

## 📋 Enunciado

Continuação da Atividade 01: a equipe deveria escolher **uma das três oportunidades priorizadas** na aula anterior e aprofundá-la usando pelo menos **4 técnicas avançadas de engenharia de prompt**, sem ainda propor solução. Regra principal: investigar o problema antes de decidir a solução.

**Técnicas exigidas (usar ao menos 4):** decomposição do problema, encadeamento de prompts, metaprompt, saída estruturada, rubrica de avaliação, refinamento iterativo e comparação de respostas.

**Roteiro:** escolher oportunidade → decompor com um prompt → encadear a saída no próximo prompt → pedir crítica à IA (metaprompt) → refinar o prompt → comparar duas respostas → registrar a hipótese de problema final.

**Entrega exigida (1 PDF por equipe):** oportunidade escolhida, sequência de 3 a 5 prompts encadeados, refinamentos, comparação entre respostas, hipótese de problema final e lacunas de validação pendentes. Ainda não era necessário propor solução.

## 👥 Grupo

Alisson Gustavo, Allyson George, Hericc Rocha, Vitor Vieira, Willami Durand

## 🎯 Oportunidade escolhida

Entre as 3 oportunidades priorizadas na Atividade 01, a equipe selecionou a **Oportunidade 2** por ter a base de evidência externa mais forte e estar no núcleo da proposta de matchmaking do PI:

> "Investidores anjo têm dificuldade de triagem eficiente de startups candidatas, por falta de padronização e evidência estruturada nas informações apresentadas (pitch decks, dados de tração, informações financeiras)."

## 🔗 Sequência de prompts encadeados

Foram usados 5 prompts, aplicando decomposição, encadeamento, metaprompt e refinamento:

| Prompt | Técnica | Resumo da resposta |
|---|---|---|
| **1** | Decomposição | Separou quem é afetado (investidores e startups), a dor (tempo/esforço na triagem), 4 causas possíveis e o que falta validar |
| **2** | Encadeamento | Classificou as 4 causas em fato / hipótese razoável / suposição sem base, apontando a necessidade de evidência externa |
| **3** | Encadeamento (busca de evidências) | Localizou dados reais: 92% dos investidores relatam dificuldade em localizar startups qualificadas (Pesquisa Sebrae/Anjos do Brasil, 2025) |
| **4** | Metaprompt (crítica) | Apontou viés de generalização (evidência nacional, não local), falta de distinção entre investidor individual e rede organizada, e termo "padronização" vago |
| **5** | Refinamento | Reformulou a hipótese explicitando o escopo nacional da evidência, separando tipos de investidor e definindo "padronização" com precisão |

## 🧱 Saída estruturada (JSON)

```json
{
  "oportunidade": "triagem de startups por investidores anjo",
  "envolvido_principal": "investidor anjo (individual e rede organizada)",
  "envolvido_secundario": "startup early-stage",
  "dor": "dificuldade de triagem eficiente por falta de conteúdo mínimo comparável entre propostas",
  "evidencias": [
    {"fonte": "Pesquisa Investimento Anjo Brasil 2025 (Sebrae/Anjos do Brasil)", "tipo": "fato", "escopo": "nacional"},
    {"fonte": "guias de análise de pitch (GV Angels)", "tipo": "hipótese com apoio", "escopo": "nacional"},
    {"fonte": "programas de pré-incubação do Porto Digital", "tipo": "hipótese com apoio", "escopo": "local"}
  ],
  "lacunas": [
    "não há evidência local específica sobre investidores do Porto Digital",
    "não há distinção clara entre investidor individual e rede organizada",
    "definição de padronização ainda depende de validação"
  ],
  "status": "hipótese de problema, não validada"
}
```

## 📊 Rubrica de avaliação da investigação

| Critério | Nota da equipe (0-2) |
|---|---|
| Aderência ao tema | 2 |
| Evidências | 2 |
| Estrutura | 2 |
| Técnica | 2 |
| Refinamento | 2 |
| **Pontuação total** | **10 de 10** |

## ⚖️ Comparação entre versões (antes x depois do metaprompt)

| Aspecto | Versão 1 (antes da crítica) | Versão 2 (depois do refinamento) |
|---|---|---|
| Escopo da evidência | Aplicável ao ecossistema em geral | Explicitamente marcada como nacional, com validação local pendente |
| Tipo de investidor | Tratado como grupo único | Separa investidor individual de rede organizada |
| Definição de padronização | Vaga (formato do pitch) | Definida como conteúdo mínimo comparável entre propostas |
| Tratamento da incerteza | Misturada às afirmações | Isolada em lista própria de "pontos a validar" |

## 🏁 Hipótese de problema (final)

> Nossa investigação indica que **investidores anjo** que avaliam startups do ecossistema do Porto Digital podem enfrentar **dificuldade de triagem eficiente** das propostas recebidas, no contexto de um alto volume de oportunidades chegando por canais informais e sem conteúdo mínimo comparável entre os pitches, porque pesquisas nacionais recentes (Sebrae/Anjos do Brasil, 2025) mostram que 92% dos investidores relatam dificuldade em localizar startups qualificadas e 59,5% relatam dificuldade em acessar boas oportunidades, além de o próprio ecossistema do Porto Digital já oferecer mentoria de preparação de pitch para startups em fase inicial.

**Ainda precisamos validar:**
- Se investidores que atuam especificamente no Porto Digital enfrentam essa mesma dificuldade (a evidência disponível é nacional).
- Se o problema afeta de forma diferente investidores individuais e redes organizadas.
- O que, na prática, investidores locais consideram "conteúdo mínimo comparável".

## 📎 Anexos

- [Slide da aula (Engenharia de Prompt Avançada)](./slide-aula-engenharia-de-prompt-avancada.pdf)
- [PDF da entrega completa do grupo](./entrega-hipotese-de-problema.pdf)

## Conteúdos relacionados

- [UC02 - Inteligência Artificial - README](../README.md)
- [Atividade 01 - Mapa de Oportunidades](../atividade-01)
- [Projeto Integrador - Etapa de Pesquisa](../../../projeto-integrador/02-pesquisa)
- [Projeto Integrador - Etapa de Requisitos](../../../projeto-integrador/03-requisitos)
