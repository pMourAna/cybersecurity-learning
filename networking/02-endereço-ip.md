# 🌐 Endereço IP

## Conceito

IP significa **Internet Protocol** (Protocolo de Internet).

Um endereço IP é um endereço lógico utilizado para identificar uma interface de rede dentro de uma rede IP e permitir a comunicação entre dispositivos.

Por meio do endereçamento IP, os dispositivos conseguem enviar e receber pacotes de dados.

Exemplo de endereço IPv4:

`192.168.1.10`

---

##  Para que serve um endereço IP?

O endereço IP permite que os dispositivos sejam identificados logicamente dentro de uma rede e que os dados sejam encaminhados até o destino correto.

Podemos pensar nele como um endereço lógico utilizado durante a comunicação em uma rede.

Exemplos de dispositivos que podem possuir um endereço IP:

- 💻 Computadores
- 📱 Smartphones
- 🖨️ Impressoras de rede
- 🖥️ Servidores
- 📷 Câmeras IP
- 📡 Roteadores
- 📺 Smart TVs
- 🌐 Outros dispositivos conectados à rede

---

# IPv4

IPv4 significa **Internet Protocol version 4**.

É uma das principais versões do protocolo IP utilizadas para comunicação em redes.

Um endereço IPv4 possui **32 bits**, divididos em quatro grupos de 8 bits chamados de **octetos**.

Exemplo:

`192.168.1.10`

Em representação binária:

`11000000.10101000.00000001.00001010`

Cada octeto possui 8 bits:

`8 + 8 + 8 + 8 = 32 bits`

Os valores de cada octeto podem variar de:

`0 a 255`

Por isso, um endereço IPv4 possui quatro números separados por pontos.

---
## Rede e Host

Um endereço IP possui uma parte relacionada à rede e outra relacionada ao host.

Rede

Identifica a rede à qual o dispositivo pertence.

Host

Identifica a interface/dispositivo dentro daquela rede.

A divisão entre rede e host é determinada pela máscara de sub-rede.


## CIDR e a notação /24

O /24 é uma forma de representar a máscara de sub-rede utilizando a notação CIDR (Classless Inter-Domain Routing).

`192.168.1.10/24`

significa que os primeiros 24 bits pertencem à parte da rede.

Como o IPv4 possui 32 bits:

32 - 24 = 8

Portanto, sobram 8 bits para a parte dos hosts.

A máscara equivalente ao /24 é:

`255.255.255.0`

Em binário:

`11111111.11111111.11111111.00000000`

---
## Exemplo com /25

Quando utilizamos:

`192.168.1.10/25`

temos:

25 bits → Rede
7 bits  → Host

A máscara equivalente é:

`255.255.255.128`

Uma rede /24 pode ser dividida em duas redes /25.

Primeira rede

`192.168.1.0/25`

Intervalo:

`192.168.1.0 - 192.168.1.127`

Hosts utilizáveis:

`192.168.1.1 - 192.168.1.126`

Segunda rede

`192.168.1.128/25`

Intervalo:

`192.168.1.128 - 192.168.1.255`

Hosts utilizáveis:

`192.168.1.129 - 192.168.1.254`

---
## Quantidade de endereços

### /24
A quantidade total de endereços depende da quantidade de bits disponíveis para hosts.

2^n

32 - 24 = 8 bits de host

2⁸ = 256 endereços totais

Normalmente:

256 endereços totais
- 1 endereço de rede
- 1 endereço de broadcast
= 254 hosts utilizáveis

### /25

32 - 25 = 7 bits para hosts

2⁷ = 128 endereços

Normalmente:

128 endereços totais
- 1 endereço de rede
- 1 endereço de broadcast
= 126 hosts utilizáveis

---
  ## IP privado e IP público

Os endereços IP podem ser utilizados em diferentes contextos.

### IP privado

É utilizado dentro de redes privadas, como redes domésticas e corporativas.

Algumas faixas privadas IPv4 são:

`10.0.0.0/8
172.16.0.0/12
192.168.0.0/16`

Exemplo:

`192.168.1.10`

Esse endereço pode ser utilizado dentro de uma rede local.

### IP público

É um endereço utilizado para comunicação através da Internet e é atribuído dentro do espaço de endereçamento público.

Um dispositivo dentro de uma rede privada pode acessar a Internet através de mecanismos como o NAT (Network Address Translation) realizado normalmente pelo roteador.

---
## NAT

NAT significa Network Address Translation.

Ele permite traduzir endereços entre redes, sendo muito utilizado para permitir que dispositivos com endereços privados acessem a Internet através de um endereço público.

Vários dispositivos de uma rede doméstica podem compartilhar um mesmo endereço IP público.

---
## IPv4 e IPv6
IPv4
Possui 32 bits
Utiliza quatro octetos
Exemplo: 192.168.1.10
Possui aproximadamente 4,3 bilhões de endereços possíveis
IPv6

O IPv6 foi desenvolvido para ampliar enormemente o espaço de endereçamento disponível.

Ele possui 128 bits.

Exemplo:

`2001:db8::1`

O IPv6 utiliza representação hexadecimal e é separado por dois-pontos.

IPv4 e IPv6 podem coexistir em uma mesma rede ou dispositivo por meio de mecanismos de transição e compatibilidade.

---
## O que eu aprendi

Neste estudo, aprendi que:

O endereço IP é utilizado para identificação lógica e comunicação em redes IP.

O IPv4 possui 32 bits.

Os 32 bits são divididos em quatro octetos.

A máscara de sub-rede determina a divisão entre rede e host.

A notação /24 significa que 24 bits pertencem à rede.

A notação /25 significa que 25 bits pertencem à rede.

Quanto mais bits são utilizados para a rede, menos bits ficam disponíveis para hosts.

IPs privados são utilizados dentro de redes privadas.

NAT permite que dispositivos com IPs privados acessem a Internet através de endereços públicos.

IPv6 possui 128 bits e oferece um espaço de endereçamento muito maior que o IPv4.


---
## Relação com Cybersecurity

Conhecer endereçamento IP é fundamental para Cybersecurity.

Esse conhecimento será utilizado posteriormente em assuntos como:

🔎 Reconhecimento
🔎 Enumeração
🌐 Análise de redes
🧪 Pentest
🛡️ Segurança de redes
🔥 Firewall
📊 Análise de tráfego
🚨 Detecção de ataques
🔵 Blue Team
🔴 Red Team

Entender IP, rede, host e sub-redes é essencial para compreender como os dispositivos se comunicam e como essa comunicação pode ser analisada e protegida.

---
## Próximos assuntos
MAC Address
Máscara de sub-rede
Sub-redes
TCP/IP
Portas
Protocolos
DNS
DHCP
Roteamento
