# Arquitetura da Informação deste Repositório

Este documento explica como os 6 conceitos estudados foram aplicados na organização do repositório.

## 1. Classificação

O conteúdo foi dividido em 4 grandes categorias no nível raiz:

| Pasta | Critério de classificação |
|---|---|
| `docs/` | Documentação sobre a estrutura do próprio repositório |
| `assets/` | Arquivos de mídia (imagens, diagramas, documentos), separados por tipo |
| `projeto-integrador/` | Classificado por **etapa do processo** (contextualização → entrega final) |
| `unidades-curriculares/` | Classificado por **disciplina** |

Dentro de `unidades-curriculares`, cada UC separa suas atividades numeradas, e a UC03 (Verificação e Validação de Software) tem ainda uma subpasta `testes/`, por ser específica da natureza daquela disciplina.

## 2. Taxonomia

Vocabulário controlado usado em todo o repositório:

- UCs: prefixo numérico + nome descritivo → `uc01-gestao-da-informacao`, `uc02-inteligencia-artificial`, `uc03-verificacao-e-validacao-de-software`, `uc04-extensao-full-stack`
- Etapas do PI: número + nome da etapa → `01-contextualizacao`, `02-pesquisa`
- Atividades: `atividade-NN` (numeração sequencial de 2 dígitos)
- Sempre em minúsculas, palavras separadas por hífen, sem acentos (evita problemas de compatibilidade entre sistemas operacionais)

Essa taxonomia está documentada no [glossário](./glossario.md), que também define os termos técnicos usados nas atividades.

## 3. Metadados

Cada `README.md` de atividade/UC contém um cabeçalho com metadados descritivos:

```markdown
---
uc: UC02 - Inteligência Artificial
atividade: atividade-01
data-entrega: 2026-10-15
status: concluido
tags: [machine-learning, dados]
---
```

Esses metadados tornam cada unidade de conteúdo autodescritiva, sem depender de contexto externo para ser compreendida.

## 4. Navegação

A navegação acontece em 3 camadas:

1. `README.md` da raiz → visão geral e links para as 4 categorias principais
2. `INDEX.md` → mapa completo, uma lista de tudo o que existe, com links diretos
3. `README.md` de cada UC → índice local daquela disciplina específica

Essa redundância é intencional: alguém que caiu direto numa subpasta via busca ainda encontra um README local explicando onde está.

## 5. Encontrabilidade

- Nomenclatura previsível (ver Taxonomia) permite adivinhar caminhos sem precisar navegar.
- [`mapa-de-conteudos.md`](./mapa-de-conteudos.md) funciona como um índice temático, agrupando atividades por assunto (não por pasta).
- Tags nos metadados permitem busca por tema usando a busca nativa do GitHub.

## 6. Relações entre conteúdos

As conexões entre UCs e entre UCs e o PI são explicitadas em dois lugares:

- No [`mapa-de-conteudos.md`](./mapa-de-conteudos.md), que lista essas relações de forma centralizada.
- Em uma seção **"Conteúdos relacionados"** ao final de cada atividade, linkando diretamente para o conteúdo correlato. Por exemplo, a atividade de modelagem da UC02 (Inteligência Artificial) pode referenciar a etapa de Requisitos do PI, caso o mesmo dataset seja usado nos dois.

---
⬅️ [Voltar ao índice](../INDEX.md)
