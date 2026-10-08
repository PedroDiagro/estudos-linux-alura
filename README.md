#Estudos de Linux e Shell Script (Alura)

Scripts em Bash desenvolvidos durante os cursos de Linux da Alura, feitos acompanhando as aulas. Este repositório registra meus estudos em automação e processamento de logs.

Scripts
processamento-logs.sh

Curso: Linux: criando script para processamento de arquivos de logs

1- Localiza todos os arquivos .log de uma pasta com find

2- Filtra as linhas de erro e as que contêm dados sensíveis com grep

3- Mascara senhas, tokens, chaves de API e dados de cartão com sed, substituindo os valores por REDACTED

4- Ordena e remove linhas duplicadas com sort e uniq

5- Gera estatísticas de linhas e palavras de cada arquivo com wc

6- Combina os logs em um único arquivo, identificando a origem com os prefixos [FRONTEND] e [BACKEND]

7- Espera os logs em ../myapp/logs e grava os resultados em ../myapp/logs-processados.

**O que aprendi**

•Navegação, permissões e execução de scripts no terminal

•Busca e filtragem de texto com grep e expressões regulares

•Edição de texto em fluxo com sed

•Percorrer arquivos com find e laços while read

•Condicionais e redirecionamento (> e >>) em Bash

•Ordenação, remoção de duplicatas e contagem com sort, uniq e wc
