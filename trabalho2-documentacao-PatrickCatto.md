# Trabalho 2: Integração de habilidades - 2022/1
**Disciplina: Redes de Computadores**

**Curso: Engenharia de Computação / Elétrica**

**Patrick Catto/2155214:**

---

## Tarefa 1:  Sub-Redes


|    Nome     | Pref. |   Tam.   |    ipv4 sub    |     Mascara     |   broadcast    |          ipv6 sub           |
| :---------: | :---: | :------: | :------------: | :-------------: | :------------: | :-------------------------: |
|   Matriz    |  /26  | 2^6 = 64 |  200.200.14.0  | 255.255.255.192 | 200.200.14.63  |   2001:DB8:ACAD:0E00::/64   |
|  filial 1   |  /27  | 2^5 = 32 | 200.200.14.64  | 255.255.255.224 | 200.200.14.95  |   2001:DB8:ACAD:0E01::/64   |
|  filial 2   |  /27  | 2^5 = 32 | 200.200.14.96  | 255.255.255.224 | 200.200.14.127 |   2001:DB8:ACAD:0E02::/64   |
|  filial 3   |  /27  | 2^5 = 32 | 200.200.14.128 | 255.255.255.224 | 200.200.14.159 |   2001:DB8:ACAD:0E03::/64   |
|  filial 4   |  /27  | 2^5 = 32 | 200.200.14.160 | 255.255.255.224 | 200.200.14.191 |   2001:DB8:ACAD:0E04::/64   |
|  filial 5   |  /27  | 2^5 = 32 | 200.200.14.192 | 255.255.255.224 | 200.200.14.223 |   2001:DB8:ACAD:0E05::/64   |
| links wan 1 |  /30  | 2^2 =  4 | 200.200.14.224 | 255.255.255.252 | 200.200.14.227 | 2001:DB8:ACAD:0EFF::0:0/112 |
| links wan 2 |  /30  | 2^2 =  4 | 200.200.14.228 | 255.255.255.252 | 200.200.14.231 | 2001:DB8:ACAD:0EFF::1:0/112 |
| links wan 3 |  /30  | 2^2 =  4 | 200.200.14.232 | 255.255.255.252 | 200.200.14.235 | 2001:DB8:ACAD:0EFF::2:0/112 |
| links wan 4 |  /30  | 2^2 =  4 | 200.200.14.236 | 255.255.255.252 | 200.200.14.239 | 2001:DB8:ACAD:0EFF::3:0/112 |
| links wan 5 |  /30  | 2^2 =  4 | 200.200.14.240 | 255.255.255.252 | 200.200.14.243 | 2001:DB8:ACAD:0EFF::4:0/112 |

---

## Tarefa 2: Endereçamento de Dispositivos

