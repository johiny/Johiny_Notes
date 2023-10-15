- Los IOC (Indicador de Compromiso) son pistas o informacion que puede delatar un ataque cibernético estas contienen informacion como [[IP]] sospechosas, nombres de archivos, patrones de trafico inusuales, etc.
- Con esta informacion que comúnmente es compartida entre sistemas de inteligencia se pueden crear sistemas de seguridad que mitigan estos ataques.
- ***Example of an IOC*** #code
  ```plain text
  Malware File - "studiox-link-standalone-v20.03.8-stable.exe"
          sha256 6a6c28f5666b12beecd56a3d1d517e409b5d6866c03f9be44ddd9efffa90f1e0
          sha1 eb019ad1c73ee69195c3fc84ebf44e95c147bef8
          md5 3a104b73bb96dfed288097e9dc0a11a8
  DNS requests
          domain log.studiox.link
          domain my.studiox.link
          domain  _sips._tcp.studiox.link
          domain sip.studiox.link
  Connections
          ip 198.51.100.248
          ip 203.0.113.82
  ```