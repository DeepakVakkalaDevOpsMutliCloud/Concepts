### Problem 1
* I want to create a network of 500 devices and create two subnets with the capacity of 250 each
* note: \
  n: hostid bits \
  N: network id bits
Network
       
           2^n -2 ~= 500
           n = 9
           N = 32 - 9 = 23
           192.168.0.0/23
        
    * subnets = 2

```bash
2^n - 2 ~= 250
n = 8
N = 32 - 8 = 24

network ip: 192.168.0.0/23
network sm: 11111111.11111111.11111110.00000000
subnet sm:  11111111.11111111.11111111.00000000
-------------------------------------------------
                                     X
subnet 1 :            192.168.00000000.xxxxxxxx => 192.168.0.0/24
subnet 2 :            192.168.00000001.xxxxxxxx => 192.168.1.0/24
```

### Problem 2:
 I want a network of 1000 devices with two subnets of 500 each\
Network

```bash
2^n ~= 1000
n = 10
N = 32 - 10 = 22

172.16.0.0/22
```

Subnet = 2

```bash
2 ^ n ~= 500
n = 9
N = 32 - 9 = 23

network ip: 172.16.0.0/22
network SM: 11111111.11111111.11111100.00000000
subnet SM : 11111111.11111111.11111110.00000000
--------------------------------------------------
                                    X
subnet 1   :           172.16.0000000x.xxxxxxxx => 172.16.0.0/23
subnet 2   :           172.16.0000001x.xxxxxxxx => 172.16.2.0/23
```

#### Problem 3
I need a network for 4 subnets with 100 devices each\
Network:

```bash
2^n ~= 400
n = 9
N = 32 -9 = 23

network ip: 10.0.0.0/23
```

subnet
```bash
2^n ~= 100
n = 7
N = 32-7 = 25

network ip: 10.0.0.0/23
network SM: 11111111.11111111.11111110.00000000
subnet SM : 11111111.11111111.11111111.10000000
-------------------------------------------------
                                     X.X
subnet 1:                10.0.00000000.0xxxxxxx => 10.0.0.0/25
subnet 2:                10.0.00000000.1xxxxxxx => 10.0.0.128/25
subnet 3:                10.0.00000001.0xxxxxxx => 10.0.1.0/25
subnet 4:                10.0.00000001.1xxxxxxx => 10.0.1.128/25
```
#### Problem 4
Create 2 subnets of size 50000 devices  \
Network size = 100000
```bash
2^n ~= 100000
n = 17
N = 32 -17 = 15

network ip: 10.0.0.0/15

```

subnets
```bash
2^n ~= 50000
n = 16
N = 32 - 16 = 16

network ip: 10.0.0.0/15
network SM: 11111111.11111110.00000000.00000000
subnet SM:  11111111.11111111.00000000.00000000
------------------------------------------------
                            X.
subnet 1:         10.00000000.xxxxxxxx.xxxxxxxx  => 10.0.0.0/16
subnet 2:         10.00000001.xxxxxxxx.xxxxxxxx  => 10.1.0.0/16
```

### Problem 5

Create 8 subnets of 100 devices each \ 
Network size = 800

```bash
2^n ~= 800
n = 10
N = 22

network ip: 192.168.0.0/22 
```
Subnet

```bash
2^n ~= 100
n = 7
N = 25

network ip: 192.168.0.0/22
network sm: 11111111.11111111.11111100.00000000
subnet sm:  11111111.11111111.11111111.10000000
---------------------------------------------------
                                    XX.X

subnet 1:             192.168.00000000.0xxxxxxx 192.168.0.0/25
subnet 2:             192.168.00000000.1xxxxxxx 192.168.0.128/25
subnet 3:             192.168.00000001.0xxxxxxx 192.168.1.0/25
subnet 4:             192.168.000000XX.Xxxxxxxx 192.168.1.128/25
subnet 5:             192.168.000000XX.Xxxxxxxx 192.168.2.0/25
subnet 6:             192.168.000000XX.Xxxxxxxx 192.168.2.128/25
subnet 7:             192.168.000000XX.Xxxxxxxx 192.168.3.0/25
subnet 8:             192.168.000000XX.Xxxxxxxx 192.168.3.128/25
```