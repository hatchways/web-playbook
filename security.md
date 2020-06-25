## How does HTTPS work? What is the difference between HTTP and HTTPS?
- [HTTPS](https://en.wikipedia.org/wiki/HTTPS) is a secure version of [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) that uses [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) for communication encryption
- Unlike HTTP, which can only use [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) _for data transfer_, HTTPS can use either TCP or [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol)
  - UDP is used when data loss is tolerable (e.g. in gaming, streaming, etc.)
### Handshake protocol for HTTPS
  - [TLS handshake](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/#:~:text=A%20TLS%20handshake%20is%20the,and%20agree%20on%20session%20keys.) is the current process for establishing a secure connection between a client and a server
    - Sometimes referred to as an "SSL handshake", but keep in mind that [SSL encryption](https://www.cloudflare.com/learning/ssl/what-is-ssl/) is mostly deprecated ([last update was in 1996!](https://en.wikipedia.org/wiki/Transport_Layer_Security#Secure_Data_Network_System)) 
      - Most modern browsers don't support SSL encryption at all

Check out [this presentation](https://docs.google.com/presentation/d/1nn2VisaJ8egn3Gu6GwDNyYCNzCZmDQHwsHNL1mAdmM0/edit?usp=sharing) for more details