| Dispositivo           | Interface | IPv4           | IPv4 - Máscara  | IPv4 - Gateway |        IPv6/Prefixo         |    IPv6 - Gateway     |
| --------------------- | --------- | -------------- | --------------- | :------------: | :-------------------------: | :-------------------: |
| PC1                   | NIC       | 200.200.14.3   | 255.255.255.192 |  200.200.14.1  |  2001:DB8:ACAD:0E00::3/64   | 2001:DB8:ACAD:0E00::1 |
| PC2                   | NIC       | 200.200.14.4   | 255.255.255.192 |  200.200.14.1  |  2001:DB8:ACAD:0E00::4/64   | 2001:DB8:ACAD:0E00::1 |
| PC3                   | NIC       | 200.200.14.67  | 255.255.255.224 | 200.200.14.65  |  2001:DB8:ACAD:0E01::3/64   | 2001:DB8:ACAD:0E01::1 |
| PC4                   | NIC       | 200.200.14.68  | 255.255.255.224 | 200.200.14.65  |  2001:DB8:ACAD:0E01::4/64   | 2001:DB8:ACAD:0E01::1 |
| PC5                   | NIC       | 200.200.14.99  | 255.255.255.224 | 200.200.14.97  |  2001:DB8:ACAD:0E02::3/64   | 2001:DB8:ACAD:0E02::1 |
| PC6                   | NIC       | 200.200.14.100 | 255.255.255.224 | 200.200.14.97  |  2001:DB8:ACAD:0E02::4/64   | 2001:DB8:ACAD:0E02::1 |
| Switch-Matriz         | SVI       | 200.200.14.2   | 255.255.255.192 |  200.200.14.1  |              -              |           -           |
| Switch-Filial1        | SVI       | 200.200.14.66  | 255.255.255.224 | 200.200.14.65  |              -              |           -           |
| Switch-Filial2        | SVI       | 200.200.14.98  | 255.255.255.224 | 200.200.14.97  |              -              |           -           |
| Roteador-Pato Branco  | Fa0/0     | 200.200.14.1   | 255.255.255.192 |       -        |  2001:DB8:ACAD:0E00::1/64   |           -           |
| Roteador-Pato Branco  | Se0/0/0   | 200.200.14.225 | 255.255.255.252 |       -        |  2001:DB8:ACAD:0EFF::1/112  |           -           |
| Roteador-Pato Branco  | Se0/0/1   | 200.200.14.238 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::3:2/112 |           -           |
| Roteador-Fco. Beltrão | Fa0/0     | 200.200.14.65  | 255.255.255.224 |       -        |  2001:DB8:ACAD:0E01::1/64   |           -           |
| Roteador-Fco. Beltrão | Se0/0/0   | 200.200.14.233 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::2:1/112 |           -           |
| Roteador-Fco. Beltrão | Se0/0/1   | 200.200.14.230 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::1:2/112 |           -           |
| Roteador-Vitorino     | Se0/0/0   | 200.200.14.229 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::1:1/112 |           -           |
| Roteador-Vitorino     | Se0/0/1   | 200.200.14.226 | 255.255.255.252 |       -        |  2001:DB8:ACAD:0EFF::2/112  |           -           |
| Roteador-Itapejara    | Se0/0/0   | 200.200.14.237 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::3:1/112 |           -           |
| Roteador-Itapejara    | Se0/0/1   | 200.200.14.234 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::2:2/112 |           -           |
| Roteador-Itapejara    | Fa0/1     | 200.200.14.241 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::4:1/112 |           -           |
| Roteador-Coronel      | Fa0/0     | 200.200.14.97  | 255.255.255.224 |       -        |  2001:DB8:ACAD:0E02::1/64   |           -           |
| Roteador-Coronel      | Fa0/1     | 200.200.14.242 | 255.255.255.252 |       -        | 2001:DB8:ACAD:0EFF::4:2/112 |           -           |

---

## Tarefa 3: Tabela de Roteamento
### Roteador Pato Branco
#### IPv4
| Rede de Destino | Máscara         | Next Hop       | Interface de Saída |
| --------------- | --------------- | -------------- | ------------------ |
| 200.200.14.64   | 255.255.255.224 | 200.200.14.226 | Se0/0/0            |
| 200.200.14.96   | 255.255.255.224 | 200.200.14.226 | Se0/0/0            |
| 200.200.14.228  | 255.255.255.252 | 200.200.14.226 | Se0/0/0            |
| 200.200.14.232  | 255.255.255.252 | 200.200.14.226 | Se0/0/0            |
| 200.200.14.240  | 255.255.255.252 | 200.200.14.226 | Se0/0/0            |
#### IPv6
| Rede de Destino/Prefixo     | Next Hop              | Interface de Saída |
| --------------------------- | --------------------- | ------------------ |
| 2001:DB8:ACAD:0E01::/64     | 2001:DB8:ACAD:0EFF::2 | Se0/0/0            |
| 2001:DB8:ACAD:0E02::/64     | 2001:DB8:ACAD:0EFF::2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::1:0/112 | 2001:DB8:ACAD:0EFF::2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::2:0/112 | 2001:DB8:ACAD:0EFF::2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::4:0/112 | 2001:DB8:ACAD:0EFF::2 | Se0/0/0            |


### Roteador Francisco Beltrão
#### IPv4
| Rede de Destino | Máscara         | Next Hop       | Interface de Saída |
| --------------- | --------------- | -------------- | ------------------ |
| 200.200.14.0    | 255.255.255.192 | 200.200.14.234 | Se0/0/0            |
| 200.200.14.96   | 255.255.255.224 | 200.200.14.234 | Se0/0/0            |
| 200.200.14.224  | 255.255.255.252 | 200.200.14.234 | Se0/0/0            |
| 200.200.14.236  | 255.255.255.252 | 200.200.14.234 | Se0/0/0            |
| 200.200.14.240  | 255.255.255.252 | 200.200.14.234 | Se0/0/0            |
#### IPv6
| Rede de Destino/Prefixo     | Next Hop                | Interface de Saída |
| --------------------------- | ----------------------- | ------------------ |
| 2001:DB8:ACAD:0E00::/64     | 2001:DB8:ACAD:0EFF::2:2 | Se0/0/0            |
| 2001:DB8:ACAD:0E02::/64     | 2001:DB8:ACAD:0EFF::2:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::/112    | 2001:DB8:ACAD:0EFF::2:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::3:0/112 | 2001:DB8:ACAD:0EFF::2:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::4:0/112 | 2001:DB8:ACAD:0EFF::2:2 | Se0/0/0            |

