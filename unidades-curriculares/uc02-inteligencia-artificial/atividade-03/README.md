---
uc: UC02 - Inteligência Artificial
atividade: atividade-03
titulo: PI - Prompts e Dados Públicos - Oportunidade a Investigar
data-entrega: 2026-10-03
status: concluido
tags: [dados-publicos, decomposicao, saida-estruturada, rubrica, bndes, cnpj, analise-de-dados]
grupo: [Alisson Gustavo, Allyson George, Vitor Vieira, Hericc Rocha, Willami Durand]
equipe: Los Hermanos
---

# Atividade 03 — PI: Prompts e Dados Públicos — Qual Oportunidade Vale Investigar?

**Disciplina:** Inteligência Artificial
**Atividade em equipe:** 20 minutos
**Equipe:** Los Hermanos

## 📋 Enunciado

Analisar três bases públicas reais e escolher **um público e uma oportunidade** para investigar no Projeto Integrador.

**Bases fornecidas:**
| Base | Conteúdo |
|---|---|
| `01_Empresas_Recife_Reais.xlsx` | 31.683 registros de empresas abertas entre 2022 e 2025 |
| `02_Credito_BNDES_PE_2020_2025.xlsx` | 2.672 registros de operações de crédito do BNDES em PE (2020-2025) |
| `03_Contratos_Recife_Reais.xlsx` | 7.427 registros de contratos e 11.186 de aditivos da Prefeitura do Recife |

**Limites impostos pelo professor:** empresa cadastrada **não** significa startup; crédito do BNDES **não** equivale a investimento-anjo; é preciso cuidado com CNPJ completo, duplicação por aditivos e datas de vigência.

**Entrega exigida:** uma página com 3 evidências (fonte, recorte e cálculo verificável), 2 hipóteses comparadas (com evidência contrária a cada uma) e 1 decisão justificada (público + oportunidade + próximo teste), usando pelo menos **2 técnicas de prompt** (decomposição, encadeamento, saída estruturada ou rubrica), com a primeira resposta revisada.

## 👥 Equipe — Los Hermanos

Alisson Gustavo, Allyson George, Vitor Vieira, Hericc Rocha, Willami Durand

## 🔍 Evidências encontradas

**Evidência 1 — Existe um público recente e numeroso em tecnologia e economia criativa.**
A base de empresas tem 31.683 registros, correspondentes a **11.591 CNPJs distintos** (empresas abertas entre 2022-2025, CNAEs 58, 59, 60, 62, 63, 73, 74 e 90). Cálculo: 31.683 ÷ 11.591 ≈ **2,73 registros por CNPJ** — por isso não é correto tratar cada linha como uma empresa.

**Evidência 2 — Poucas empresas recentes aparecem também como fornecedoras da prefeitura.**
Cruzando CNPJ completo entre empresas e contratos, considerando só contratos iniciados **depois** da abertura da empresa: **34 empresas distintas**, **70 contratos**. Isso é **34 ÷ 11.591 × 100 = 0,29%** — ou seja, ~99,71% das empresas recentes não aparecem como fornecedoras com contrato posterior à abertura. Desses 70 contratos, ~61,4% estão ligados a eventos, produção cultural ou atividades criativas.

**Evidência 3 — O crédito do BNDES em Recife está concentrado em empresas maiores, sem correspondência direta com o recorte de empresas recentes.**
No recorte de Recife: 628 operações automáticas, 319 clientes distintos (311 médio porte, 162 pequeno, 133 grande, 22 microporte, 73 com indicador de inovação). Apenas **22 de 628 (3,5%)** eram microempresas. No cruzamento por CNPJ completo, **nenhuma correspondência** foi encontrada entre os 11.591 CNPJs recentes e os clientes das operações não automáticas do BNDES.

## ⚖️ Duas hipóteses comparadas

### Hipótese 1 — Empresas recentes têm dificuldade para acessar contratação pública
- **A favor:** só 34 de 11.591 CNPJs (≈0,29%) tiveram contrato iniciado após a abertura.
- **Contra:** as 34 empresas que conseguiram mostram que é possível; a ausência de contrato não prova que as demais tentaram e falharam.
- **Conclusão:** hipótese possível, mas não comprovada — os dados mostram baixa presença, não a causa dela.

### Hipótese 2 — O principal problema é a falta de acesso a financiamento
- **A favor:** apenas 22 de 628 operações automáticas do BNDES em Recife eram de microporte; nenhuma correspondência por CNPJ com operações não automáticas.
- **Contra:** ausência de correspondência não prova ausência de financiamento (identificadores mascarados nas operações automáticas; BNDES ≠ investimento-anjo).
- **Conclusão:** também precisa ser validada diretamente com os usuários.

