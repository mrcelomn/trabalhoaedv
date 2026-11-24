# A evolução do estilo de jogo na NBA (1950–2026)

Trabalho da disciplina **Análise Exploratória de Dados e Visualização** (FGV EMAp, 2026.2).

Este trabalho investiga, a partir das estatísticas coletivas das equipes, como o estilo de jogo da NBA se transformou desde 1950. A análise olha para o ritmo, a eficiência ofensiva, o uso da bola de 3 pontos e a composição da pontuação. Também identifica quais métricas melhor descrevem essas mudanças.

**Grupo:** Diogo Vieira dos Santos · João Gabriel de Souza Machado · Marcelo Maiato Neves

## Entregas

| Marco | Arquivo | Conteúdo |
|---|---|---|
| Marco 1 | [`Marco_1.pdf`](Marco_1.pdf) | Proposta do projeto e perguntas de pesquisa |
| Marco 2 | [`Marco_2.ipynb`](Marco_2.ipynb) | Entrega intermediária: notebook em forma de artigo, com uma visualização inicial por pergunta |
| Marco 3 | [`Marco_3.ipynb`](Marco_3.ipynb) · [`Marco_3.html`](Marco_3.html) | Entrega final: notebook completo, com todas as visualizações e a conclusão |
| Marco 3 | [`Apresentacao.pdf`](Apresentacao.pdf) | Slides da apresentação de 10 minutos |
| Marco 3 | [`DECLARACAO_DE_CONTRIBUICOES.md`](DECLARACAO_DE_CONTRIBUICOES.md) | Declaração de contribuições (quem fez o quê) |

## Estrutura do repositório

```
.
├── data/                           # dados brutos (CSVs do Kaggle) e _info.md com a fonte
├── sem_comentarios/                # versões dos notebooks sem comentários no código
├── Marco_1.pdf                     # entrega do Marco 1
├── Marco_2.ipynb                   # entrega do Marco 2
├── Marco_3.ipynb                   # entrega final (notebook executado)
├── Marco_3.html                    # entrega final exportada (abre no navegador, com gráficos interativos)
├── Apresentacao.pdf                # slides da apresentação
├── DECLARACAO_DE_CONTRIBUICOES.md  # quem fez o quê
├── requirements.txt
├── LICENSE
└── README.md
```

## Dados

Os dados vêm da base [NBA Stats (1947–present)](https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats), de Sumitro Datta, que reúne estatísticas do Basketball-Reference. No Marco 2, foram usados os arquivos `Team_Totals.csv` e `Team_Summaries.csv`. No Marco 3, foram acrescentados `Opponent_Totals.csv` (lado defensivo), `Player_Shooting.csv` e `Player_Totals.csv` (arremessos por distância, desde 1997) e `Advanced.csv` (qualidade do elenco, pelo BPM).

## Principais achados

1. A NBA mudou em **duas ondas**: velocidade nos anos 1950–60 e eficiência e perímetro desde meados dos anos 2010.
2. O **3 pontos** passou de 2% para 35% dos pontos e substituiu, sobretudo, o arremesso de 2 de média distância.
3. Dentro de uma temporada, **ritmo e eficiência explicam 98,7%** das diferenças de pontuação entre equipes.
4. O estilo acompanha as vitórias mais do que as causa: controlando pela qualidade do elenco, a associação da taxa de 3 com as vitórias cai de +2,7 para +0,4 vitória por desvio-padrão.
5. As equipes **não convergiram** para um estilo único: a liga mudou de lugar, não de diversidade.
6. As maiores mudanças se concentram em **1954–59, 1969–74 e 2015–20**.

## Como reproduzir

```
pip install -r requirements.txt
jupyter notebook Marco_3.ipynb
```

O notebook lê os CSVs de `data/` e roda em poucos segundos. Os gráficos são feitos com Altair e são interativos (seleção pela legenda, zoom, menu de franquias, dicas ao passar o mouse). Para vê-los sem instalar nada, abra o `Marco_3.html` no navegador: o GitHub não exibe gráficos Altair na pré-visualização do notebook.