### Roteador Vitorino
#### IPv4
| Rede de Destino | Máscara         | Next Hop       | Interface de Saída |
| --------------- | --------------- | -------------- | ------------------ |
| 200.200.14.0    | 255.255.255.192 | 200.200.14.230 | Se0/0/0            |
| 200.200.14.64   | 255.255.255.224 | 200.200.14.230 | Se0/0/0            |
| 200.200.14.96   | 255.255.255.224 | 200.200.14.230 | Se0/0/0            |
| 200.200.14.232  | 255.255.255.252 | 200.200.14.230 | Se0/0/0            |
| 200.200.14.236  | 255.255.255.252 | 200.200.14.230 | Se0/0/0            |
| 200.200.14.240  | 255.255.255.252 | 200.200.14.230 | Se0/0/0            |
#### IPv6
| Rede de Destino/Prefixo     | Next Hop                | Interface de Saída |
| --------------------------- | ----------------------- | ------------------ |
| 2001:DB8:ACAD:0E00::/64     | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |
| 2001:DB8:ACAD:0E01::/64     | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |
| 2001:DB8:ACAD:0E02::/64     | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::2:0/112 | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::3:0/112 | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::4:0/112 | 2001:DB8:ACAD:0EFF::1:2 | Se0/0/0            |

### Roteador Itapejara D'Oeste
#### IPv4
| Rede de Destino | Máscara         | Next Hop       | Interface de Saída |
| --------------- | --------------- | -------------- | ------------------ |
| 200.200.14.0    | 255.255.255.192 | 200.200.14.238 | Se0/0/0            |
| 200.200.14.64   | 255.255.255.224 | 200.200.14.238 | Se0/0/0            |
| 200.200.14.96   | 255.255.255.224 | 200.200.14.242 | Fa0/1              |
| 200.200.14.224  | 255.255.255.252 | 200.200.14.238 | Se0/0/0            |
| 200.200.14.228  | 255.255.255.252 | 200.200.14.238 | Se0/0/0            |
#### IPv6
| Rede de Destino/Prefixo     | Next Hop                | Interface de Saída |
| --------------------------- | ----------------------- | ------------------ |
| 2001:DB8:ACAD:0E00::/64     | 2001:DB8:ACAD:0EFF::3:2 | Se0/0/0            |
| 2001:DB8:ACAD:0E01::/64     | 2001:DB8:ACAD:0EFF::3:2 | Se0/0/0            |
| 2001:DB8:ACAD:0E02::/64     | 2001:DB8:ACAD:0EFF::4:2 | Fa0/1              |
| 2001:DB8:ACAD:0EFF::/112    | 2001:DB8:ACAD:0EFF::3:2 | Se0/0/0            |
| 2001:DB8:ACAD:0EFF::1:0/112 | 2001:DB8:ACAD:0EFF::3:2 | Se0/0/0            |

### Roteador Coronel Vivida
#### IPv4
| Rede de Destino | Máscara         | Next Hop       | Interface de Saída |
| --------------- | --------------- | -------------- | ------------------ |
| 200.200.14.0    | 255.255.255.192 | 200.200.14.241 | Fa0/1              |
| 200.200.14.64   | 255.255.255.224 | 200.200.14.241 | Fa0/1              |
| 200.200.14.224  | 255.255.255.252 | 200.200.14.241 | Fa0/1              |
| 200.200.14.228  | 255.255.255.252 | 200.200.14.241 | Fa0/1              |
| 200.200.14.232  | 255.255.255.252 | 200.200.14.241 | Fa0/1              |
| 200.200.14.236  | 255.255.255.252 | 200.200.14.241 | Fa0/1              |
#### IPv6
| Rede de Destino/Prefixo     | Next Hop                | Interface de Saída |
| --------------------------- | ----------------------- | ------------------ |
| 2001:DB8:ACAD:0E00::/64     | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |
| 2001:DB8:ACAD:0E01::/64     | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |
| 2001:DB8:ACAD:0EFF::/112    | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |
| 2001:DB8:ACAD:0EFF::1:0/112 | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |
| 2001:DB8:ACAD:0EFF::2:0/112 | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |
| 2001:DB8:ACAD:0EFF::3:0/112 | 2001:DB8:ACAD:0EFF::4:1 | Fa0/1              |

