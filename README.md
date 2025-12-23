# Séries Temporais: Análise de Volume e Impacto de Variáveis Exógenas

Este repositório documenta nossa jornada de modelagem estatística para a disciplina de Séries Temporais na FGV EMAp. O projeto foi estruturado em duas fases principais, evoluindo de uma compreensão univariada básica para sistemas preditivos multivariados complexos.

## Nossa Linha de Raciocínio

A análise foi guiada pelo rigor estatístico, seguindo este fluxo de implementação:

### Fase 1: Análise Exploratória e Suavização (A1)
Iniciamos com o tratamento de uma série temporal de volume, onde realizamos a decomposição STL para isolar tendência, sazonalidade e ruído. Nesta etapa, exploramos a modelagem via Suavização Exponencial Simples e o método de Holt, buscando capturar a tendência de crescimento dos dados. A validação inicial nos permitiu entender a inércia da série e a estabilidade dos parâmetros de suavização.

### Fase 2: Modelagem Avançada e SARIMAX (A2)
Na segunda fase, elevamos a complexidade ao incorporar variáveis exógenas (`users` e `inv`). Nossa hipótese foi que o volume não era apenas dependente de seu passado, mas também do fluxo de usuários e investimentos. 
- **Estacionariedade:** Aplicamos testes de Dickey-Fuller Aumentado (ADF) e realizamos as diferenciações necessárias para estabilizar a variância e a média.
- **Modelagem:** Implementamos modelos SARIMAX para capturar tanto a sazonalidade sazonal quanto o impacto imediato das variáveis externas. 
- **Validação:** Utilizamos a técnica de *Walk-Forward Validation*, que simula o uso real do modelo em produção, prevendo um passo à frente e re-treinando o modelo, o que nos deu métricas de erro (MAE e RMSE) muito mais confiáveis.

## Conclusões Técnicas
Através do diagnóstico de resíduos (Ljung-Box e análise de normalidade), garantimos que os modelos não estavam deixando informações "na mesa". A inclusão de variáveis exógenas provou-se fundamental para reduzir o erro de previsão, demonstrando que o volume de transações é fortemente correlacionado ao engajamento da base de usuários.

## Integrantes
* **Gustavo Bianchi**
* **Guilherme Buss**
* **Guilherme Carvalho**
* **João Gabriel**
* **Luís Felipe Marciano**
* **Vinícius Nascimento**
