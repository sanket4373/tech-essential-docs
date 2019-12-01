- All traffic on the internet is split-up into messages called packets

- packet is a short message sent from one computer to another.

- ping is simpler than HTTP, but HTTP is not based on ping

- In everyday softwares the HTTP layers is implemented by programs such as browsers and servers

- Lower layers such as TCP is implemented in the Operating System.

- `nc` command is a thin wrapper over TCP 

| Layer      | Protols  | Concepts  |   
|------------|----------|-----------|
|Application |HTTP, SSH |URLs, password| 
|Transport   |TCP, UDP  |port numbers, sessions|   
|Internet    |IP        |IP Address, routes|
|Hardware    | wifi, ethernet, DSL|signal strength, access points|

- Each Top layer depends on the layer below it, however each layer functions independently and do not need worry about the layers below it


- ports distinguishes different applications/programs running on the same server. `nc` command is used to listen on to that port. 

- The port range that a normal (non-root) user can listen on is 1024 through 65535.

- But if you use root access (including sudo) then you can listen on ports down to 1.