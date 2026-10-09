# Estudos de Linux e Shell Script (Alura)

Scripts em Bash desenvolvidos durante os cursos de Linux da Alura, feitos acompanhando as aulas. Este repositório registra meus estudos em automação, processamento de logs e monitoramento de sistemas.

## Estrutura

```
processamento-logs/
    processamento-logs.sh
monitoramento-sistema/
    monitoramento-sistema.sh
```

## Scripts

### `processamento-logs/`
Curso: *Linux: criando script para processamento de arquivos de logs*

- Localiza todos os arquivos `.log` de uma pasta com `find`
- Filtra as linhas de erro e as que contêm dados sensíveis com `grep`
- Mascara senhas, tokens, chaves de API e dados de cartão com `sed`, substituindo os valores por `REDACTED`
- Ordena e remove linhas duplicadas com `sort` e `uniq`
- Gera estatísticas de linhas e palavras de cada arquivo com `wc`
- Combina os logs em um único arquivo, identificando a origem com os prefixos `[FRONTEND]` e `[BACKEND]`

Espera os logs em `../myapp/logs` e grava os resultados em `../myapp/logs-processados`.

### `monitoramento-sistema/`
Curso: *Linux: criando script de monitoramento de sistema*

- **Logs:** procura falhas, erros e acessos negados em `/var/log/syslog` e `/var/log/auth.log`
- **Rede:** testa a conectividade com `ping` e o acesso a um site com `curl`
- **Disco:** alerta partições acima de 70% de uso e mostra o tamanho da pasta pessoal
- **Hardware:** registra uso de memória RAM, CPU e operações de leitura e escrita em disco

Os resultados ficam na pasta `monitoramento_sistema`, criada onde o script é executado.

## Como rodar

```bash
cd processamento-logs
chmod +x processamento-logs.sh
./processamento-logs.sh
```

```bash
cd monitoramento-sistema
chmod +x monitoramento-sistema.sh
sudo ./monitoramento-sistema.sh
```

O monitoramento precisa de `sudo` para ler `/var/log/auth.log` e do pacote `sysstat` para o comando `iostat`:

```bash
sudo apt install sysstat
```

Testado em distribuições baseadas em Debian/Ubuntu. Em sistemas sem `/var/log/syslog`, a parte de logs não encontra o arquivo.

## O que aprendi

- Navegação, permissões e execução de scripts no terminal
- Busca e filtragem de texto com `grep` e expressões regulares
- Edição de texto em fluxo com `sed` e extração de colunas com `awk`
- Percorrer arquivos com `find` e laços `while read`
- Funções, condicionais e redirecionamento (`>` e `>>`) em Bash
- Ordenação, remoção de duplicatas e contagem com `sort`, `uniq` e `wc`
- Comandos de monitoramento: `df`, `du`, `free`, `top`, `iostat`, `ping`, `curl`

## Próximos passos

- Mascarar os dados sensíveis antes de gravar qualquer arquivo em disco
- Usar caminhos absolutos para os scripts funcionarem de qualquer pasta
- Evitar duplicar resultados ao rodar o processamento mais de uma vez no mesmo dia
- Verificar se as dependências estão instaladas antes de rodar o monitoramento
- Agendar o monitoramento com `cron`

## Tecnologias

Bash · Linux · grep · sed · awk
