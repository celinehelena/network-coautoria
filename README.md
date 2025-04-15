# Projeto U1P1 — Redes Temporais de Coautoria

Este repositório contém a implementação do Projeto 1 da Unidade 1 da disciplina de Algoritmos e Estrutura de dados 2, cujo objetivo é a construção e análise de redes de coautoria a partir de dados reais do PPgEEC, utilizando a biblioteca NetworkX em Python.

## Integrantes

- Celine Helena Abrantes de Andrade
- Maria Eduarda Lima da Luz

---

## Estrutura do repositório

- `dados/` — Arquivos de entrada no formato `.gexf`
- `video/` — Link para vídeo explicativo
- `README.md` — Este documento
- `requisitos/` — Subpastas ou arquivos separados por requisito (1, 2 e 3)

---

## Requisito 1 — Análise Temporal

Análise das métricas ano a ano (2010 a 2025) da rede geral, com geração de gráficos para:

- Densidade
- Número de vértices
- Número de arestas
- Número médio de vizinhos
- Distribuição do número de vizinhos (ridgeline chart)

As análises foram documentadas no notebook correspondente e acompanhadas de explicações sobre o que foi feito, principais achados e hipóteses.

---

## Requisito 2 — Análise dos Períodos de Avaliação

As redes dos períodos 2010–2012, 2013–2016, 2017–2020 e 2021–2024 foram visualizadas considerando:

- Tamanho dos nós proporcional ao grau
- Cor da aresta: vermelha (entre permanentes) e preta (caso contrário)
- Largura da aresta proporcional ao número de citações
- Destaque dos 5 autores mais conectados em dourado

A análise qualitativa desses períodos, junto das visualizações, está registrada na pasta do Requisito 2.

---

## Requisito 3 — Subgrafo e Rede Ego

Foi gerado um subgrafo a partir da rede geral (2010–2025), considerando apenas os vértices com pelo menos X vizinhos. A escolha de X foi baseada em uma análise estatística da distribuição do grau.

- Comparação de densidade entre rede geral e subgrafo
- Visualizações de ambos os grafos
- Análise da rede ego de um dos principais vértices do subgrafo

Todos os passos estão descritos no notebook do Requisito 3.

---

## Uso de IA Generativa

Foram utilizadas ferramentas de IA para auxiliar na escrita de código, estruturação do README e organização das análises textuais. A principal ferramenta foi:

- ChatGPT (OpenAI) — apoio na geração de gráficos com NetworkX e na organização de seções explicativas

---

## Execução

Para rodar o projeto:

1. Subir os arquivos `.gexf` em `dados/`
2. Abrir e executar os notebooks em `notebooks/`
3. As imagens serão salvas automaticamente em `imagens/`

---

## Vídeo explicativo

🎥 [Link para o vídeo no Loom ou YouTube](https://www.loom.com/share/seu-video-aqui)

---

## Referências

- NetworkX documentation: https://networkx.org/
- Matplotlib: https://matplotlib.org/
- Exemplos de repositório:
  - [Classificador Cat/Dog/Panda](https://github.com/Morsinaldo/embedded_artificial_intelligence/tree/main/projects/cat_dog_panda_classifier)
  - [Tráfego aéreo no Brasil](https://github.com/thaisaraujom/algorithms_datastructure_ii/tree/main/brazil_air_traffic)

---
