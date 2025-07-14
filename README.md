# Analisador de Sentimentos para Google Sheets via Groq AI

Este projeto é um script Google Apps Script que permite analisar automaticamente sentimentos em feedbacks de clientes diretamente em uma planilha Google Sheets, utilizando a API Groq com o modelo Llama3.

---

## Funcionalidades

- Cria um menu personalizado chamado **✉️ Analisar Sentimentos** no Google Sheets.
- Analisa a coluna **"Resposta do Cliente"** para identificar:
  - Sentimento (positivo, negativo, neutro)
  - Grau de confiança da análise
  - Categoria do feedback (ex: elogio, reclamação, sugestão)
  - Emoção predominante (ex: alegria, tristeza, raiva)
  - Palavras-chave mais relevantes do texto
- Preenche automaticamente novas colunas na planilha com os resultados da análise.
- Gera uma aba/resumo chamada **Resumo Sentimentos** com "big numbers" dos principais indicadores:
  - Total de feedbacks analisados
  - Quantidade e porcentagem de feedbacks positivos, negativos e neutros
  - Taxa de satisfação geral

---

## Como usar

1. Abra sua planilha Google Sheets contendo uma coluna chamada **Resposta do Cliente** com os textos a serem analisados.
2. No editor de scripts do Google Sheets (`Extensões > Apps Script`), copie e cole o código deste projeto.
3. Substitua o valor da variável `GROQ_API_KEY` pela sua chave de API válida da Groq.
4. Salve o script.
5. Atualize a planilha para que o menu personalizado apareça.
6. No menu **✉️ Analisar Sentimentos**, clique em **Iniciar Análise** para executar a análise dos feedbacks.

---

## Requisitos

- Conta com acesso à API Groq ([https://groq.com](https://groq.com)) e chave de API válida.
- Planilha Google Sheets com coluna **Resposta do Cliente** preenchida.
- Permissões para execução de scripts e acesso à internet pela planilha.

---

## Exemplo de resposta esperada da IA

O script envia para a API um prompt que pede a análise com o seguinte formato (sem explicações extras):

 
---

## Como funciona o script

- Lê todas as respostas da coluna **Resposta do Cliente**.
- Para cada resposta, envia um prompt para a API Groq solicitando a análise detalhada.
- Processa a resposta e preenche as colunas correspondentes na mesma linha.
- Conta e acumula os resultados para exibir um resumo final.
- Cria ou atualiza uma aba **Resumo Sentimentos** com indicadores chave.

---

## Possíveis melhorias

- Personalizar o prompt para o seu negócio específico.
- Ajustar o modelo ou parâmetros da API para melhor desempenho.
- Adicionar mais visualizações e gráficos direto na planilha.
- Integrar com outras fontes de dados para análise combinada.

---

## Contato

Desenvolvido por Gabriel Lima Procópio — entre em contato para dúvidas ou sugestões no meu LinkedIn.

---

## Licença

MIT License — Sinta-se livre para usar e adaptar o código conforme sua necessidade.


