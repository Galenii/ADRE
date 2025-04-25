# ADRE

**Centralização de Logs com Rsyslog**
- Este projeto tem como objetivo configurar um servidor de logs centralizado usando o rsyslog em uma rede local. A solução permite que múltiplos computadores clientes enviem suas mensagens de log para um único servidor, facilitando o monitoramento e a análise de eventos em tempo real.

**O que foi feito**
- Configuração de um servidor Linux para receber logs via protocolo UDP (porta 514).
 
- Modificação dos arquivos de configuração do rsyslog tanto no servidor quanto nos clientes.

- Criação de uma regra no servidor para armazenar logs recebidos em um arquivo separado (/var/log/clients.log).

- Testes de envio de logs entre clientes e servidor com sucesso.
