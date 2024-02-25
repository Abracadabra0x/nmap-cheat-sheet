How to use nmap better and faster
### Installation

```
-> apt install libssl-dev autoconf make g++ subversion

-> svn co https://svn.nmap.org/nmap/

-> cd nmap

-> ./configure

-> make

```

### Check the Help menu and version

```
## To check the version you can use
    -> nmap -V
    
## To get a help with command you can use
    -> nmap -h
    
## or
    -> man nmap
```

### Basic Nmap Commands

```
Verbos output

	-> nmap -v {target-ip} allow you to get more detailed information during the scan

 Scan multie Ip Adress
 
    you can provid nmap with more then one ip adress just by adding a space
    -> nmap 127.0.0.1 128.1.2.3 192.168.1.1

	 Scan the SubNet (CIDIR)
     nmap 192.168.1.1/24

	Scan Ip Range
    -> nmap 192.168.1-10

	 Scan A list of Ip Address
    -> nmap -iL filename.txt

	 Exclued your target
	 
    -> nmap 192.168.1.1/24 --exclude 192.168.1.5
    
    -> nmap 192.168.1.1/24 --excludefile filename.txt

	 Show only the open ports
	 
    -> nmap --open 192.168.1.1

## How to do Fast Scan using nmap

    -> nmap -F {Ip Adress} -> only common port are check for

  
## Os Detection with nmap

    -> nmap -O {Ip}

  
## nmap Service Detection

    -? nmap -sV {ip}

  
## Nmap is slow ?

        -> nmap -T0-5 {ip} // you have opttion form 0 to 5

```

### Nmap Template used in videos

```
nmap -A -p- -T4 -v {ip}

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN

nmap -sC -sV -oA nmap/result {ip}

nmap -sV -sC -v -p- --min-rate=1000

nmap -sV -sC -oA scans/initial {ip}
```
