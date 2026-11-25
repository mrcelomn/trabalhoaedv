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
│   ├── graficos/                         # imagens de todas as visualizações do notebook
│   └── DECLARACAO_DE_CONTRIBUICOES.md    # quem fez o quê
├── data/                                 # CSVs da base do Kaggle
├── requirements.txt                      # pacotes necessários
└── README.md
```

## Entregas

| Marco | O que é | Arquivos |
|---|---|---|
| 1 | Proposta: problema, dados e perguntas de pesquisa | [Proposta (PDF)](marco_1/Marco_1.pdf) |
| 2 | Entrega intermediária: notebook em forma de artigo | [Notebook](marco_2/Marco_2.ipynb) |
| 3 | Entrega final | [Notebook](marco_3/Marco_3.ipynb) · [Slides](marco_3/Apresentacao.pdf) · [Gráficos](marco_3/graficos/) · [Contribuições](marco_3/DECLARACAO_DE_CONTRIBUICOES.md) |

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
3. Pontos por jogo são, na prática, **ritmo × eficiência**: por isso confundem velocidade com qualidade do ataque e enganam na comparação entre épocas.
4. O estilo está associado às vitórias, mas boa parte disso parece refletir a qualidade dos elencos: controlando por ela, a associação da taxa de 3 com as vitórias cai de +2,7 para +0,4 vitória por desvio-padrão.
5. As equipes **não convergiram** para um estilo único: a liga mudou de lugar, e a diversidade geral de estilos não teve tendência.
6. As maiores mudanças se concentram em **1954–59, 1969–74 e 2015–20**.

## Visualizações

O GitHub não exibe os gráficos interativos do notebook. Por isso, a pasta [`marco_3/graficos/`](marco_3/graficos/) tem uma imagem de cada visualização, na ordem em que aparecem no notebook. As imagens são estáticas: a interatividade (seleção pela legenda, zoom, menu de franquias e valores ao passar o mouse) só funciona rodando o notebook.

| Pergunta | Gráficos |
|---|---|
| Q1. Pontos por jogo | [Média da liga e faixa das equipes](marco_3/graficos/q1_1_pontos_por_jogo.png) · [Boxplots por década](marco_3/graficos/q1_2_boxplot_decadas.png) |
| Q2. Arremessos | [Tentativas por tipo](marco_3/graficos/q2_1_tentativas_por_tipo.png) · [Aproveitamento por tipo](marco_3/graficos/q2_2_aproveitamento_por_tipo.png) · [Arremessos por distância](marco_3/graficos/q2_3_arremessos_por_distancia.png) |
| Q3. Bola de 3 | [Adoção do 3](marco_3/graficos/q3_1_adocao_do_3.png) · [Composição dos pontos](marco_3/graficos/q3_2_composicao_dos_pontos.png) |
| Q4. Ritmo e eficiência | [Trajetória ritmo × eficiência](marco_3/graficos/q4_1_trajetoria_ritmo_eficiencia.png) · [Séries no tempo](marco_3/graficos/q4_2_ritmo_e_eficiencia_no_tempo.png) |
| Q5. Pontuação | [Pontos × ritmo e eficiência](marco_3/graficos/q5_1_dispersao_pontos_ritmo_eficiencia.png) · [Índice 1980 = 100](marco_3/graficos/q5_2_indice_1980.png) |
| Q6. Estilo e vitórias | [Estilo × vitórias](marco_3/graficos/q6_1_estilo_vs_vitorias.png) · [Correlação por década](marco_3/graficos/q6_2_correlacao_por_decada.png) |
| Q7. Diversidade | [Heterogeneidade](marco_3/graficos/q7_1_heterogeneidade.png) · [Dispersão por característica](marco_3/graficos/q7_2_dispersao_por_caracteristica.png) · [Mapa de estilos (PCA)](marco_3/graficos/q7_3_mapa_de_estilos_pca.png) |
| Q8. Períodos de mudança | [Métricas padronizadas](marco_3/graficos/q8_1_metricas_padronizadas.png) · [Intensidade de mudança](marco_3/graficos/q8_2_intensidade_de_mudanca.png) · [Variação entre décadas](marco_3/graficos/q8_3_variacao_entre_decadas.png) |

## Como rodar

1. Instale os pacotes (de preferência num ambiente virtual):

   ```
   pip install -r requirements.txt
   ```

2. Abra `marco_3/Marco_3.ipynb` no Jupyter ou no VS Code e rode todas as células. O notebook lê os CSVs de `data/` e roda em poucos segundos.

Os gráficos são feitos com Altair e são interativos. Para vê-los sem rodar nada, use as imagens de [`marco_3/graficos/`](marco_3/graficos/).
