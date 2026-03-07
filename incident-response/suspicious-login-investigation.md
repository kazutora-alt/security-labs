# Suspicious Login Investigation

Laboratório simples de investigação de login suspeito em um sistema Linux.

## Ver histórico de logins

last

## Ver tentativas de autenticação

cat /var/log/auth.log

## Procurar logins falhados

grep "Failed password" /var/log/auth.log

## Ver atividades do usuário

lastlog
