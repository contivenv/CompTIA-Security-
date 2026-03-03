https://www.cloudflare.com/pt-br/learning/network-layer/what-is-sdn/
## O que é rede definida por software (SDN)?

Uma rede definida por software (SDN) é uma categoria de tecnologias que permitem gerenciar uma [rede](https://www.cloudflare.com/learning/network-layer/what-is-the-network-layer/) por meio de software. A tecnologia SDN permite aos administradores de TI configurar suas redes usando um software aplicativo. O software SDN é interoperável, ou seja, deve ser capaz de funcionar com qualquer [roteador](https://www.cloudflare.com/learning/network-layer/what-is-routing/) ou [switch](https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/), não importando qual fornecedor o tenha feito.

## O que é plano de controle?

Tecnicamente falando, uma SDN é possível separando-se o plano de controle do plano de dados. "Plano" é um termo de rede que se refere a uma concepção abstrata de onde ocorrem os processos de rede. O plano de controle se refere aos processos de rede que direcionam o tráfego da rede, enquanto o plano de dados se refere aos dados reais que percorrem a rede. O plano de controle faz isso estabelecendo rotas de rede e comunicando quais protocolos devem ser usados.

Pense no plano de controle como sendo o grupo dos semáforos que operam nos cruzamentos de uma cidade. Enquanto isso, o plano de dados seria como os carros que percorrem as estradas, param nos cruzamentos e obedecem aos semáforos.

Em configurações de rede que utilizam apenas hardware físico, cada roteador ou switch individual precisa ser configurado por si só. O plano de controle está estreitamente interligado com o plano de dados e com o hardware de rede subjacente. Com a SDN, o plano de controle é separado do plano de dados e do hardware real, permitindo configurar o plano de controle a partir de um local central.

## O que é topologia de rede?

"Topologia de rede" é um termo que se refere à forma como os dados fluem em uma rede. O plano de controle estabelece e altera a topologia de rede. Mais uma vez, pense nos semáforos que funcionam nos cruzamentos de uma cidade. A topologia da rede é como a disposição das estradas e dos vários destinos na cidade, com as rotas da rede sendo as estradas e os dispositivos de computação como os destinos. Enquanto isso, os roteadores e switches são os semáforos que funcionam nos "cruzamentos" dessas rotas.

A topologia de rede não se refere às posições físicas dos roteadores, switches e computadores em relação uns aos outros. Em vez disso, tem a ver exclusivamente com os caminhos que os dados percorrem na rede. Se dois computadores se conectarem diretamente a um switch de rede por meio de cabos Ethernet, e o computador A estiver próximo à sala ao lado do switch, enquanto o computador B estiver do outro lado da sala, ambos os computadores estarão equidistantes do switch na topologia de rede.

No SDN, como o plano de controle é separado do hardware subjacente, é possível mudar a topologia da rede por meio de software em vez de hardware. Voltando ao exemplo, se um administrador usando a SDN quisesse mudar o lugar em que o Computador B estava na topologia de rede, ele poderia usar seu software de rede para redefinir a topologia de modo que o tráfego fosse do switch para (por exemplo) outro roteador antes de ir para o Computador B.

## Quais são alguns dos principais usos da SDN?

As redes definidas por software são cada vez mais utilizadas em grandes data centers. Um data center é uma coleção de servidores e equipamentos de rede, normalmente dentro de um único edifício, que armazena, processa e troca dados. Quase todos os [servidores web](https://www.cloudflare.com/learning/cdn/glossary/origin-server/) estão localizados dentro de data centers, e muitas empresas operam seus próprios data centers para armazenar dados corporativos e executar aplicativos internas (por exemplo, e-mail corporativo). Como os data centers utilizam muitos equipamentos físicos de rede, a SDN facilita muito o trabalho administrativo dentro deles.

A SDN também permite que as empresas conectem mais facilmente sua infraestrutura local à sua infraestrutura de nuvem, como em uma implantação de [nuvem híbrida](https://www.cloudflare.com/learning/cloud/what-is-hybrid-cloud/). As nuvens corporativas podem se conectar com softwares muito mais facilmente do que com hardwares; o hardware muitas vezes apresenta problemas de compatibilidade, enquanto o software em nuvem e o software SDN podem ser integrados independentemente do hardware subjacente. Na verdade, muitos fornecedores oferecem tanto serviços de nuvem quanto um produto SDN, tornando as integrações de nuvem híbrida ainda mais simples.

## Qual é a diferença entre SDN e SD-WAN?

Uma [rede de longa distância](https://www.cloudflare.com/learning/network-layer/what-is-a-wan/) definida por software, ou [SD-WAN](https://www.cloudflare.com/learning/network-layer/what-is-an-sd-wan/), é um tipo de arquitetura de rede baseada em software. As SD-WANs são um aplicativo de rede definida por software. Basicamente, todas as SD-WANs usam SDN, mas nem todas as redes definidas por software são SD-WANs.

Muitas empresas estão optando pela SDN ou pelas SD-WANs à medida que suas pilhas de tecnologia migram para a nuvem. Uma abordagem virtualizada baseada em software para a rede permite que elas sejam mais flexíveis. No entanto, as redes definidas por software estão abertas a vários tipos de ataques, incluindo [ataques DDoS](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/). O [Magic Transit](https://www.cloudflare.com/magic-transit/) da Cloudflare [protege redes no local, híbridas e em nuvem](https://www.cloudflare.com/pt-br/network-security/) contra esses ataques.

Além disso, a Cloudflare WAN oferece uma alternativa mais rápida e segura para o uso de SD-WANs. Saiba mais sobre a [Cloudflare WAN](https://www.cloudflare.com/magic-wan).