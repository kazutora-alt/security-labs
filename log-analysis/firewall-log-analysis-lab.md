# Firewall Log Analysis Lab

## Objetivo

Analisar logs de firewall para identificar atividades suspeitas na rede.

## Exemplo de log

BLOCK TCP 192.168.1.50 -> 192.168.1.10 PORT 22

## Procurar conexões bloqueadas

grep "BLOCK" firewall.log

## Identificar IPs que tentam acessar muitas portas

awk '{print $3}' firewall.log | sort | uniq -c | sort -nr

## O que procurar

- IP tentando muitas portas
- muitas conexões bloqueadas
- atividade repetitiva
