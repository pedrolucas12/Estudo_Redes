## Resumo da Camada de Transporte

- **Processos = aplicacoes do usuario**
- **Portas = enderecos de tranporte - n inteiros de 16 bits**
- **Segmentos = pacotes ( na camada de aplicacao)**

Objetivo: oferecer transporte de dados entre processos de usuario (camada de aplicacao) em hosts distintos.

Modalidade de transporte:
- Nao Confiavel (simples)
    - UDP
- Confiavel (complexo)
    - TCP
    - Logica:
        - Conexao - Three-way handshake
        - Sequenciamento
        - Controle de fluxo
        - Controle de Erros
        - Encerra conexao
        - **Dados chegando em ordem e sem erros no receptor**

Three-way handshake:
- Cliente deve estar "escutando" na porta
- Cliente envia SYN = 1 e ACK = 0
- Servidor envia SYN = 1 e ACK = 1
- Cliente envia ACK = 1 e SYN = 0

Por que camada de transporte?
- A camada de rede oferece um servico de comunicacao entre hosts, e para prover um paralelismo no host e para tratar apenas um processo

Multiplexacao:
- Protocolo de transporte aceita mensagem de varios processos

Demultiplexacao:
- Entrega a mensagem para varios processos

Enderecamento:
- Processos sao vinculados a portas

Paradigma cliente-servidor:
- Processo que no cliente (host local) solicita servicos a outro processo no servidor (host remoto)

Servicos de transporte:
- Protocolo UDP
    - Datagramas de tamanho variavel
    - Nao estabelece conexao
    - Pequeno overhead no cabecalho
    - Nao tem controle de fluxo
    - Nao tem controle de congestionamento
    - Porta de origem = 16 bits = Porta de destino
    - Tamanho Datagrama = 16 bits = Soma de verificacao
    - Voltado para aplicacao que suportem perda de dados
    - API Socket
        - sendto
            - result = sendto(socket, buffer, tamanho, flags, (SOCKADDR*) &servidor, sizeof(SOCKADDR))
            - Envia dados
        - recvfrom
            - result = recvfrom(socket, buffer, tamanho, flags, (SOCKADDR*) &cliente, sizeof(SOCKADDR))
            - Recebe dados
        - close
            - result = close(socket)
            - Encerra conexao

- Protocolo TCP
    - Conexao fim-a-fim de um para um (sem multicast)
    - Os dados sao enviados em segmentos (MSS)
    - Envolvem:
        - Protocolo de comunicacao - TCP
        - Endereco do cliente e do servidor - SOCKADDR_IN
    - Estabelece conexao
    - Porta de origem = 16 bits = Porta de destino = Soma de verificacao
    - Numero de sequencia = 32 bits = Numero de Reconhecimento
    - Bytes transmitidos sao numerados
    - Campo de reconhecimento indica o proximo byte esperado
    - Voltado para transmissao confiavel de dados
    - Janela deslizante = Receptor indica quantos bytes pode receber
    - Funcoes similares a Go-Back-N e Stop-and-Wait
        - O receptor recebe segmentos ordenados, devolve um ACK e entrega os bytes para camada de aplicacao
        - O receptor enviar so reconhecimento cumulativos, ele nao reconhece segmentos fora de ordem e armazena em buffer os segmentos fora de ordem
    - API Socket
        - connect
            - result = connect(socket, (SOCKADDR*) &servidor, sizeof(SOCKADDR))
            - Conexao ponto-a-ponto
        - send
            - result = send(socket, buffer, tamanho, flags)
            - Envia dados
        - recv
            - result = recv(socket, buffer, tamanho, flags)
            - Recebe dados
        - close
            - result = close(socket)
            - Encerra conexao
        - listen
            - result = listen(socket, tamFila)
            - Espera por conexao
        - accept
            - result = accept(socket, (SOCKADDR*) &cliente, sizeof(SOCKADDR))
            - Aceita conexao

Controle de Erros:
- Checksum
    - Verifica se os dados foram corrompidos
- Retransmissao
    - Reenvio de segmentos nao reconhecidos
- RTO
    - Tempo de retransmissao
- Finaliza a transmissao confiavel de dados
