Camada de Rede e Configurações de Rede IP (Modelo OSI e Internet)
📌 Introdução

A camada de rede é uma das camadas mais importantes do Modelo OSI, sendo responsável por possibilitar a comunicação entre dispositivos localizados em diferentes redes. Este trabalho tem como objetivo apresentar os principais conceitos relacionados à camada de rede, abordando o protocolo IP, endereçamento IPv4, roteamento, sub-redes, CIDR, ARP e NAT, destacando seu funcionamento e importância para a Internet moderna.

🌐 1. Camada de Rede no Modelo OSI

No Modelo OSI, a camada de rede está localizada acima da camada de enlace e tem como função principal garantir que os dados enviados por um hospedeiro cheguem corretamente ao seu destino, independentemente da localização desse destino na rede.

As principais responsabilidades da camada de rede são:

Definir um esquema de endereçamento lógico;

Realizar o roteamento dos pacotes;

Encaminhar os pacotes através de roteadores intermediários;

Permitir a comunicação fim a fim entre hospedeiros.

A unidade de dados da camada de rede é o pacote, também chamado de datagrama.

🔁 2. Roteamento e Repasse

O funcionamento da camada de rede envolve dois processos distintos:

Roteamento (routing): processo global responsável por calcular o melhor caminho entre origem e destino, utilizando algoritmos de roteamento para construir tabelas de rotas.

Repasse (forwarding): processo local no qual o roteador, ao receber um pacote, consulta sua tabela de repasse e decide por qual interface o pacote deve ser encaminhado.

Esses dois processos trabalham de forma complementar para garantir a entrega eficiente dos pacotes.

📦 3. Comutação Store and Forward

A Internet utiliza a comutação de pacotes do tipo store and forward, na qual cada roteador recebe o pacote completo, realiza verificações e somente depois o encaminha ao próximo salto. Esse método aumenta a confiabilidade da transmissão, embora possa gerar maior latência.

🔌 4. Circuitos Virtuais e Datagramas

A camada de rede pode operar de duas formas:

Circuitos Virtuais

Serviço orientado à conexão;

Um caminho é estabelecido antes da transmissão;

Todos os pacotes seguem a mesma rota;

Os pacotes chegam ao destino na ordem correta.

Datagramas

Serviço sem conexão;

Cada pacote é tratado de forma independente;

Os pacotes podem seguir rotas diferentes;

Podem ocorrer perda, duplicação ou chegada fora de ordem.

A Internet utiliza o modelo baseado em datagramas.

🌍 5. Protocolo IP e IPv4

O Internet Protocol (IP) é o protocolo da camada de rede responsável por transportar datagramas entre redes. No IPv4, os endereços possuem 32 bits, escritos em notação decimal pontuada, como por exemplo: 192.168.1.10.

Cada interface de rede possui seu próprio endereço IP, e esses endereços devem ser únicos dentro da Internet válida.

🧮 6. CIDR e Endereçamento IP

O CIDR (Classless Inter-Domain Routing) permite uma divisão flexível dos endereços IP, representada pela notação A.B.C.D/X, onde X indica o número de bits que identificam a rede.

O CIDR substituiu o antigo sistema de classes (A, B e C), reduzindo o desperdício de endereços e melhorando a eficiência do roteamento.

🧩 7. Sub-redes e Máscaras de Rede

A divisão de uma rede em sub-redes é realizada por meio da máscara de rede, que define quais bits representam a rede e quais representam os hospedeiros.

A criação de sub-redes permite:

Redução do tráfego;

Melhor organização da rede;

Maior segurança;

Separação por departamentos ou regiões.

🔎 8. Protocolo ARP

O ARP (Address Resolution Protocol) é responsável por realizar a conversão entre o endereço IP e o endereço MAC dentro da rede local. Ele funciona por meio de mensagens broadcast, perguntando qual dispositivo possui determinado endereço IP.

Sem o ARP, não seria possível enviar dados corretamente em redes locais baseadas em Ethernet.

🔐 9. NAT – Network Address Translation

Devido à escassez de endereços IPv4, o NAT permite que uma organização utilize endereços IP privados internamente e um ou poucos endereços públicos para acesso à Internet.

O NAT:

Economiza endereços IPv4;

Permite que múltiplos dispositivos compartilhem um único IP público;

Oferece uma camada adicional de segurança, pois os dispositivos internos não são acessíveis diretamente da Internet.

🏁 Conclusão

A camada de rede é essencial para o funcionamento da Internet, pois possibilita a comunicação entre redes distintas de forma eficiente e escalável. O uso de protocolos como IP, ARP e técnicas como CIDR, sub-redes e NAT garante que bilhões de dispositivos possam se comunicar diariamente, mesmo diante das limitações do IPv4.

📚 Referências

TANENBAUM, Andrew S. Redes de Computadores

RFC 791 – Internet Protocol

RFC 3022 – NAT

Material didático da disciplina de Redes de Computadores