---

## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-PatrickCatto](trabalho2-topologia-PatrickCatto.pkt)


## Arquivos de Configuração dos Dispositivos Intermediários (roteadores e switches)

<details>
    <summary>Roteador Pato Branco <a href="r-pb-pc.txt">Abrir config.</a></summary>
```
enable
conf t
hostname r-pb-pc
ipv6 unicast-routing
interface Se0/0/0
description pb-vit
clock rate 56000
ip address 200.200.14.225 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::1/112
ipv6 enable
no shutdown
exit
interface Se0/0/1
description ita-pb
ip address 200.200.14.238 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::3:2/112
ipv6 enable
no shutdown
exit
interface fa0/0
description Matriz
ip address 200.200.14.1 255.255.255.192
ipv6 address 2001:DB8:ACAD:0E00::1/64
ipv6 address FE80::1 link-local
ipv6 enable
no shutdown
exit
ip route 200.200.14.64 255.255.255.224 200.200.14.226
ip route 200.200.14.96 255.255.255.224 200.200.14.226
ip route 200.200.14.228 255.255.255.252 200.200.14.226
ip route 200.200.14.232 255.255.255.252 200.200.14.226
ip route 200.200.14.240 255.255.255.252 200.200.14.226
ipv6 route 2001:DB8:ACAD:0E01::/64 2001:DB8:ACAD:0EFF::2
ipv6 route 2001:DB8:ACAD:0E02::/64 2001:DB8:ACAD:0EFF::2
ipv6 route 2001:DB8:ACAD:0EFF::1:0/112 2001:DB8:ACAD:0EFF::2
ipv6 route 2001:DB8:ACAD:0EFF::2:0/112 2001:DB8:ACAD:0EFF::2
ipv6 route 2001:DB8:ACAD:0EFF::4:0/112 2001:DB8:ACAD:0EFF::2
security passwords min-length 10
login block-for 120 attempts 3 within 60
service password-encryption
ip domain name patrick.catto.com.br
crypto key generate rsa general-keys modulus 1024
username patrick secret ssh@Network1ng
line vty 0 15
exec-timeout 5
login local
transport input ssh 
exit
line con 0
exec-timeout 5
exit
enable secret @dmin-patrick
line con 0
password @Cons-patrick
login
exit
banner motd $	-------------------------------------------------------------------------------------------
|                                                                                          |
|                         Roteador Pato Branco                                             |
|                                                                                          |
|               ATENCAO Acesso Restrito a pessoas autorizadas!                             |
|                                                                                          |
|         Administrador: PATRICK CATTO (catto@alunos.utfpr.edu.br)                         |
|                                                                                          |
-------------------------------------------------------------------------------------------$
exit
wr

```
</details>

<details>
    <summary>Roteador Francisco Beltrão <a href="r-fb-pc.txt">Abrir config.</a></summary>
```
enable
conf t
hostname r-fb-pc
ipv6 unicast-routing
interface Se0/0/0
description fb-ita
clock rate 56000
ip address 200.200.14.233 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::2:1/112
ipv6 enable
no shutdown
exit
interface Se0/0/1
description vit-fb
ip address 200.200.14.230 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::1:2/112
ipv6 enable
no shutdown
exit
interface fa0/0
description Filial_1
ip address 200.200.14.65 255.255.255.224
ipv6 address 2001:DB8:ACAD:0E01::1/64
ipv6 address FE80::1 link-local
ipv6 enable
no shutdown
exit
ip route 200.200.14.0 255.255.255.192 200.200.14.234
ip route 200.200.14.96 255.255.255.224 200.200.14.234
ip route 200.200.14.224 255.255.255.252 200.200.14.234
ip route 200.200.14.236 255.255.255.252 200.200.14.234
ip route 200.200.14.240 255.255.255.252 200.200.14.234
ipv6 route 2001:DB8:ACAD:0E00::/64 2001:DB8:ACAD:0EFF::2:2
ipv6 route 2001:DB8:ACAD:0E02::/64 2001:DB8:ACAD:0EFF::2:2
ipv6 route 2001:DB8:ACAD:0EFF::/112 2001:DB8:ACAD:0EFF::2:2
ipv6 route 2001:DB8:ACAD:0EFF::3:0/112 2001:DB8:ACAD:0EFF::2:2
ipv6 route 2001:DB8:ACAD:0EFF::4:0/112 2001:DB8:ACAD:0EFF::2:2
security passwords min-length 10
login block-for 120 attempts 3 within 60
service password-encryption
ip domain name patrick.catto.com.br
crypto key generate rsa general-keys modulus 1024
username patrick secret ssh@Network1ng
line vty 0 15
exec-timeout 5
login local
transport input ssh 
exit
line con 0
exec-timeout 5
exit
enable secret @dmin-patrick
line con 0
password @Cons-patrick
login
exit
banner motd $	-------------------------------------------------------------------------------------------
|                                                                                          |
|                         Roteador Francisco Beltrao                                       |
|                                                                                          |
|               ATENCAO Acesso Restrito a pessoas autorizadas!                             |
|                                                                                          |
|         Administrador: PATRICK CATTO (catto@alunos.utfpr.edu.br)                         |
|                                                                                          |
-------------------------------------------------------------------------------------------$
exit
wr
```
</details>

