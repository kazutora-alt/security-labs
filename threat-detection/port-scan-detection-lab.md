# Port Scan Detection Lab

Laboratório para identificar possíveis varreduras de portas na rede.

## Procurar conexões suspeitas

netstat -ant

## Ver tentativas de conexão repetidas

netstat -ant | grep SYN

## Identificar IPs conectando em muitas portas

netstat -ant | awk '{print $5}' | cut -d: -f1 | sort | uniq -c | sort -n
