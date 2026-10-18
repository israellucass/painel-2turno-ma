# Painel — Seções eleitorais alteradas · Maranhão 2026

Página **estática e autocontida** que mostra quais das **194 seções eleitorais transferidas** no Maranhão para o **2º turno presidencial (25/10/2026)** afetam cada eleitor, além de um cruzamento com o voto do **1º turno (04/10/2026)** nessas seções — presidência em destaque — e uma **análise de distância** entre o local do 1º e o do 2º turno.

## Link

https://israellucass.github.io/painel-2turno-ma/

## O que tem

- **Busca** por município, local ou nº da seção (ex.: “Timon 214”).
- **Boletim presidencial** do 1º turno nas 194 seções (Lula em vermelho, Bolsonaro em azul, os demais somados em “Outros”), com percentuais sobre votos válidos.
- **Peso eleitoral**: quanto do voto de cada candidato no MA vem dessas seções.
- **Visualização interativa** Lula × Bolsonaro: distribuição do eleitorado por faixa de distância, com alternador (nº de eleitores / % de cada eleitorado) e controle de limiar (“quem mudou mais de X km”). Abaixo, uma tira com as 190 seções medidas, colorida pelo vencedor.
- **Análise de deslocamento**: as três lentes, o ranking dos locais que mais pesam (eleitores × km) e a distância de cada seção.
- **“Pode mudar o resultado da Presidência?”** — o tamanho do que está em jogo e uma simulação de comparecimento.
- **Gaveta por município** com o 1º turno e o contexto de senador/deputados.

## Números da base atual

| | |
|---|---|
| Seções / municípios | **194 / 27** |
| Eleitores · compareceram no 1º t. | **52.699 · 46.076 (87,4%)** |
| Votos válidos nessas seções | **44.474** — Lula **58,3%** (25.918) × Bolsonaro **36,0%** (16.001) |
| Distância mediana · máxima | **371 m · 14,3 km** |
| Média por eleitor | Lula **0,70 km** × Bolsonaro **0,76 km** |

## Fontes (oficiais, TSE)

| O que | Arquivo | Onde |
|---|---|---|
| Seções alteradas p/ o 2º turno (MA), **194 seções** | `secoes_eleitorais_alteradas_2t-pais_2026_ma.csv` | [TSE — locais de votação](https://www.tse.jus.br/servicos-eleitorais/local-de-votacao-zonas-eleitorais) · [por que o TSE mudou](https://www.tse.jus.br/comunicacao/noticias/2026/Outubro/entenda-por-que-a-justica-eleitoral-trocou-o-endereco-de-algumas-secoes-para-o-2o-turno) |
| Votação por seção — **1º turno (04/10/2026)** | `votacao_secao_2026_BR.csv` · `votacao_secao_2026_MA.csv` | [Dados Abertos TSE — Resultados 2026](https://dadosabertos.tse.jus.br/dataset/resultados-2026) |
| Locais e **coordenadas** — linhas do 1º e do 2º turno | `eleitorado_local_votacao_2026_MA.csv` | [Dados Abertos TSE — Eleitorado 2026](https://dadosabertos.tse.jus.br/dataset/eleitorado-2026) |

## Método (resumo)

- Percentuais sobre **votos válidos** (brancos e nulos excluídos).
- **Peso**: fatia do voto do candidato no Maranhão que saiu dessas 194 seções.
- **Distância**: linha reta (haversine) entre a **coordenada oficial do local no 1º turno** e a do **2º turno** — o próprio TSE publica as duas linhas por seção, com nome e coordenada. **0 m** quando a coordenada é a mesma; o nome cadastrado pode ter sido reescrito. Entram nas médias as **190 de 194** seções com coordenada válida nas duas pontas (97,9%); as 4 de Graça Aranha aparecem como “indisponível”.
- Quem define o que é uma **seção alterada** é a **lista oficial do TSE** — o nome do local pode continuar igual mesmo quando ele se desloca, e pode mudar sem que o local saia do lugar. Por isso o nome não é usado como critério.
- Em **6 municípios** (Barão de Grajaú, Buriticupu, Caxias, Grajaú, Lima Campos e Pinheiro) o total de votos do 1º turno supera o eleitorado listado para o 2º turno; nesses casos mostramos só o total de votos, sem percentual.

Página independente, sem vínculo com o TSE. Em caso de divergência, prevalece a informação oficial do TRE-MA/TSE.

## Reprodução e auditoria

O site publica `versao.json` com os hashes das entradas usadas. O pipeline e os portões de auditoria estão em [`ferramentas/`](../ferramentas/LEIAME.md).