<details>
    <summary>Roteador Vitorino <a href="r-vit-pc.txt">Abrir config.</a></summary>
```
enable
conf t
hostname r-vit-pc
ipv6 unicast-routing
interface Se0/0/0
description vit-fb
clock rate 56000
ip address 200.200.14.229 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::1:1/112
ipv6 enable
no shutdown
exit
interface Se0/0/1
description pb-vit
ip address 200.200.14.226 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::2/112
ipv6 enable
no shutdown
exit
ip route 200.200.14.0 255.255.255.192 200.200.14.230
ip route 200.200.14.64 255.255.255.224 200.200.14.230
ip route 200.200.14.96 255.255.255.224 200.200.14.230
ip route 200.200.14.232 255.255.255.252 200.200.14.230
ip route 200.200.14.236 255.255.255.252 200.200.14.230
ip route 200.200.14.240 255.255.255.252 200.200.14.230
ipv6 route 2001:DB8:ACAD:0E00::/64 2001:DB8:ACAD:0EFF::1:2
ipv6 route 2001:DB8:ACAD:0E01::/64 2001:DB8:ACAD:0EFF::1:2
ipv6 route 2001:DB8:ACAD:0E02::/64 2001:DB8:ACAD:0EFF::1:2
ipv6 route 2001:DB8:ACAD:0EFF::2:0/112 2001:DB8:ACAD:0EFF::1:2
ipv6 route 2001:DB8:ACAD:0EFF::3:0/112 2001:DB8:ACAD:0EFF::1:2
ipv6 route 2001:DB8:ACAD:0EFF::4:0/112 2001:DB8:ACAD:0EFF::1:2
security passwords min-length 10
login block-for 120 attempts 3 within 60
service password-encryption
ip domain name patrick.catto.com.br
crypto key generate rsa general-keys modulus 1024
username patrick secret ssh@Network1ng
line vty 0 15
exec-timeout 5
login local
transport input ssh 
exit
line con 0
exec-timeout 5
exit
enable secret @dmin-patrick
line con 0
password @Cons-patrick
login
exit
banner motd $	-------------------------------------------------------------------------------------------
|                                                                                          |
|                         Roteador Vitorino                                                |
|                                                                                          |
|               ATENCAO Acesso Restrito a pessoas autorizadas!                             |
|                                                                                          |
|         Administrador: PATRICK CATTO (catto@alunos.utfpr.edu.br)                         |
|                                                                                          |
-------------------------------------------------------------------------------------------$
exit
wr
```
</details>

<details>
    <summary>Roteador Itapejara D'Oeste <a href="r-ita-pc.txt">Abrir config.</a></summary>
