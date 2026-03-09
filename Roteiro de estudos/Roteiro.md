Com a nova data alvo de **5 de junho de 2026** (daqui a exatamente 97 dias, ou cerca de **14 semanas**) e usando o seu **Linux Mint** com essa excelente configuração de hardware, o cenário muda um pouco, mas para melhor!

Sua máquina (Ryzen 5 9600X + 16GB de RAM + RX 7600) é **perfeita para virtualização e testes pesados**. Com 16GB de RAM e esse processador de 6 núcleos fortíssimos, você pode rodar 2 ou 3 Máquinas Virtuais (VMs) ao mesmo tempo sem o sistema engasgar. Além disso, a RX 7600 é ótima caso você queira brincar com quebra de hashes (usando o _Hashcat_), algo que é citado nos módulos de criptografia e ataques a senhas do SY0-701.

Como mudamos do OpenSUSE para o **Linux Mint** (que é baseado no Ubuntu/Debian), nosso gerenciador de pacotes passa a ser o `apt`, o que facilita bastante, pois a maioria dos tutoriais de segurança foca no Debian/Ubuntu.

Como você tem 14 semanas até o dia 5 de junho e **quer descansar nos finais de semana**, teremos que agrupar alguns dos 16 módulos mais curtos para garantir que a última semana seja exclusiva para revisão.

Aqui está o seu **Plano de Estudos Atualizado e Oficializado (SY0-701) até 5 de Junho**:

---

### A Estrutura do Seu Home Lab Gratuito no Linux Mint

Antes de começar, prepare seu ambiente usando o terminal do Mint:

1. **Virtualização:** Como você tem um Ryzen 5 e 16GB de RAM, use o VirtualBox ou o KVM.
    
    - _Instalação:_ `sudo apt update && sudo apt install virtualbox`
        
    - _Alvos:_ Baixe a ISO do Kali Linux (para simular ataques) e a Metasploitable 2 (vítima). Reserve 2GB de RAM para o Kali e 1GB para a Metasploitable. Vai sobrar muita memória para o seu Mint.
        
2. **Ferramentas Oficiais exigidas pela CompTIA:**
    
    - _Instalação básica:_ `sudo apt install nmap wireshark tcpdump netcat-traditional openssl hashcat`
        
    - _Docker (para o OWASP Juice Shop - app web vulnerável):_ `sudo apt install docker.io` e depois `sudo docker run --rm -p 3000:3000 bkimminich/juice-shop`
        

---

### O Cronograma (Sem fins de semana) - 14 Semanas

_A rotina sugerida continua sendo de 1 hora por dia (Segunda a Sexta)._

#### Fase 1: Fundamentos e Ameaças (Semanas 1 a 3)

- **Semana 1 (2 a 6 de Março):** Módulos 1.0 (Conceitos) e 2.0 (Tipos de Ameaças).
    
    - _Foco Oficial:_ Diferenciar Controles de Segurança (Técnico, Administrativo, Físico) e Vetores de Ataque (Phishing, BEC, Cadeia de Suprimentos).
        
    - _Lab no Mint:_ Use o `nmap` na sua própria rede (`sudo nmap -sn 192.168.0.0/24`) para entender superfície de ataque.
        
- **Semana 2 (9 a 13 de Março):** Módulo 3.0 (Soluções Criptográficas).
    
    - _Foco Oficial:_ PKI, Hashing vs Encriptação, PFS (Perfect Forward Secrecy).
        
    - _Lab no Mint:_ Brinque com o OpenSSL no terminal (`openssl enc -aes-256-cbc -in arquivo.txt -out arquivo.enc`) e teste quebrar senhas fracas com o `hashcat` usando sua RX 7600.
        
- **Semana 3 (16 a 20 de Março):** Módulo 4.0 (Gestão de Identidade e Acesso).
    
    - _Foco Oficial:_ MFA, SSO, SAML, OAuth, Zero Trust.
        

#### Fase 2: Arquitetura e Defesa de Redes (Semanas 4 a 7)

- **Semana 4 (23 a 27 de Março):** Módulo 5.0 (Arquitetura de Rede).
    
    - _Foco Oficial:_ Posicionamento de Firewalls, WAF, Balanceadores de carga, VPN (IPSec vs TLS).
        
    - _Lab no Mint:_ Abra o Wireshark e capture pacotes enquanto navega para entender a diferença entre tráfego limpo e em túnel.
        
