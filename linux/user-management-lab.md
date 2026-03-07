# Linux User Management Lab

Pequeno laboratório sobre gerenciamento de usuários no Linux.

## Criar usuário

sudo useradd testuser

## Definir senha

sudo passwd testuser

## Verificar usuário criado

cat /etc/passwd | grep testuser

## Remover usuário

sudo userdel testuser
