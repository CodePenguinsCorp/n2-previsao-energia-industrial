# Origem dos dados

- Conjunto: **Steel Industry Energy Consumption**.
- Autores: Sathishkumar V E, Changsun Shin e Yongyun Cho.
- Repositório: UCI Machine Learning Repository, conjunto 851.
- Referência: V E, S.; Shin, C.; Cho, Y. (2021). *Steel Industry Energy Consumption* [Dataset]. https://doi.org/10.24432/C52G8C.
- Página: https://archive.ics.uci.edu/dataset/851/steel+industry+energy+consumption.
- Download: https://archive.ics.uci.edu/static/public/851/steel%2Bindustry%2Benergy%2Bconsumption.zip.
- Acesso: 27/10/2026.
- Licença: Creative Commons Attribution 4.0 International, https://creativecommons.org/licenses/by/4.0/.
- SHA-256 do CSV bruto: `9b1cee6f9cb9cd9df2b95814ca90a9a2ff15b7f5f1fba0fae3c643e82072eacc`.

`raw/Steel_industry_data.csv` é uma cópia sem alteração do CSV distribuído pela UCI, com a codificação original. O notebook calcula atributos derivados, previsões e métricas, documentando essas transformações. A licença e a atribuição devem acompanhar a redistribuição dos dados.

O conjunto representa medições de consumo de uma siderúrgica na Coreia do Sul. Não é coleta realizada pelos integrantes deste trabalho. Consulte a fonte para os detalhes de obtenção. O campo de emissões apresenta inconsistência entre nome e unidade na ficha e não é usado no modelo.

## Convenção temporal adotada

Na ordem original, os 96 registros de cada dia começam em `00:15` e terminam em `00:00`, ainda com a data do mesmo dia. O notebook interpreta essa última leitura como encerramento do dia e acrescenta um dia apenas a essas 365 meias-noites. A sequência resultante vai de 01/01/2018 00:15 a 01/01/2019 00:00, sem lacunas e sem reordenar linhas. Calendário e defasagens são calculados depois dessa normalização.

Essa interpretação é uma hipótese apoiada na ordem dos registros, não uma confirmação do processo de aquisição. O arquivo bruto e seus valores são preservados; a transformação ocorre em memória e é registrada na auditoria. Antes de uso operacional, a convenção deve ser confirmada com o responsável pelos dados.
