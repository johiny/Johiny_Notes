- nmap es la herramienta predilecta, la navaja suiza para explorar redes y descubrir un montón de de datos sobre estas, mira aqui algunos comandos muy útiles.
  ***nmap Common Uses*** #code
  ```linux
  nmap [ip] # scan tcp ports (most common ports)
  nmap -sU [ip] # scan udp ports (less frequent)
  nmap -sV [ip] # scan ports and get more info about the software in them like OS version
  nmap -A [ip] # full scan -A comes from All this type of scan is very agressive and can be detected more easily
  ```