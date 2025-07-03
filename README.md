# Desafio de Projeto DIO Randstad-Analise Dados
Desafio de Projeto sobre Analise de Sentimentos utilizando Language Studio no Azure AI.

# Análise de Sentimentos com Language Studio no Azure AI
Este guia mostra como usar o Azure AI Language Studio para executar análises de sentimento e opinião em textos de forma interativa, sem escrever código.

## 1. Introdução
A análise de sentimento e a mineração de opinião são recursos do Serviço de Linguagem do Azure que classificam textos como positivos, neutros ou negativos, além de extrair aspectos específicos mencionados no texto (por exemplo, atributos de produto) e fornecer uma pontuação de confiança para cada instância analisada.

## 2. Pré-requisitos
- Assinatura ativa no Azure.
- Permissão para criar recursos no grupo de recursos desejado.
- Navegador com acesso ao portal do Azure e ao Language Studio.

## 3. Criar o recurso de Language Service
1. Clique [aqui](https://portal.azure.com/#home) para acessar Portal Azure.(https://portal.azure.com/#home)
2. Clique em Create a resource.
3. Busque por “Language” e selecione Azure AI Language.
4. Preencha:
    - Subscription
    - Resource group (ou crie um novo)
    - Nome único para o recurso
    - Pricing tier: Free F0 (se disponível)
    - Clique em Review + create e depois em Create para provisionar o serviço.

## 4. Conectar-se ao Language Studio
  1. Clique [aqui](https://language.cognitive.azure.com/) para conectar-se (https://language.cognitive.azure.com/)
  2. Faça login com sua conta Azure.
  3. Na primeira vez, será solicitada a associação de um recurso existente:
  4. Selecione:
     - Subscription
     - Resource Type (Language)
     - Resource group criado anteriormente.
     - Clique em Done para conectar o estúdio ao seu serviço de linguagem na nuvem.

## 5. Passo a passo no Language Studio
1. No menu lateral, vá em Classify text.
2. Clique em Analyse sentiment and mine opinions.
3. Escolha o idioma do texto (por exemplo, English ou Português).
4. Cole o texto de exemplo na caixa de entrada. Por exemplo:
5. Clique em Run para ver:
    - Rótulo de sentimento geral (positivo, neutro, negativo)
    - Pontuação de confiança (0.0–1.0)
    - Frases e aspectos específicos extraídos (p.ex., “room furnishings”, “internet”) e seus sentimentos relacionados1.

## 6. Exemplo de resultados

Frase                                                | Sentimento | Score
---------------------------------------------------- | :--------: |:-----:
“room furnishings are average – becoming a bit old”  | Negativo   | 0.12  
“internet didn't work”                               | Negativo   | 0.05
Sentimento geral do documento                        | Negativo   | 0.15

Esses retornos ajudam a diagnosticar quais partes do texto geram reclamações ou elogios.






## 7. Boas práticas e próximos passos
  - Teste textos de diferentes comprimentos e estilos para calibrar o limite de confiança ideal.
  - Explore a Opinion Mining para obter análises de subcomponentes do texto (aspect-based sentiment).
  - Para integrações em produção, utilize a API REST ou SDKs (C#, Java, Python) conforme a documentação oficial do Azure AI Language Service.
  - Avalie usar o Azure Synapse Analytics para enriquecer grandes volumes de dados textuais com análise de sentimento em escala.
  - Experimente variações de texto, compare idiomas e documente suas descobertas no README do seu repositório para futuras referências.

## 8. Links Úteis
https://learn.microsoft.com/pt-br/azure/ai-services/language-service/sentiment-opinion-mining/overview

https://github.com/daniel-trezena/analise-sentimentos-azure-AI

https://learn.microsoft.com/pt-br/azure/synapse-analytics/machine-learning/tutorial-cognitive-services-sentiment

https://bing.com/search?q=An%c3%a1lise+de+Sentimentos+com+Language+Studio+no+Azure+AI





