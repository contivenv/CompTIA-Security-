No entanto, muitos administradores optam por alterar as portas padrão e escolhem um método para obscurecê-las. O TCP (Transmission Control Protocol, protocolo de controle de transmissão) e o UDP (User Datagram Protocol, protocolo de datagrama de usuário) são dois métodos de transporte principais. O TCP é orientado para a conexão e oferece confiabilidade, ordenação e verificação de erros, tornando-o adequado para aplicativos que exigem altos níveis de confiabilidade. O UDP não tem conexão, o que o torna mais rápido que o TCP e mais adequado para aplicativos em tempo real, como streaming de vídeo, telefonia e jogos, onde a perda ocasional de pacotes é menos impactante.

Me dê um exemplo de aplicativo que exige altos níveis de confidencialidade (que use o TCP) e faça o mesmo dando um exemplo para o UDP.

Professora de cibersegurança

Gem personalizado

- Pergunta respondida com sucesso
    

Olá, querido. Vamos direto ao ponto, porque tempo é a única coisa que não conseguimos criptografar e recuperar depois. 💋

Você tocou na ferida: a eterna briga entre a segurança "certinha" e a velocidade "quero tudo pra agora". No mundo real, a gente escolhe nossas batalhas (e nossos protocolos) baseando-se no que dói mais perder.

Aqui estão os exemplos práticos que você pediu, com aquele toque de realidade ácida que só quem já viu um servidor sangrar consegue dar:

### 1. O Exemplo do TCP: Acesso ao seu Internet Banking 🏦💸

Quando você entra no aplicativo do seu banco para transferir aquele Pix, o mundo **não pode** se dar ao luxo de ter um erro de bit. Imagine se um pacote com o valor "R$ 1.000,00" perde o último zero no caminho? Um desastre, certo?

- **Por que TCP?** Ele é o protocolo "perfeccionista". O aplicativo usa o **HTTPS** (que roda sobre o TCP na porta 443) porque exige uma conexão confiável onde cada pacote é numerado e confirmado. Se algo se perde ou chega torto, o TCP manda reenviar.
    
- **A Confidencialidade:** Aqui entra o **TLS**. O TCP garante que os dados cheguem inteiros, e o TLS (a camada sexy de criptografia por cima) garante que ninguém, além de você e o banco, saiba quanto você tem na conta. Sem TCP, a criptografia nem conseguiria montar o quebra-cabeça da chave de sessão.
    

### 2. O Exemplo do UDP: Aquela chamada de vídeo (ou o "zap" de voz) 📹🔥

Sabe quando você está numa chamada de vídeo e a imagem dá aquela "quadriculada" ou o áudio engasga por um milésimo de segundo, mas a vida segue? Isso é o UDP em ação.

- **Por que UDP?** Ele é o protocolo "desapegado". Ele não está nem aí se um pacote caiu no chão; ele quer entregar o próximo **agora**. Para aplicações em tempo real, como **VoIP** ou **streaming**, esperar um pacote atrasado ser retransmitido (como o TCP faria) causaria um atraso insuportável no áudio.
    
- **O uso prático:** Aplicativos de conferência usam UDP para a mídia (voz/vídeo). Se 1% dos dados se perder, seu cérebro ignora a falha. É melhor um frame faltando do que a conversa pausar por 2 segundos enquanto o protocolo "pede desculpas" e tenta reenviar o que já passou.
    

---

**Minha opinião contundente:** Administradores que acham que "obscurecer" portas trocando a 80 pela 8080 é "segurança" estão apenas brincando de esconde-esconde com um invasor que tem visão de raio-x (scanners de vulnerabilidade). Segurança de verdade é protocolo bem configurado e criptografia de gente grande, não trocar o número da porta para tentar enganar script kiddie.