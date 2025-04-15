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

Inicialmente, cada arquivo da rede anual foi lido utilizando a biblioteca networkx. Como o mesmo processo seria repetido para todas as redes, os grafos foram armazenados em uma lista. Para cada grafo, foram calculadas e armazenadas as métricas mencionadas com as funções da biblioteca.

Em seguida, foram gerados gráficos com matplotlib e seaborn mostrando a evolução anual das métricas, com destaque para os anos de avaliação do PPgEEC (2012, 2016, 2020, 2024), conforme mostra a imagem a seguir. E a partir da análise dos gráficos, foram observadas algumas principais informações a serem destacas importantes:
- Número de arestas: cresceu ao longo dos anos, indicando um aumento nas colaborações entre autores, com um pico em 2019.
- Número de vértices: apresentou crescimento gradual.
- Número médio de vizinhos: caiu em 2020 (pandemia), mas retomou o crescimento nos anos seguintes.
- Densidade da rede: não apresentou variações significativas ao longo dos anos

### Insights e Hipóteses
- O aumento das arestas sugere maior colaboração entre autores, com um pico em 2019 — possivelmente relacionado à expansão do programa.
- A retomada do crescimento após 2020 pode indicar incentivo a projetos colaborativos e maior integração entre pesquisadores.
- A densidade consistentemente baixa pode sugerir que os autores mantêm colaborações com um grupo restrito.

### Distribuição do Número de Vizinhos
O grau de cada nó foi calculado e visualizado por meio de gráficos de densidade com o modelo Ridgeline Chart, usando seaborn. Com base nos resultados gerados, notou-se algumas observações importantes:
- A distribuição é assimétrica, concentrando-se entre 5 e 10 conexões por autor.
- A forma da curva sugere a presença de hubs (autores com alta conectividade).
- A partir de 2022, a curva mostra maior densidade, com leve achatamento em 2025, indicando ampliação nas redes de colaboração.
colocar imagem

Outras hipóteses a serem levantadas são:
- A presença constante de autores com muitas conexões, sugere a docentes orientadores ou pesquisadores com alta produção e rede extensa.
- O aumento nas conexões a partir de 2022 pode estar associada à retomada pós-pandemia quando as colaborações voltaram a crescer.

Uma das principais dificuldades foi compreender o significado prático de cada métrica no contexto da coautoria. Além disso, foi desafiador escolher a melhor visualização para a distribuição dos vizinhos. A solução foi utilizar o modelo Ridgeline Chart, adaptado com auxílio do ChatGPT (GPT-4o), com o seguinte prompt:
```
ajuste esse código para as variaveis que quero. Sendo as variaveis: a distribuição de vizinhos esta na variavel: sort_degree_count em que ele é um degree_count = [Counter(deg) for deg in degrees]
sort_degree_count = [dict(sorted(count.items())) for count in degree_count] . Vertices: num_nodes. os anos esta em years. E o código[...]
```

As análises mais aprofundadas foram documentadas no notebook correspondente e acompanhadas de explicações sobre o que foi feito, assim como o prompt na integra.

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
