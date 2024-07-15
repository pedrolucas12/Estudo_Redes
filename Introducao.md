## Resumo de Introducao

**Atraso Nodal = Atraso de processamento + Atraso de enfileiramento + Atraso de transmissao + Atraso de propagacao**

- Atraso de Processamento
    - Tempo que o roteador leva para processar o pacote
    - Verificacao de erros
    - Determinacao do enlace de saida
    - Verificacao de bit de redundancia ciclica (CRC)
    - Checagem de cabecalho
    - Encaminhamento do pacote para o enlace de saida

- Atraso de Enfileiramento
    - Tempo que o pacote passa na fila de saida do roteador
    - Depende do nivel de congestionamento
    - Se a fila estiver vazia, o atraso de enfileiramento e

- Atraso de Transmissao
    - Tempo que o roteador leva para transmitir o pacote
    - Depende do tamanho do pacote e da taxa de transmissao do enlace

- Atraso de Propagacao
    - Tempo que o pacote leva para viajar do roteador de origem ao roteador de destino
    - Depende da distancia entre os roteadores e da velocidade de propagacao do meio

- Arquitetura de camadas = cada camada: realiza seu próprio serviço e usa os serviços da camada imediatamente inferior
    - Vantagens da arquitetura de camadas: modularidade (facilita a implementação e a modificação da implementação do serviço prestado pela camada)
    - Desvantagens: risco de duplicação de funcionalidades da camada inferior

- Protocolos são organizados em camadas = pilha de protocolos (formada por cinco camadas: aplicação, transporte, rede, enlace e física)
    - Camada de aplicação: aplicações de rede e seus protocolos
    - Camada de transporte: transporta mensagens da camada de aplicação entre os lados cliente e servidor; dois protocolos na Internet: TCP e UDP
    - Camada de rede: responsável pela movimentação de uma máquina pra outra de pacotes
    - Camada de enlace: Leva o pacote de um nó ao nó seguinte da rota, camada de rede depende dela
    - Camada física: movimenta bits individuais - dentro de um quadro - de um nó pro seguinte
    - Em cada camada, um pacote possui dois tipos de campo: cabeçalho, campo de carga útil