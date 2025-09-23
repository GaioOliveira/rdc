# Aula 7 - Segmentação de Rede com VLAN
## Cenário com 3 VLAN: Vendas, TI e RH
Inicialmente, definimos uma rede com endereços IPv4: 192.168.1.0/24.
Daí, reservarmos o endereço 192.168.1.1 para o default gateway e utilizamos os endereços a partir de 192.168.1.2 para os hosts da rede.
Conectamos todos os hosts ao switch SW1 e passamos a utilizar o modo CLI do switch para configurar as VLAN, na seguinte ordem:
1) Acessamos o modo privilegiado com o comando:
``` enable```
2) Verificamos as VLAN existentes com o comando:
``` show vlan brief ```
3) Acessamos o modo de configuração global:
```configure terminal ```
4) Demos um novo nome ao switch:
```hostname SW1```
5) Criamos a primeira VLAN do cenário proposto:
```vlan 10 ```
6) Demos um nome à VLAN 10:
```name VENDAS ```
7) Repetimos os passos 4 e 5 para as outras duas VLAN (20 e 30).
8) Escolhemos um conjunto de portas no SW1 (portas FastEthernet 0/1 e 0/2):
```interface range Fa0/1-2```
9) Definimos que tais portas devam pertencer à VLAN 10:
```switchport access vlan 10```
10) Definimos que essas portas funcionarão como portas de acesso:
```switchport mode access```

