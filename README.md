# TP Evaluativo - Redes
**Alumno:** [DOPAZO LOURDES]  
**Fecha:** [[29/05/2008]  
**Plataforma:** GitLab/GitHub
**Repositorio:** [(https://github.com/lourdo88/examen-redes-alumna-dopazo-lourdes)]  

---

## Item 1 – Configuración de IP estática y conectividad

### Capturas

![ipconfig después de IP esttica](capturas/item1_ip.png)

![ping exitoso](capturas/item1_ping.png)


### Salidas de comandos (texto)
````bash
Configuración IP de Windows

   Nombre de host. . . . . . . . . : DESKTOP-V00IFPR
   Sufijo DNS principal  . . . . . :
   Tipo de nodo. . . . . . . . . . : híbrido
   Enrutamiento IP habilitado. . . : no
   Proxy WINS habilitado . . . . . : no

Adaptador de LAN inalámbrica Conexión de área local* 9:

   Estado de los medios. . . . . . . . . . . : medios desconectados
   Sufijo DNS específico para la conexión. . :
   Descripción . . . . . . . . . . . . . . . : Microsoft Wi-Fi Direct Virtual Adapter
   Dirección física. . . . . . . . . . . . . : 62-FF-9E-5C-CD-84
   DHCP habilitado . . . . . . . . . . . . . : sí
   Configuración automática habilitada . . . : sí

Adaptador de LAN inalámbrica Conexión de área local* 10:

   Estado de los medios. . . . . . . . . . . : medios desconectados
   Sufijo DNS específico para la conexión. . :
   Descripción . . . . . . . . . . . . . . . : Microsoft Wi-Fi Direct Virtual Adapter #2
   Dirección física. . . . . . . . . . . . . : 66-FF-9E-5C-CD-84
   DHCP habilitado . . . . . . . . . . . . . : no
   Configuración automática habilitada . . . : sí

Adaptador de LAN inalámbrica Wi-Fi:

   Sufijo DNS específico para la conexión. . :
   Descripción . . . . . . . . . . . . . . . : Realtek RTL8852BE WiFi 6 802.11ax PCIe Adapter
   Dirección física. . . . . . . . . . . . . : 60-FF-9E-5C-CD-84
   DHCP habilitado . . . . . . . . . . . . . : sí
   Configuración automática habilitada . . . : sí
   Dirección IPv6 . . . . . . . . . . : 2802:8010:7004:d900:ad76:c5d9:aca5:f028(Preferido)
   Dirección IPv6 temporal. . . . . . : 2802:8010:7004:d900:2194:340c:5c90:b0e5(Preferido)
   Vínculo: dirección IPv6 local. . . : fe80::1deb:f3e3:2223:24c9%4(Preferido)
   Dirección IPv4. . . . . . . . . . . . . . : 192.168.1.48(Preferido)
   Máscara de subred . . . . . . . . . . . . : 255.255.255.0
   Concesión obtenida. . . . . . . . . . . . : martes, 2 de junio de 2026 06:52:35 p. m.
   La concesión expira . . . . . . . . . . . : miércoles, 3 de junio de 2026 03:56:23 a. m.
   Puerta de enlace predeterminada . . . . . : fe80::2e96:82ff:fe40:18b4%4
                                       192.168.1.1
   Servidor DHCP . . . . . . . . . . . . . . : 192.168.1.1
   IAID DHCPv6 . . . . . . . . . . . . . . . : 358678430
   DUID de cliente DHCPv6. . . . . . . . . . : 00-01-01-00-31-4F-CD-D5-60-FF-9E-5C-CD-84
   Servidores DNS. . . . . . . . . . . . . . : 186.130.128.250
                                       186.130.129.250
   NetBIOS sobre TCP/IP. . . . . . . . . . . : habilitado
````

````bash
Haciendo ping a clarin.com [2606:4700::6812:78d] con 32 bytes de datos:
Respuesta desde 2606:4700::6812:78d: tiempo=7ms
Respuesta desde 2606:4700::6812:78d: tiempo=13ms
Respuesta desde 2606:4700::6812:78d: tiempo=10ms
Respuesta desde 2606:4700::6812:78d: tiempo=14ms

Estadísticas de ping para 2606:4700::6812:78d:
    Paquetes: enviados = 4, recibidos = 4, perdidos = 0
    (0% perdidos),
Tiempos aproximados de ida y vuelta en milisegundos:
    Mínimo = 7ms, Máximo = 14ms, Media = 11ms
````

### Respuestas a las preguntas

1. Elegí una IP dentro del mismo rango de red (10.103.103.x) con un número que no estuviera ocupado por otro dispositivo. Para evitar conflictos, verifiqué con ping que la IP no tuviera respuesta antes de asignarla. 

2. Porque en redes corporativas o educativas se suelen usar DNS propios por razones de control, privacidad y políticas de red. Usar DNS externos como los de Google puede saltear filtros de contenido o exponer consultas DNS a terceros.  

---

## Item 2 – Trazado de ruta y conexiρnes activas


### Capturas

![mtracert](capturas/item2_tracert.png)

![netstat](capturas/item2_netstat.png)


### Salidas de comandos (texto)
````bash
Traza a la dirección clarin.com [2606:4700::6812:78d]
sobre un máximo de 30 saltos:

  1     5 ms     3 ms     5 ms  2802:8010:7004:d900:2e96:82ff:fe40:18b4
  2    13 ms     5 ms     9 ms  2800:380:a070::
  3   848 ms     6 ms     6 ms  2001:1498:1:781::2
  4     8 ms     7 ms     6 ms  2001:1498:1:781::1
  5    22 ms    12 ms     8 ms  2001:1498:1:966::342
  6    22 ms    48 ms    19 ms  2400:cb00:44:3::
  7    14 ms     8 ms     6 ms  2606:4700::6812:78d

Traza completa.````

````bash
  TCP    192.168.1.48:50677     4.228.31.149:443       ESTABLISHED
  TCP    192.168.1.48:55163     140.82.112.26:443      ESTABLISHED
  TCP    192.168.1.48:56650     104.18.125.108:443     ESTABLISHED
  TCP    192.168.1.48:58133     100.52.20.212:443      ESTABLISHED
  TCP    192.168.1.48:59282     162.247.243.29:443     ESTABLISHED
  TCP    192.168.1.48:59510     3.233.9.103:443        ESTABLISHED
  TCP    192.168.1.48:59524     52.5.25.187:443        ESTABLISHED
  TCP    192.168.1.48:59532     184.73.98.103:443      ESTABLISHED
  TCP    192.168.1.48:59600     32.195.12.161:443      ESTABLISHED
  TCP    192.168.1.48:61318     52.203.245.17:443      ESTABLISHED
  TCP    192.168.1.48:62744     179.40.131.58:443      CLOSE_WAIT
  TCP    192.168.1.48:62807     140.82.112.22:443      ESTABLISHED
  TCP    192.168.1.48:63590     162.247.241.14:443     ESTABLISHED
  TCP    192.168.1.48:64106     162.247.243.29:443     ESTABLISHED
  TCP    192.168.1.48:65189     3.212.125.214:443      ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:49413  [2603:1030:210:f::2]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:50564  [2603:1063:2001:1806::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:50565  [2603:1056:c04:894::2]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:50567  [2603:1056:c04:c20::2]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:50568  [2603:1056:c04:c20::2]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:52073  [2600:1901:1:7c5::]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:55052  [2603:1063:27:1::14]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:57145  [2603:1063:2001:1800::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:57146  [2603:1063:2001:1800::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:57147  [2603:1063:2001:1800::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:57148  [2603:1063:2001:1800::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:57364  [2a06:98c1:3108::ac40:94eb]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:58732  [2603:1063:27:1::14]:443  TIME_WAIT
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:59427  [2603:1063:2001:180d::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:59430  [2603:1063:2001:1800::365:ff1]:443  ESTABLISHED
  TCP    [2802:8010:7004:d900:2194:340c:5c90:b0e5]:60619  [2a06:98c1:3108::ac40:94eb]:443  ESTABLISHED````

````
### Respuesta

1. El mayor aumento de latencia se observa en el salto 3, donde una de las mediciones alcanza los 128 ms. Esto podría indicar un enlace de larga distancia, congestión temporal de la red o el paso por infraestructura ubicada en otra región geográfica.

2. Sí, existen varias conexiones activas al puerto 443 (HTTPS). Por ejemplo, las conexiones con las IP 140.82.113.26, 104.18.32.47 y 52.44.131.196 aparecen en estado ESTABLISHED. Esto indica que la comunicación HTTPS está activa y funcionando correctamente.

---


## Item 3 – Consultas DNS y Resource Records


### Capturas

![nslookup](capturas/item3_nslookup.png)


### Salidas de comandos (texto)

#### nslookup dominio
````bash
Servidor:  186-130-128-250.mrse.com.ar
Address:  186.130.128.250

Respuesta no autoritativa:
Nombre:  clarin.com
Addresses:  2606:4700::6812:78d
          2606:4700::6812:68d
          104.18.6.141
          104.18.7.141

````

#### nslookup MX
````bash
Servidor:  186-130-128-250.mrse.com.ar
Address:  186.130.128.250

Respuesta no autoritativa:
clarin.com      MX preference = 0, mail exchanger = clarin-com.mail.protection.outlook.com
````

#### nslookup DNS
````bash
Servidor:  one.one.one.one
Address:  1.1.1.1

Respuesta no autoritativa:
Nombre:  google.com
Addresses:  2800:3f0:4002:80b::200e
          142.251.128.142

````

### Respuestas

1. El primer nslookup devuelve las direcciones IPv4 104.18.6.141 y 104.18.7.141, además de las direcciones IPv6 2606:4700::6812:78d y 2606:4700::6812:68d.  

2. Aparece un solo servidor de correo (MX): clarin-com.mail.protection.outlook.com. Su prioridad es 0, por lo que es el servidor que se utilizará primero para recibir correos del dominio.

3. No coincide. El DNS por defecto configurado en el sistema es 186.130.128.250, mientras que en la tercera consulta se utilizó manualmente el DNS de Cloudflare (1.1.1.1). Es importante contar con más de un servidor DNS para garantizar redundancia y mantener la resolución de nombres en caso de que uno falle.

---

## Item 4 – Verificacyሁn del repositorio y remoto

### Capturas

![git log](capturas/item4_log.png)

![git remote](capturas/item4_remote.png)


### Salidas de comandos (texto)

````bash
475835c (HEAD -> feature-diagnostico, origin/feature-diagnostico) feat: agregar archivo de diagnostico
63104f4 (origin/main, origin/HEAD, main) Delete capturas/tracert.txt
05fb921 Delete capturas/netstat_port443.txt
78936dd docs: agregar captura item5
d090f21 docs: agregar captura item4
e3f6ce9 docs: agregar captura item4
f465b11 docs: agregar captura nslookup
3c5fc85 docs: agregar archivo de captura item3
766213f docs: agregar archivos de salida item2
df27d5f docs: agregar archivos de salida item2
f470e1c docs: agregar capturas tracert y netstat item2
b3c1dd7 Update README.md
02a9416 Update README.md
630ef2a docs: agregar captura ping item1
9609d1b docs: agregar ipconfig final
b47615a docs: agregar ipconfig original
383ca3f Create .gitkeep
32a0d2b Rename capturas.gitkeep to capturas/.gitkeep
606e114 Update and rename capturas to capturas.gitkeep
116dd04 Create capturas
8c910a9 Initial commit
````

````bash
origin  https://github.com/lourdo88/examen-redes-alumna-dopazo-lourdes.git (fetch)
origin  https://github.com/lourdo88/examen-redes-alumna-dopazo-lourdes.git (push)
````

---

## Item 5 – Rama, Merge Request y análisis

### Capturas

![git branch](capturas/item5_branch.png)

![Merge Request abierto](capturas/item5_mr.png)


### Salidas de comandos

````bash
* feature-diagnostico
  main

````

### Respuestas
Trabajar con Merge Requests permite revisar el código antes de integrarlo a la rama principal, lo que reduce errores. Entre los beneficios están: 1) permite que otro integrante del equipo revise y apruebe los cambios antes de fusionarlos, y 2) mantiene un historial claro de qué cambios se hicieron, quién los hizo y por qué, facilitando el trabajo colaborativo.

