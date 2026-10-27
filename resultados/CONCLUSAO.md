# Síntese dos resultados

O método selecionado pela validação foi **HistGradientBoosting**. No teste temporal com
5,156 intervalos, entre 08/11/2018 07:15 e
01/01/2019 00:00, obteve **MAE de 3.8957 kWh por intervalo**,
**RMSE de 7.9050 kWh** e
**R² de 0.9361**. O resultado representa redução de 22.01% do MAE frente à persistência.

Nos 302 intervalos de consumo elevado,
o MAE foi **17.2832 kWh**,
com viés de **14.5872 kWh**.
Nos demais intervalos, o MAE foi
**3.0628 kWh**.
O viés positivo nos maiores consumos indica tendência de subestimação nesse grupo.
Por isso, a boa média geral não garante antecipação confiável dos picos.

O estudo demonstra uma aplicação reproduzível de ciência de dados ao monitoramento
energético industrial, com dados públicos, preparação temporal e avaliação posterior
ao treinamento. Os resultados são restritos à previsão sequencial de um intervalo
de 15 minutos nesta base. A eficácia em outra fábrica e eventual economia exigem
validação operacional e avaliação da intervenção.

O modelo pode apoiar o planejamento, mas não prova redução de gastos, consumo ou
emissões. Sua adoção deve considerar os erros de pico, a atualização das medições
e a comparação continuada com referências simples.
