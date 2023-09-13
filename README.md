# HVN


Instalação

:: Instalação normal, escolher senha forte (aBa1#cDaTxh39)
:: Alterar NOME / DOMINIO
:: Habilitar área de trabalho remota
:: Telemetria Completa

:: ACESSAR POWERSHELL ::


:: Regras de Firewall para Gerenciar de outra Maquina ::

 

Sistema Operacional em Inglês:
Set-NetFirewallRule -DisplayGroup "Windows Management Instrumentation (WMI)" -Enabled True
Set-NetFirewallRule -DisplayGroup "Remote Event Log Management" -Enabled True
Set-NetFirewallRule -DisplayGroup "Remote Service Management" -Enabled True
Set-NetFirewallRule -DisplayGroup "File and Printer Sharing" -Enabled True
Set-NetFirewallRule -DisplayGroup "Remote Scheduled Tasks Management" -Enabled True
Set-NetFirewallRule -DisplayGroup "Performance Logs and Alerts" -Enabled True
Set-NetFirewallRule -DisplayGroup "Remote Volume Management" -Enabled True
Set-NetFirewallRule -DisplayGroup "Windows Firewall Remote Management" -Enabled True

 

Sistema Operacional em Português:
Set-NetFirewallRule -DisplayGroup "Instrumentação de Gerenciamento do Windows (WMI)" -Enabled True
Set-NetFirewallRule -DisplayGroup "Gerenciamento Remoto do Log de Eventos" -Enabled True
Set-NetFirewallRule -DisplayGroup "Gerenciamento Remoto de Serviços" -Enabled True
Set-NetFirewallRule -DisplayGroup "Compartilhamento de Arquivo e Impressora" -Enabled True
Set-NetFirewallRule -DisplayGroup "Gerenciamento Remoto de Tarefas Agendadas" -Enabled True
Set-NetFirewallRule -DisplayGroup "Logs e Alertas de Desempenho" -Enabled True
Set-NetFirewallRule -DisplayGroup "Gerenciamento de Volumes Remoto" -Enabled True

 

Caso dê erro:
Set-NetFirewallRule -DisplayGroup "Gerenciamento Remoto do Windows Defender Firewall" -Enabled True

:: ACESSAR CMD ::


:: DISKPART ::

 

list disk
select disk
clear
create partition primary
list volume
select volume
active
assign letter =D
format quick

 

:: CONFIGURAR 2 PORTAS ETHERNET EM 1 VIRTUAL TEAM / MULTIPLEXOR ::

Get-NetAdapter
New-NetSwitchTeam -Name "2Gbps" -TeamMembers "Ethernet","Ethernet 4"
Get-NetSwitchTeam
