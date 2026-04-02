# Portifolio
# Relatório Técnico: Fundamentos do Protocolo TCP/IP
**Referência Bibliográfica:** TANENBAUM, Andrew S.; WETHERALL, David J. *Redes de Computadores*.

---

## 1. Contexto Histórico
O modelo **TCP/IP** não foi uma criação puramente teórica, mas sim o resultado de necessidades práticas de defesa e pesquisa (projeto ARPANET). Diferente do modelo OSI, o TCP/IP foi desenvolvido para ser resiliente, permitindo que a comunicação entre máquinas ocorresse mesmo se parte da rede física estivesse inativa.

## 2. Camadas do Modelo TCP/IP
O modelo é estruturado em quatro camadas principais, onde cada nível provê serviços para a camada superior:

* **Aplicação:** Onde residem os protocolos que interagem com o usuário (HTTP, DNS, FTP).
* **Transporte:** Responsável pela comunicação host-a-host (origem-destino). É aqui que o fluxo de dados é controlado.
* **Internet:** Define o endereçamento lógico (IP) e como os pacotes devem ser roteados através de diferentes redes.
* **Acesso à Rede:** Trata da interface física e do envio de quadros de dados pelo meio (Ethernet, Wi-Fi).

---

## 3. Protocolos de Transporte: TCP vs. UDP
A escolha entre TCP e UDP depende da prioridade da aplicação: **confiabilidade** ou **velocidade**.

| Característica | TCP (*Transmission Control Protocol*) | UDP (*User Datagram Protocol*) |
| :--- | :--- | :--- |
| **Conexão** | Orientado à conexão (*Handshake*) | Não orientado à conexão |
| **Confiabilidade** | Alta (garante entrega e ordem) | Baixa (melhor esforço, pode perder dados) |
| **Velocidade** | Menor (devido ao controle de erro) | Alta (mínimo de cabeçalho) |
| **Exemplos** | Navegação Web, E-mail, SSH | Streaming, VoIP, Jogos Online |

---

## 4. Portas Lógicas e Identificação de Serviços
Para que o sistema operacional saiba qual aplicação deve receber os dados que chegam, ele utiliza o conceito de **Portas**. Enquanto o endereço IP identifica o computador, a porta identifica o serviço específico dentro dele.

> **Portas de 16 bits:** Variam de 0 a 65.535.

### Principais Portas e Protocolos:
* **Porta 21:** FTP (Transferência de Arquivos)
* **Porta 22:** SSH (Acesso Remoto Seguro)
* **Porta 53:** DNS (Resolução de nomes de domínio)
* **Porta 80:** HTTP (Tráfego Web padrão)
* **Porta 443:** HTTPS (Tráfego Web criptografado)

---

## 5. Conclusão
Conforme descrito por Tanenbaum, a flexibilidade do TCP/IP permitiu que ele se tornasse o padrão global. A separação clara entre a camada de Internet (que move os pacotes) e a camada de Transporte (que cuida da integridade ou velocidade) é o que torna a Internet escalável para bilhões de dispositivos.