## ✅ Decisão

**Público escolhido:** empresas recentes de Recife ligadas a tecnologia, economia criativa e serviços digitais, abertas entre 2022 e 2025.

**Oportunidade escolhida:** investigar como essas empresas conseguem acesso a financiamento, investidores e oportunidades de mercado, e quais as principais dificuldades para apresentar o negócio e encontrar parceiros adequados.

> Importante: os dados **não comprovam que essas empresas sejam startups** — CNPJ e CNAE isoladamente não classificam uma organização como startup. A próxima etapa deve validar essa característica diretamente com os usuários.

**Próximo teste:** entrevistas com 10 a 15 empresas recentes de tecnologia/economia criativa de Recife, perguntando sobre tentativas de financiamento, maior dificuldade encontrada, busca por investidores-anjo, tentativa de participar de licitações, e o que geraria confiança numa plataforma de conexão com investidores.

## 🔧 Prompts utilizados

**Prompt 1 — Decomposição:** pediu para dividir a análise em etapas (identificar recorte de cada base, contar CNPJs distintos, cruzar empresas × contratos por CNPJ completo, verificar se o contrato é posterior à abertura, cruzar com operações não automáticas do BNDES, isolar as automáticas por terem identificador mascarado, extrair 3 evidências quantitativas, formular 2 hipóteses com evidência contrária cada, e decidir público/oportunidade).

**Prompt 2 — Saída estruturada + rubrica:** exigiu revisão da primeira resposta em um formato fixo (Evidência 1/2/3 com fonte+filtro+unidade+cálculo+interpretação; Hipótese 1/2 com argumento a favor+evidência contrária+conclusão; Decisão; Próximo teste), revisando especificamente: diferença entre linhas e CNPJs, CNPJ completo, contratos anteriores à abertura, duplicação por aditivos, diferença entre contratado e desembolsado, identificadores mascarados do BNDES, e diferença entre crédito e investimento-anjo.

## 🔄 Comparação entre a primeira resposta e a revisada

A primeira análise identificava tendências gerais, mas corria o risco de generalizar demais (tratar empresas recentes como startups, ou relacionar crédito do BNDES diretamente com investimento). Após a revisão com o Prompt 2, foram adicionados controles metodológicos:

- Uso de **CNPJs distintos**, não apenas contagem de linhas
- Verificação da **data de abertura** antes de considerar contrato como posterior
- Separação entre **contratos e aditivos**
- Separação entre operações **automáticas e não automáticas** do BNDES
- Inclusão de evidência que **contraria cada hipótese**
- Distinção clara entre o que os dados comprovam e o que ainda precisa validação

## 📌 Conclusão

Os dados mostram um público relevante de empresas recentes de tecnologia/economia criativa em Recife, mas pouca presença desse grupo em contratos públicos e crédito não automático do BNDES. Isso não comprova uma dor específica, mas abre uma oportunidade de investigação: entender as dificuldades reais dessas empresas para acessar investidores, financiamento, clientes e parceiros — sem ainda partir para uma solução.

## 📚 Fontes dos dados

- `01_Empresas_Recife_Reais.xlsx` — 31.683 registros
- `02_Credito_BNDES_PE_2020_2025.xlsx` — 2.672 registros
- `03_Contratos_Recife_Reais.xlsx` — 7.427 contratos e 11.186 aditivos
- [Portal de Dados Abertos do Recife](https://dados.recife.pe.gov.br/)
- [BNDES Data](https://www.bndes.gov.br/wps/portal/site/home/bndes-data/)

## 📎 Anexos

- [Slide do enunciado da atividade](./enunciado-pi-prompts-dados-publicos.pdf)
- [Documento completo da análise (Word)](./pi-prompts-dados-publicos-oportunidade.docx)
- [01_Empresas_Recife_Reais.xlsx](./01_Empresas_Recife_Reais.xlsx)
- [02_Credito_BNDES_PE_2020_2025.xlsx](./02_Credito_BNDES_PE_2020_2025.xlsx)
- [03_Contratos_Recife_Reais.xlsx](./03_Contratos_Recife_Reais.xlsx)

## Conteúdos relacionados

- [UC02 - Inteligência Artificial - README](../README.md)
- [Atividade 01 - Mapa de Oportunidades](../atividade-01)
- [Atividade 02 - Hipótese de Problema](../atividade-02)
- [Projeto Integrador - Etapa de Pesquisa](../../../projeto-integrador/02-pesquisa)
- [Projeto Integrador - Etapa de Requisitos](../../../projeto-integrador/03-requisitos)
