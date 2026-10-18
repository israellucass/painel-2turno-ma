# Painel — Seções eleitorais alteradas · Maranhão 2026

Página **estática e autocontida** que mostra quais das **204 seções eleitorais transferidas** no Maranhão para o **2º turno presidencial (25/10/2026)** afetam cada eleitor, além de um cruzamento com o voto do **1º turno (04/10/2026)** nessas seções — presidência em destaque — e uma **análise de distância** entre o local antigo e o novo.

## Link

https://israellucass.github.io/painel-2turno-ma/

## O que tem

- **Busca** por município, local ou nº da seção (ex.: “Timon 214”).
- **Boletim presidencial** do 1º turno nas 204 seções (Lula em vermelho, Bolsonaro em azul), com percentuais sobre votos válidos.
- **Peso eleitoral**: quanto do voto de cada candidato no MA vem dessas seções.
- **Análise de deslocamento**: três lentes (dia a dia, cauda longa, extremos), ranking dos locais mais afetados (eleitores × km) e distância estimada por seção.
- **Gaveta por município** com o 1º turno e o contexto de senador/deputados.

## Fontes

- Seções alteradas: `secoes_eleitorais_alteradas_2t-pais_2026_ma.csv` (TSE).
- Votação por seção: `votacao_secao_2026_BR.csv` / `votacao_secao_2026_MA.csv` (TSE).
- Distâncias: estimativa em **linha reta** entre local antigo e novo, via OpenStreetMap (Nominatim + Overpass). Não é a rota real — é ordem de grandeza.

Página independente, montada a partir dos dados oficiais do TSE. Em caso de divergência, prevalece a informação oficial do TRE-MA/TSE.