```
enable
conf t
hostname r-ita-pc
ipv6 unicast-routing
interface Se0/0/0
description ita-pb
clock rate 56000
ip address 200.200.14.237 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::3:1/112
ipv6 enable
no shutdown
exit
interface Se0/0/1
description fb-ita
ip address 200.200.14.234 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::2:2/112
ipv6 enable
no shutdown
exit
interface fa0/1
description ita-cvv
ip address 200.200.14.241 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::4:1/112
ipv6 enable
no shutdown
exit
ip route 200.200.14.0 255.255.255.192 200.200.14.238
ip route 200.200.14.64 255.255.255.224 200.200.14.238
ip route 200.200.14.96 255.255.255.224 200.200.14.242
ip route 200.200.14.224 255.255.255.252 200.200.14.238
ip route 200.200.14.228 255.255.255.252 200.200.14.238
ipv6 route 2001:DB8:ACAD:0E00::/64 2001:DB8:ACAD:0EFF::3:2
ipv6 route 2001:DB8:ACAD:0E01::/64 2001:DB8:ACAD:0EFF::3:2
ipv6 route 2001:DB8:ACAD:0E02::/64 2001:DB8:ACAD:0EFF::4:2
ipv6 route 2001:DB8:ACAD:0EFF::/112 2001:DB8:ACAD:0EFF::3:2
ipv6 route 2001:DB8:ACAD:0EFF::1:0/112 2001:DB8:ACAD:0EFF::3:2
security passwords min-length 10
login block-for 120 attempts 3 within 60
service password-encryption
ip domain name patrick.catto.com.br
crypto key generate rsa general-keys modulus 1024
username patrick secret ssh@Network1ng
line vty 0 15
exec-timeout 5
login local
transport input ssh 
exit
line con 0
exec-timeout 5
exit
enable secret @dmin-patrick
line con 0
password @Cons-patrick
login
exit
banner motd $	-------------------------------------------------------------------------------------------
|                                                                                          |
|                         Roteador Itapejara D'Oeste                                       |
|                                                                                          |
|               ATENCAO Acesso Restrito a pessoas autorizadas!                             |
|                                                                                          |
|         Administrador: PATRICK CATTO (catto@alunos.utfpr.edu.br)                         |
|                                                                                          |
-------------------------------------------------------------------------------------------$
exit
wr
```
</details>

<details>
    <summary>Roteador Coronel Vivida <a href="r-cv-pc.txt">Abrir config.</a></summary>
```
enable
conf t
hostname r-cvv-pc
ipv6 unicast-routing
interface fa0/1
description ita-cvv
ip address 200.200.14.242 255.255.255.252
ipv6 address 2001:DB8:ACAD:0EFF::4:2/112
ipv6 enable
no shutdown
exit
interface fa0/0
description Filial_2
ip address 200.200.14.97 255.255.255.224
ipv6 address 2001:DB8:ACAD:0E02::1/64
ipv6 address FE80::1 link-local
ipv6 enable
no shutdown
exit
ip route 200.200.14.0 255.255.255.192 200.200.14.241
ip route 200.200.14.64 255.255.255.224 200.200.14.241
ip route 200.200.14.224 255.255.255.252 200.200.14.241
ip route 200.200.14.228 255.255.255.252 200.200.14.241
ip route 200.200.14.232 255.255.255.252 200.200.14.241
ip route 200.200.14.236 255.255.255.252 200.200.14.241
ipv6 route 2001:DB8:ACAD:0E00::/64 2001:DB8:ACAD:0EFF::4:1
ipv6 route 2001:DB8:ACAD:0E01::/64 2001:DB8:ACAD:0EFF::4:1
ipv6 route 2001:DB8:ACAD:0EFF::/112 2001:DB8:ACAD:0EFF::4:1
ipv6 route 2001:DB8:ACAD:0EFF::1:0/112 2001:DB8:ACAD:0EFF::4:1
ipv6 route 2001:DB8:ACAD:0EFF::2:0/112 2001:DB8:ACAD:0EFF::4:1
ipv6 route 2001:DB8:ACAD:0EFF::3:0/112 2001:DB8:ACAD:0EFF::4:1
security passwords min-length 10
login block-for 120 attempts 3 within 60
service password-encryption
ip domain name patrick.catto.com.br
crypto key generate rsa general-keys modulus 1024
username patrick secret ssh@Network1ng
line vty 0 15
exec-timeout 5
login local
transport input ssh 
exit
line con 0
exec-timeout 5
exit
enable secret @dmin-patrick
line con 0
password @Cons-patrick
login
exit
banner motd $	-------------------------------------------------------------------------------------------
|                                                                                          |
|                         Roteador Coronel Vivida                                          |
|                                                                                          |
|               ATENCAO Acesso Restrito a pessoas autorizadas!                             |
|                                                                                          |
|         Administrador: PATRICK CATTO (catto@alunos.utfpr.edu.br)                         |
|                                                                                          |
-------------------------------------------------------------------------------------------$
exit
wr
```
</details>


- [ ] ![Switch Pato Branco](sw-pb-pc.txt)
- [ ] ![Switch Francisco Beltrão](sw-fb-pc.txt)
- [ ] ![Switch Coronel Vivida](sw-cv-pc.txt)