- **Semana 5 (30 de Março a 3 de Abril):** Módulo 6.0 (Nuvem e Confiança Zero).
    
    - _Foco Oficial:_ Matriz de responsabilidade em nuvem, SDN, IoT e OT.
        
- **Semana 6 (6 a 10 de Abril):** Módulo 7.0 (Resiliência) e Módulo 8.0 (Vulnerabilidades).
    
    - _Foco Oficial:_ Alta disponibilidade (RAID, Clustering), Backups e CVEs.
        
    - _Dica de TI:_ Lembre-se que na CompTIA, o processo de "Patch Management" é tão importante quanto o patch em si.
        
- **Semana 7 (13 a 17 de Abril):** Módulos 9.0 (Seg. de Rede) e 10.0 (Seg. de Endpoint).
    
    - _Foco Oficial:_ NAC, 802.1X, WPA3, Hardening e MDM.
        
    - _Lab no Mint:_ Explore as regras do UFW (Uncomplicated Firewall) nativo do Mint (`sudo ufw status`).
        

#### Fase 3: Operações e Resposta (Semanas 8 a 10)

- **Semana 8 (20 a 24 de Abril):** Módulo 11.0 (Segurança de Aplicativos).
    
    - _Foco Oficial:_ OWASP, injeção de SQL e XSS, protocolos seguros (DNSSEC, LDAPS).
        
- **Semana 9 (27 de Abril a 1 de Maio):** Módulo 12.0 (Monitoramento e Resposta a Incidentes).
    
    - _Foco Oficial:_ A ordem exata do plano de resposta (Preparação -> Detecção -> Contenção -> Erradicação -> Recuperação -> Lições). Análise Forense (Cadeia de Custódia).
        
- **Semana 10 (4 a 8 de Maio):** Módulo 13.0 (Indicadores de Atividades Maliciosas).
    
    - _Foco Oficial:_ Identificar se um ataque é DDoS, SQLi ou Ransomware lendo logs.
        
    - _Lab no Mint:_ Leia os logs do seu próprio sistema no diretório `/var/log` (ex: `tail -f /var/log/auth.log` e tente errar a senha do `su` de propósito para ver o log gerado).
        

#### Fase 4: Governança, Risco e Compliance - GRC (Semanas 11 a 13)

_Nesta fase, feche o terminal. O foco é leitura pura do E-book, pois é a parte burocrática._

- **Semana 11 (11 a 15 de Maio):** Módulo 14.0 (Governança).
    
    - _Foco Oficial:_ Políticas, Controle de Mudança (Change Management - NUNCA mude nada em produção sem aprovação na CompTIA!).
        
- **Semana 12 (18 a 22 de Maio):** Módulo 15.0 (Gestão de Riscos).
    
    - _Foco Oficial:_ Risco Quantitativo vs Qualitativo (SLE x ARO = ALE). Avaliação de Fornecedores.
        
- **Semana 13 (25 a 29 de Maio):** Módulo 16.0 (Proteção de Dados e Conformidade).
    
    - _Foco Oficial:_ Classificação de dados (PII, PHI), Leis de Privacidade (GDPR), DLP e treinamento de usuários.
        

#### Fase 5: Reta Final e Prova (Semana 14)

- **Semana 14 (1 a 4 de Junho):** * Sem estudo de material novo.
    
    - Revise os Flashcards/Anki de portas e protocolos de cor (Porta 22, 53, 67, 68, 80, 443, 3389, 636, etc.).
        
    - Faça as perguntas de revisão finais do e-book.
        
    - Procure vídeos no YouTube (de graça) sobre **"CompTIA Security+ SY0-701 PBQ"** (Performance-Based Questions). O exame terá de 3 a 5 perguntas práticas onde você precisará arrastar servidores para zonas de rede ou configurar regras de firewall simuladas.
        
- **5 DE JUNHO DE 2026 (Sexta-feira): O Dia da Prova!**
    
    - Durma bem. Confie nos seus 6 anos de experiência somados ao vocabulário da CompTIA que você adquiriu no Mint.
        

### Resumo da sua Rotina Diária Ideal:

1. **Segunda a Quinta:** Leia o e-book, faça anotações de siglas (RTO, RPO, MTTR) e execute um comando no terminal do Linux Mint relacionando ao que leu.
    
2. **Sexta-feira:** Responda as questões de fixação do e-book sobre os capítulos daquela semana.
    
3. **Sábado e Domingo:** Desligue a máquina, vá relaxar a mente e curtir. Segurança cibernética exige mente limpa.