# Failed Login Detection Lab

Laboratório para identificar tentativas de login falhadas no Linux.

## Procurar falhas de autenticação

grep "Failed password" /var/log/auth.log

## Contar número de falhas

grep "Failed password" /var/log/auth.log | wc -l

## Ver IPs que tentaram login

grep "Failed password" /var/log/auth.log | awk '{print $11}'
