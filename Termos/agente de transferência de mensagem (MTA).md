### 2. MTA (Mail Transfer Agent) - O Transportador

O **MTA** é o "motor" que move o e-mail pela internet. Ele é um software de servidor que transfere mensagens de um computador para outro usando o protocolo **SMTP** (Simple Mail Transfer Protocol).

- **O que faz:** Ele olha para o endereço de destino (ex: @empresa.com), consulta o DNS para saber para onde enviar e despacha a mensagem para o próximo MTA até chegar ao destino.
    
- **Analogia:** São os caminhões e aviões dos correios que levam a carga de uma cidade para outra.
    
- **Importância nos Metadados:** Como você leu no texto, **cada MTA que processa o e-mail adiciona uma linha de cabeçalho "Received"**. Isso permite que um investigador rastreie por quais servidores (IPs) a mensagem passou, identificando a origem real de um ataque de phishing.