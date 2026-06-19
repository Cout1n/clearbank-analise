# 📊 Análise e Limpeza de Transações Financeiras
 
Projeto de análise de dados desenvolvido em Python que processa o histórico mensal de transações de clientes exportado em CSV. O sistema lê o arquivo, valida e limpa os dados, identifica transações suspeitas, gera um relatório consolidado em JSON e produz um gráfico com a distribuição de créditos e débitos por mês.

## ▶️ Como executar
 
### Google Colab
 
1. Acesse [colab.research.google.com](https://colab.research.google.com) e faça login com sua conta Google.
2. Clique em **Arquivo -> Fazer upload de notebook** e selecione `desafio_final.ipynb`.
3. No painel lateral, clique no ícone de pasta e faça upload de um arquivo CSV contendo as transações financeiras`transacoes.csv`.
4. No menu superior, clique em **Ambiente de execução -> Executar tudo**.

## 📦 O que é gerado como saída

Após a execução, o projeto gera:
### Terminal

Relatório formatado com:

Período analisado (data inicial -> final), 
Total de transações válidas e inválidas, 
Resumo mensal (créditos, débitos, saldo), 
Lista de transações suspeitas.

### Arquivo JSON (relatorio.json)
Contém:
Resumo mensal das transações, 
Totais consolidados, 
Lista de transações suspeitas.

### Gráfico (grafico.png)
Visualização da movimentação mensal, 
Comparação entre créditos e débitos, 
Inclui:
Título, 
Rótulos dos eixos, 
Legenda.


## ⚙️  Regras de validação
 
Cada linha do CSV passa pelas seguintes verificações antes de ser processada: 

Campo  Regra 
 id = Não vazio e numérico  
 cliente_id = Não vazio  
 data = Formato AAAA-MM-DD válido  
 tipo = Deve ser credito ou debito 
 valor = Numérico e maior que zero 
 
Linhas que violam qualquer regra são descartadas silenciosamente (sem interromper a execução) e listadas no relatório de limpeza.
