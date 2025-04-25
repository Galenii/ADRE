# ADRE

📡 Centralização de Logs com Rsyslog
Este projeto tem como objetivo configurar um servidor de logs centralizado usando o rsyslog em uma rede local. A solução permite que múltiplos computadores clientes enviem suas mensagens de log para um único servidor, facilitando o monitoramento e a análise de eventos em tempo real.

🛠️ O que foi feito
Configuração de um servidor Linux para receber logs via protocolo UDP (porta 514).

Modificação dos arquivos de configuração do rsyslog tanto no servidor quanto nos clientes.

Criação de uma regra no servidor para armazenar logs recebidos em um arquivo separado (/var/log/clients.log).

Testes de envio de logs entre clientes e servidor com sucesso.

🌐 Como os clientes podem enviar logs
Acesse o arquivo /etc/rsyslog.conf no cliente:

bash
Copiar
Editar
sudo nano /etc/rsyslog.conf
Adicione ao final do arquivo:

graphql
Copiar
Editar
*.* @192.168.1.100:514
(Substitua o IP pelo IP real do seu servidor.)

Reinicie o serviço:

bash
Copiar
Editar
sudo systemctl restart rsyslog
Envie uma mensagem de teste:

bash
Copiar
Editar
logger "Teste de envio de log"
📍 IP do Servidor
192.168.1.100 (modificável conforme sua rede)

🧪 Resultado
Logs enviados por qualquer cliente aparecem no servidor em tempo real e ficam salvos no arquivo /var/log/clients.log.
