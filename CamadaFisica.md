## Resumo de Camada Fisica

**A taxa de transmissao depende do metodo de codificacao e da qnt de alteracoes que o sinal sofre.**

- Transmissao de Dados
    - O sucesso da transmissao de dados depende de 2 fatores: qualidade do sinal e das caracteristicas do meio de transmissao
    - Meios de Transmissao
        - Guiados ( Fibra optica)
        - Nao Guiados (Radio)
    - Forma de Utilizacao do Meio
        -Ponto a Ponto ( sem dispositivos intermediarios como amplificadores)
        -Multiponto ( com dispositivos intermediarios)
    - Tipo de Dialogo
        - Simplex ( unidirecional)
        - Half-Duplex ( bidirecional, mas nao simultaneo)
        - Full-Duplex ( bidirecional e simultaneo)

- Relacao entre Taxa de Transmissao e Largura de Banda
    - Taxa de Transmissao = Largura de Banda * log2(1 + S/N)
    - S/N = Relacao sinal ruido
    - Largura de Banda = B
    - Taxa de Transmissao = R
    - Uma largura de banda pode suportar varias taxas de transmissao
    - Quanto mais limitada a largura de banda, menor a taxa de transmissao
    - Quanto maior a largura de banda, maior a taxa de transmissao

- Imperfeicoes na Transmissao
    - Atenuacao
        - Perda de intensidade do sinal
    - Distorsao
        - Alteracao da forma do sinal
    - Ruido
        - Termal
        - Intermodulacao (soma de sinais)
        - Cross-talk (sinal de um fio interfere no outro)
        - Impulsivo (sinal de curta duracao)

- Capacidade do Canal
    - Tx de dados : tx de dados em bits por segundo
    - Largura de Banda : largura de banda em Hz
    - Ruido : nivel medio de interferencias
    - Tx de erros 
           
- Codificacao de Dados
    - Tipos de Dados
        - Analogico
        - Digital
    - Sinais ( ondas senodais ou quadradas geradas por codificador)
    - Sinais Digitais transmitindo dados digitais
        - O receptor deve conhecer o tempo de cada bit
        - O receptor deve conhecer a relacao entre as voltagens e a representacao dos bits zero e um
    - Formas de Codificacao:
        - ON-OFF : 1 = sinal, 0 = sem sinal
        - NRZ : 1 = sinal, 0 = sinal invertido
        - Manchester : 1 = transicao de 0 para 1, 0 = transicao de 1 para 0
        - Manchester Diferencial : 1 = Nao ha transicao, 0 = transicao
    - Os metodos ON-OFF e NRZ tem as seguintes caracteristicas:
        - Capacidade de aproveitar melhor a largura
        - Facilidade de sincronizacao
        - Dificuldade de representar sequencias continuas de zero ou uns
        - Sujeito a atenuacao
    - Os metodos Manchester e Manchester Diferencial tem as seguintes caracteristicas:
        - Flexibilidade para sensibilização e recuperação de relógio (RLL) no receptor
        - Menos sujeito a atenuacao
        - Largura de banda maior

- Esquema de codificacao e tx de transmissao
    - Fatores que deve analisar para escolher o metodo de codificacao:
        - Custo e complexidade dos circuitos
        - Forma de deteccao de erros
        - Imunidade ao ruido

- Transmissao Analogica
    - Fibra otica e um meio de transmissao que usa luz para transmitir dados
    - A modulacao e necessario para alterar o espectro de frequencias da fonte para mais altas
    - O equipamento utilizado para injetar dados no sistema de transmissão analógico é denominado MODEM
    - Tecnicas de codificacao de bits em sinais analogicos:
        - ASK (Amplitude Shift Keying)
            - Os 2 sinais sao representados por 2 amplitudes diferentes
        - FSK (Frequency Shift Keying) - menos suscetivel a ruido
            - Os 2 sinais sao representados por 2 frequencias diferentes
        - PSK (Phase Shift Keying)
            - Os 2 sinais sao representados por 2 fases diferentes

- Transmissao Analogica x Digital
    - Vantagens da transmissao digital:
        - Tecnologia Digital
        - Integridade dos Dados
        - Utilizacao da capacidade
        - Seguranca e Privacidade
        - Integracao

- Multiplexacao
    - Serve para transmitir varios sinais em um unico meio de transmissao, assim aproveitando melhor a largura de banda
    - Tipos de Multiplexacao:
        - FDM (Frequency Division Multiplexing)
            - Largura da banda util excede a largura de banda do sinal
            - Largura de banda e dividida em canais
            - Problemas a serem resolvidos: 
                - Cross-talk
                - Ruido de intermodulacao
        - TDM (Time Division Multiplexing)
            - A taxa de transmissao excede a taxa de dados a serem transmitidos
            - Multiplos sinais sao transmitidos em intervalos de tempo
            - Sincrono : slots de tempo são pré-definidos e fixos para cada fonte
            - Controle de Enlace:
                - Apesar de não precisar de controle de fluxo e nem de erros, a TDM precisa lançar mão de duas técnicas de enquadramento e sincronização
        - TMD Estatistico
            - Alocacao de intervalos de tempo conforme a necessidade
            - Alocacao de intervalos de tempo conforme a demanda
        - SONET 
            - Torna possivel a interconexao de diferentes operadoras
            - Unifica os sistemas digitais
            - Maneira de multiplexar sinais digitais
            - Suporte para OAM (Operation, Administration and Maintenance)
        