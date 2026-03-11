# Network Scan Lab

## Descoberta de hosts na rede

Comando utilizado:

sudo nmap -sn 192.168.24.0/24

Resultado:

Host: 192.168.24.1  (Gateway)
Host: 192.168.24.3
Host: 192.168.24.7  (Minha máquina)

---

## Scan de portas

sudo nmap 192.168.24.3

Resultado:
All 1000 scanned ports closed.

---

## Verificação ARP

ip neigh
arp -a

Dispositivos encontrados:
192.168.24.1
192.168.24.3

---

## Firewall logs

sudo tail ufw.log

Exemplo de evento:

[UFW BLOCK] SRC=192.168.24.3 DST=192.168.24.7 PROTO=TCP SYN
