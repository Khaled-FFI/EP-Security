    ```markdown
# Metasploitable 2 - Notes de TP

## Objectif
Analyser les services vulnérables de Metasploitable 2 et comprendre les failles.

## Services vulnérables observés
- VSFTPD 2.3.4 (backdoor)
- Apache Tomcat (faibles identifiants)
- Samba (partages non sécurisés)
- MySQL (mot de passe root faible)
- Mutillidae (application volontairement vulnérable)

## Exemple : VSFTPD Backdoor
Port : 21  
Version vulnérable : 2.3.4  
Comportement : ouverture d’un shell sur le port 6200 après un login contenant `:)`.

## Exemple : Mutillidae
Vulnérabilités testées :
- XSS
- SQL Injection
- CSRF
- Command Injection

## Ce que j'ai appris
- Scanner un réseau avec Nmap  
- Identifier les versions vulnérables  
- Comprendre les failles courantes  
- Documenter un TP de sécurité
