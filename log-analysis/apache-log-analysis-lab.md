# Apache Log Analysis Lab

## Objetivo

Analisar logs de servidor web para detectar atividades suspeitas.

## Exemplo de log

192.168.1.10 - - [10/Oct/2024:13:55:36] "GET /login.php HTTP/1.1" 200

## Ver logs do servidor

cat /var/log/apache2/access.log

## Procurar IPs que acessam muito

awk '{print $1}' /var/log/apache2/access.log | sort | uniq -c | sort -nr

## Procurar scanners

grep "sqlmap" /var/log/apache2/access.log

## O que procurar

- Muitos acessos do mesmo IP
- Ferramentas de scanner
- Requisições estranhas
