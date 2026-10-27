# Plano da atividade N2

Tema escolhido pelo usuário: previsão do consumo de energia industrial.

## Entrega e escopo

Notebook em português, executado e compatível com Google Colab, com introdução, metodologia, desenvolvimento, resultados, discussão e referências. README com instruções de reprodução e entrega. Dados públicos da UCI, com atribuição CC BY 4.0. Não há necessidade de aplicação web, API ou banco externo.

## Decisões de implementação

- Prever kWh de um intervalo de 15 minutos usando histórico encerrado antes dele e calendário conhecido.
- Separar os exemplos temporalmente: 70% treino, 15% validação e 15% teste, depois de formar as variáveis históricas.
- Comparar persistência, sazonalidade diária, Ridge e HistGradientBoostingRegressor.
- Selecionar pelo MAE de validação e reajustar o vencedor com treino e validação. Consultar o teste apenas na avaliação final.
- Usar previsões sequenciais de um passo: as observações dos intervalos anteriores ficam disponíveis ao longo do teste. Não declarar previsão de um dia inteiro antecipadamente.
- Não usar medições contemporâneas de potência reativa, fatores de potência, emissões ou classificação de carga como preditores futuros.
- Interpretar as 365 meias-noites ao fim dos blocos diários como encerramento do dia; acrescentar um dia ao timestamp, preservar a ordem original e validar a sequência contínua de 15 minutos. Documentar esta convenção como hipótese sobre a fonte.
- Não afirmar economia monetária ou redução real de consumo sem intervenção, tarifa e avaliação próprias.

## Verificações

- [x] Conferir esquema, ordenação, frequência, ausências e duplicidades dos dados originais.
- [x] Validar causalidade das defasagens e isolamento temporal dos conjuntos.
- [x] Executar todas as células em kernel limpo e verificar a ausência de erros.
- [x] Conferir métricas, arquivos exportados e gráficos gerados.
- [x] Conferir cobertura dos requisitos do enunciado e instruções para link público.

Verificação final: 27 células, das quais 12 executáveis, sem erros ou avisos nas saídas; cinco figuras; métricas recalculadas e modelo salvo conferidos. Pacote ZIP validado. A revisão independente identificou a ambiguidade das meias-noites, que foi normalizada e documentada antes da execução final.

Publicação autorizada pelo usuário em 27/10/2026: https://github.com/JHBruhmuller/n2-previsao-energia-industrial. Os nomes dos integrantes ainda precisam ser preenchidos.
