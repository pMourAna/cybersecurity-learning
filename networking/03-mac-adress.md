# 🖥️ MAC Address

## Conceito

MAC significa **Media Access Control**.

Um MAC Address é um endereço associado a uma **interface de rede** e utilizado principalmente na comunicação dentro de uma rede local.

Uma interface de rede pode ser, por exemplo:

- Interface Ethernet
- Interface Wi-Fi
- Interface de uma máquina virtual
- Outras interfaces de rede

Exemplo de MAC Address:

`00:1A:2B:3C:4D:5E`

---

# 🧠 IP x MAC

Embora IP e MAC sejam utilizados na comunicação entre dispositivos, eles possuem funções diferentes.

### IP

O endereço IP é um **endereço lógico** utilizado para endereçamento e comunicação em redes IP.

Exemplo:

`192.168.1.10`

### MAC

O MAC é associado à interface de rede e é utilizado principalmente na comunicação dentro da rede local.

Exemplo:

`00:1A:2B:3C:4D:5E`

Podemos resumir:

IP  → endereçamento lógico

MAC → identificação da interface na rede local

# Comparação entre IP e MAC

| Característica           | IP                            | MAC                       |
| ------------------------ | ----------------------------- | ------------------------- |
| Tipo                     | Endereço lógico               | Endereço da interface     |
| Uso principal            | Endereçamento e roteamento IP | Comunicação na rede local |
| IPv4                     | 32 bits                       | —                         |
| IPv6                     | 128 bits                      | —                         |
| MAC tradicional Ethernet | —                             | 48 bits                   |
| Representação IPv4       | Decimal                       | —                         |
| Representação MAC        | —                             | Hexadecimal               |
| Exemplo                  | `192.168.1.10`                | `00:1A:2B:3C:4D:5E`       |


Importante: um MAC não deve ser entendido simplesmente como "o endereço físico do computador". Ele está associado a uma interface de rede. Um dispositivo pode possuir várias interfaces e, consequentemente, vários endereços MAC.

## Quantidade de bits

Um endereço MAC Ethernet tradicional possui 48 bits.

Esses 48 bits normalmente são representados como seis grupos de dois dígitos hexadecimais.

Exemplo:

`00:1A:2B:3C:4D:5E`

Cada grupo possui 8 bits

Portanto:

8 × 6 = 48 bits

## Sistema hexadecimal

Os endereços MAC são normalmente representados utilizando o sistema hexadecimal.

O sistema decimal utiliza:

0 1 2 3 4 5 6 7 8 9

O hexadecimal utiliza:

0 1 2 3 4 5 6 7 8 9 A B C D E F

As letras representam valores:

A = 10
B = 11
C = 12
D = 13
E = 14
F = 15

Por isso um MAC pode conter letras e números:

`00:1A:2B:3C:4D:5E`

## MAC e Ethernet

Em redes Ethernet, os endereços MAC são utilizados nos quadros Ethernet para identificar a origem e o destino na comunicação dentro da rede local.

Isso significa que o pacote IP pode ser transportado dentro de um quadro Ethernet.

## IP e MAC trabalhando juntos

Imagine dois computadores na mesma rede:

PC A

IP:  192.168.1.10
MAC: AA:AA:AA:AA:AA:AA


PC B

IP:  192.168.1.20
MAC: BB:BB:BB:BB:BB:BB

O PC A deseja se comunicar com:

`192.168.1.20`

Ele conhece o endereço IP de destino, mas precisa descobrir qual endereço MAC está associado a esse IP para realizar a comunicação na rede local.

É nesse momento que entra o ARP.

## ARP

ARP significa:

Address Resolution Protocol

No IPv4, o ARP é utilizado para descobrir o endereço MAC associado a um determinado endereço IPv4 dentro da rede local.

De forma simplificada:

IP
↓
ARP
↓
MAC

Exemplo:

192.168.1.20
      ↓
     ARP
      ↓
BB:BB:BB:BB:BB:BB

O funcionamento detalhado do ARP será estudado separadamente.

## ARP Cache

Depois que um dispositivo descobre a associação entre um endereço IP e um MAC, essa informação pode ser armazenada temporariamente em uma ARP Cache.

Isso evita que o dispositivo precise realizar uma nova resolução ARP para cada comunicação.

As entradas da tabela podem expirar e ser atualizadas conforme necessário.

## Importância para Cybersecurity

O conhecimento sobre MAC Addresses é importante para diversas áreas de Cybersecurity.

Ele pode ser utilizado em:

🔎 Análise de redes
📊 Análise de tráfego
🧪 Pentest
🛡️ Monitoramento de redes
🚨 Detecção de anomalias
🔵 Blue Team
🔴 Red Team
🔬 Network Forensics

Também é importante para compreender ataques relacionados ao protocolo ARP, como:

ARP Spoofing / ARP Poisoning

Esses ataques serão estudados posteriormente.

## MAC Address pode mudar?

Um endereço MAC pode estar associado de forma permanente à interface de rede, mas isso não significa que ele seja absolutamente imutável.

Dependendo do sistema operacional, hardware ou configuração, o MAC apresentado por uma interface pode ser alterado ou virtualizado.

Isso pode ocorrer, por exemplo, em:

Máquinas virtuais
Ambientes de laboratório
Sistemas operacionais que permitem alteração do endereço
Interfaces virtualizadas

Por isso, não devemos tratar um MAC como uma identidade impossível de modificar.

#  O que eu aprendi

Neste estudo, aprendi que:

MAC significa Media Access Control.

Um MAC Address é associado a uma interface de rede.

Um MAC tradicional Ethernet possui 48 bits.

MAC Addresses são normalmente representados em hexadecimal.

IP é um endereço lógico utilizado no endereçamento de redes IP.

MAC é utilizado principalmente na comunicação dentro da rede local.

Ethernet utiliza endereços MAC nos seus quadros.

O ARP pode ser utilizado para descobrir o MAC associado a um endereço IPv4 na rede local.

A associação entre IP e MAC pode ser armazenada temporariamente na ARP Cache.

O conhecimento de MAC e ARP é importante para análise e segurança de redes.

# 🔐 Relação com Cybersecurity

Compreender a relação entre IP, MAC e ARP é importante para entender posteriormente:

Reconhecimento de rede

Enumeração

Análise de tráfego

ARP Spoofing

ARP Poisoning

Network Forensics

Monitoramento de redes

Detecção de ataques

Pentest

Red Team

Blue Team

#  Próximo assunto

## ARP — Address Resolution Protocol

### No próximo estudo serão abordados:

O que é ARP

Por que o ARP é necessário

ARP Request

ARP Reply

ARP Cache

Funcionamento passo a passo

Broadcast e unicast no ARP

ARP Spoofing

ARP Poisoning

Importância do ARP para Cybersecurity
