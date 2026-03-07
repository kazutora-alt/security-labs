# Linux Log Analysis Lab

Pequeno laboratório para visualizar e analisar logs no Linux.

## Ver últimas tentativas de login

sudo last

## Ver log de autenticação

sudo cat /var/log/auth.log

## Monitorar logs em tempo real

sudo tail -f /var/log/syslog

## Procurar falhas de login

sudo grep "Failed password" /var/log/auth.log
