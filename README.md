# A evolução do estilo de jogo na NBA (1950–2026)

Trabalho da disciplina **Análise Exploratória de Dados e Visualização** (FGV EMAp, 2026.2).

Este trabalho investiga, a partir das estatísticas coletivas das equipes, como o estilo de jogo da NBA se transformou desde 1950. A análise olha para o ritmo, a eficiência ofensiva, o uso da bola de 3 pontos e a composição da pontuação. Também identifica quais métricas melhor descrevem essas mudanças.

**Grupo:** Diogo Vieira dos Santos · João Gabriel de Souza Machado · Marcelo Maiato Neves

## Estrutura do repositório

```
.
├── marco_1/
│   └── Marco_1.pdf                       # proposta e perguntas de pesquisa
├── marco_2/
│   └── Marco_2.ipynb                     # entrega intermediária
├── marco_3/                              # entrega final
│   ├── Marco_3.ipynb                     # notebook final
│   ├── Apresentacao.pdf                  # slides da apresentação (10 min)
│   └── DECLARACAO_DE_CONTRIBUICOES.md    # quem fez o quê
├── sem_comentarios/                      # notebook do Marco 3 sem comentários no código
├── data/                                 # CSVs da base do Kaggle
├── requirements.txt                      # pacotes necessários
├── LICENSE
└── README.md
```

## Entregas

| Marco | O que é | Onde está |
|---|---|---|
| 1 | Proposta: problema, dados e perguntas de pesquisa | [`marco_1/Marco_1.pdf`](marco_1/Marco_1.pdf) |
| 2 | Entrega intermediária: notebook em forma de artigo, com uma visualização inicial por pergunta | [`marco_2/Marco_2.ipynb`](marco_2/Marco_2.ipynb) |
| 3 | Entrega final: notebook completo, slides e declaração de contribuições | [`marco_3/`](marco_3/) |

## Dados

Os dados vêm da base [NBA Stats (1947–present)](https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats), de Sumitro Datta, que reúne estatísticas do Basketball-Reference. A pasta `data/` tem a base inteira; o trabalho usa seis arquivos:

| Arquivo | Uso |
|---|---|
| `Team_Totals.csv` | Totais de cada equipe por temporada (Marcos 2 e 3) |
| `Team_Summaries.csv` | Vitórias, ritmo, eficiência e taxas (Marcos 2 e 3) |
| `Opponent_Totals.csv` | Lado defensivo (Marco 3) |
| `Player_Shooting.csv` e `Player_Totals.csv` | Arremessos por distância, desde 1997 (Marco 3) |
| `Advanced.csv` | Qualidade do elenco, pelo BPM (Marco 3) |

## Principais achados

1. A NBA mudou em **duas ondas**: velocidade nos anos 1950–60 e eficiência e perímetro desde meados dos anos 2010.
2. O **3 pontos** passou de 2% para 35% dos pontos e substituiu, sobretudo, o arremesso de 2 de média distância.
3. Dentro de uma temporada, **ritmo e eficiência explicam 98,7%** das diferenças de pontuação entre equipes.
4. O estilo acompanha as vitórias mais do que as causa: controlando pela qualidade do elenco, a associação da taxa de 3 com as vitórias cai de +2,7 para +0,4 vitória por desvio-padrão.
5. As equipes **não convergiram** para um estilo único: a liga mudou de lugar, não de diversidade.
6. As maiores mudanças se concentram em **1954–59, 1969–74 e 2015–20**.

## Como rodar

1. Instale os pacotes (de preferência num ambiente virtual):

   ```
   pip install -r requirements.txt
   ```

2. Abra `marco_3/Marco_3.ipynb` no Jupyter ou no VS Code e rode todas as células. O notebook lê os CSVs de `data/` e roda em poucos segundos.

Os gráficos são feitos com Altair e são interativos (seleção pela legenda, zoom, menu de franquias e valores ao passar o mouse). O GitHub não exibe gráficos Altair na pré-visualização do notebook: para vê-los, rode o notebook.
