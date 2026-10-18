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

## Fontes (oficiais)

Todos os números vêm de arquivos públicos do **TSE**; as distâncias, do **OpenStreetMap**.

| O que | Arquivo | Onde |
|---|---|---|
| Seções alteradas p/ o 2º turno (MA), 204 seções | `secoes_eleitorais_alteradas_2t-pais_2026_ma.csv` | [TSE — locais de votação](https://www.tse.jus.br/servicos-eleitorais/local-de-votacao-zonas-eleitorais) · [por que o TSE mudou](https://www.tse.jus.br/comunicacao/noticias/2026/Outubro/entenda-por-que-a-justica-eleitoral-trocou-o-endereco-de-algumas-secoes-para-o-2o-turno) |
| Votação por seção — 1º turno (04/10/2026) | `votacao_secao_2026_BR.csv` · `votacao_secao_2026_MA.csv` | [Dados Abertos TSE — Resultados 2026](https://dadosabertos.tse.jus.br/dataset/resultados-2026) |
| Eleitorado e locais de votação — 2026 | `eleitorado_local_votacao_2026.zip` | [Dados Abertos TSE — Eleitorado 2026](https://dadosabertos.tse.jus.br/dataset/eleitorado-2026) |
| Coordenadas dos locais (distâncias) | `eleitorado_local_votacao_2026.zip` (endereço novo) + arquivo de 2024 (endereço anterior) | [Dados Abertos TSE — Eleitorado 2026](https://dadosabertos.tse.jus.br/dataset/eleitorado-2026) |

## Método (resumo)

- Percentuais sobre **votos válidos** (brancos e nulos excluídos).
- **Peso**: fatia do voto do candidato no Maranhão que saiu dessas 204 seções.
- **Distância**: linha reta (haversine) entre as **coordenadas oficiais do TSE** do local antigo e do novo, validadas pela caixa geográfica do MA (0 m = mesmo prédio). Entram nas médias as **196 de 204** seções com as duas pontas identificadas (≈97% dos votos válidos). As 8 restantes aparecem como indisponível.
- Em 3 municípios (Anapurus, Paulino Neves e São José dos Basílios) o total de votos do 1º turno supera o eleitorado listado para o 2º turno; nesses casos mostramos só o total de votos, sem percentual.

Página independente, sem vínculo com o TSE. Em caso de divergência, prevalece a informação oficial do TRE-MA/TSE.

