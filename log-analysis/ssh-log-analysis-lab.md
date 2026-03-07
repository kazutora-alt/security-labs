# SSH Log Analysis Lab

## Objetivo

Analisar logs SSH para identificar tentativas de acesso suspeitas.

## Ver tentativas de login

cat /var/log/auth.log

## Procurar logins falhados

grep "Failed password" /var/log/auth.log

## Procurar logins bem-sucedidos

grep "Accepted password" /var/log/auth.log

## Identificar IPs suspeitos

grep "Failed password" /var/log/auth.log | awk '{print $11}' | sort | uniq -c

## O que procurar

- Muitos logins falhados
- IP desconhecido
- Várias tentativas em poucos segundos

Isso pode indicar tentativa de brute force.
