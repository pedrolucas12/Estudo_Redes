Exemplos de Questoes da Prova 1

1 -  Sabe-se que o padrão IEEE802.11 refere-se a redes locais wireless. Esse tipo de rede também exige alguma técnica de acesso ao meio para evitar colisões entre as estações de trabalho? Se sim, explique (se houver mais de um método, escolha pelo menos um para
explicar; se houver mais de um, apresente pelo menos uma diferença entre eles).
    Sim, existem técnicas de acesso ao meio para evitar colisões entre as estações de trabalho. Um exemplo é o PCF (Point Coordination
    Function), no qual uma estação base interpela os demais dispositivos presentes na rede para verificar se há algum dado a ser
    transmitido. Há ainda o DCF (Distributed Coordination Function) que utiliza um algoritmo de backoff para detecção de colisões.

2 - Analise os relógios representativos para o protocolo de janela deslizante de 1 bit abaixo, com 3 bits p/ numeração dos quadros.
    (i) A janela de transmissão reúne um conjunto de números de sequência correspondentes a protocolos que o transmissor pode enviar
    futuramente. Em suma, mantém os números de sequência e quadros já enviados porém ainda não confirmados.
    (ii) Não, pois o valor máximo segue a fórmula 2^n - 1, de modo que para o caso de 2 bits, teríamos no máximo uma janela de
    transmissão igual a 2^2 -1 = 3.

3 - d. O protocolo stop-and-wait é um caso particular de algoritmo de janela deslizante com janela de transmissão igual a 1 

4 - e. Sincronismo ao nível de bit é uma necessidade tanto em transmissões síncronas quanto em transmissões
assíncronas

5 - No caso da rede Token Ring (IEEE 802.5), o que ocorre quando uma estação de posse da ficha é desligada, nos seguintes casos: (a) A
estação desligada é uma estação comum; (b) A estação desligada é a monitora.
    No primeiro caso (A) o pacote continuará rodando até que ele chegue na estação que irá monitorá-lo e ela identifique se a estação
    comum saiu do sistema. Já no segundo caso (B), o pacote continua no sistema até identificar a saída da estação monitora.

6 - a. nenhuma das anteriores

7 - Numa rede IEEE802.3, existem 4 estações com endereços MAC iguais a A, B, C e D para cada uma delas, conforme demonstra a figura
abaixo. 
    Com em uma rede 802.3 cada quadro transmite 1500 bytes, temos como retorno 4,048 que é arredondado para 5, nos dando 5
    quadros.
    Considerando ainda source address(6), type(2), destination address(6), data(1500), pad(0), preamble(8) e checksum(4), temos
    Quadro 1 a 4: 8 + 6 + 6 + 2 + 1500 + 0 + 4 = 1526
    Quadro 5: 8 + 6 + 6 + 2 + 72 + 0 + 4 = 98

8 - a. Nenhuma das alternativas

9 - e. 00011111010111110011101 

10 - c. Nehuma alternativa satisfaz

11 - “Em uma rede local Ethernet/IEEE802.3, uma estação só pode absorver o quadro, retirando-o do meio, se perceber que o quadro é
endereçado a ela”. Analise essa frase apontando todas as inconsistências percebidas e reescreva-a de forma correta.
    A frase descrita corresponde a uma rede local Ethernet/IEEE802.5, não a uma Ethernet/IEEE802.3. Assim, a frase correta seria Em uma
    rede local Ethernet/IEEE802.5, uma estação só pode absorver o quadro, retirando-o do meio, se perceber que o quadro é endereçado a ela.

12 - b. No TDM assíncrono, cada unidade de informação transmitida deve conter um cabeçalho com os endereços de origem e
destino

13 - a. Nenhuma resposta satisfaz

14 - a. Nenhuma das respostas satisfaz o enunciado. 

15 - Sobre o padrão Ethernet responda qual a necessidade de se ter o campo PAD na formação do quadro. O que aconteceria se esse campo não existisse no cabeçalho do Ethernet?
    Como o PAD tem o papel de ser usado de preenchimento para o tamanho total do quadro, se houvesse datas menores que 64 bytes,
    eles iram com tamanhos quebrados.

16 - e. Nenhuma das respostas 

17 - Uma das diferenças básicas entre switches e hubs 802.3 é que os switches procuram evitar os chamados “domínios de colisão”. Explique como os switches garantem isso
    Um switch basicamente interliga um conjunto de dispositivos por meio de uma placa integrada de alta velocidade. Para evitar colisões,
    eles apenas enviam quadros às portas que realmente são o destino final. O switch faz isso verificando o endereço ethernet. Diferente do
    hub, o switch não necessita do algoritmo CSMA/CD para programar suas transmissões, já que cada porta é seu próprio domínio de colisão.

--------------------------------------------------------

1. **Porque o software de rede é dividido em camadas?**
   - Para organizar e modularizar as funções, facilitando a implementação, manutenção e evolução dos sistemas de rede.

2. **Quais as diferenças entre a arquitetura TCP/IP e a RM-OSI/ISO?**
   - TCP/IP tem 4 camadas (Aplicação, Transporte, Internet, Link), enquanto RM-OSI/ISO tem 7 camadas (Aplicação, Apresentação, Sessão, Transporte, Rede, Enlace, Física).

3. **O que é padrão de facto e padrão de juri?**
   - **Padrão de facto:** Aceito pela maioria sem formalização oficial.
   - **Padrão de juri:** Oficializado por uma organização reconhecida.

4. **O que é uma PDU?**
   - Unidade de Dados de Protocolo; pacote de dados formatado em uma camada específica do modelo de rede.

5. **O que é primitiva de serviço?**
   - Comandos que definem operações básicas para a interação entre camadas de uma rede.

6. **Qual a definição de protocolo de comunicação?**
   - Conjunto de regras e procedimentos para troca de dados entre dispositivos.

7. **O que é um serviço orientado à conexão? E um serviço não orientado à conexão?**
   - **Orientado à conexão:** Requer estabelecimento de conexão (ex: TCP).
   - **Não orientado à conexão:** Envia dados sem conexão prévia (ex: UDP).

8. **Qual a diferença entre a largura de banda do meio físico e a largura de banda do sinal?**
   - **Largura de banda do meio físico:** Capacidade total de transmissão.
   - **Largura de banda do sinal:** Frequência de transmissão do sinal específico.
   - **Estratégias:** Multiplexação (FDM, TDM).

9. **Para que servem os modems?**
   - Convertem sinais digitais em analógicos e vice-versa para transmissão em redes telefônicas.

10. **Quais as diferenças entre modulação ASK, FSK e PSK?**
    - **ASK:** Amplitude.
    - **FSK:** Frequência.
    - **PSK:** Fase.

11. **Qual a relação entre largura de banda e taxa de transmissão?**
    - Maior largura de banda geralmente permite maior taxa de transmissão.

12. **O que é elemento de sinal em transmissões? O que é baud?**
    - **Elemento de sinal:** Unidade básica de sinalização.
    - **Baud:** Taxa de elementos de sinal por segundo.

13. **Qual a diferença entre um multiplexador TDM e um multiplexador FDM?**
    - **TDM:** Divide o tempo de transmissão.
    - **FDM:** Divide a frequência de transmissão.

14. **Qual a diferença entre meio físico guiado e não guiado?**
    - **Guiado:** Sinais via cabos (ex: fibra ótica).
    - **Não guiado:** Sinais via ar (ex: wireless).

15. **Quais as taxas de transmissão e qual padrão de rede local fazem uso de cabo coaxial?**
    - Varia, mas comuns em redes Ethernet antigas (10 Mbps).

16. **Qual a diferença entre uma rede local com cabeamento estruturado e uma rede sem esse tipo de cabeamento?**
    - **Estruturado:** Organização e eficiência.
    - **Sem:** Menos organização, potencialmente mais interferências.

17. **Quadro comparativo de cabos par trançado**
    - **Categoria 1:** Voz, baixa taxa.
    - **Categoria 3:** 10 Mbps, Ethernet.
    - **Categoria 5:** 100 Mbps, Fast Ethernet.
    - **Categoria 6:** 1 Gbps, Gigabit Ethernet.

18. **Qual a diferença entre fibras monomodo e multimodo?**
    - **Monomodo:** Longas distâncias, único modo de luz.
    - **Multimodo:** Curta distância, múltiplos modos de luz.

19. **Explique como funciona o protocolo RS-232**
    - Transmissão serial de dados, comunicação entre dispositivos (ex: computadores e modems).

20. **Diferenças entre redes de comutação de circuito e comutação de pacotes**
    - **Circuito:** Conexão dedicada.
    - **Pacotes:** Dados divididos em pacotes, roteados independentemente.

21. **Explique como funcionam os CODECs**
    - Codificam e decodificam sinais para compressão e transmissão de dados.

22. **Técnica PCM e PAM**
    - **PCM:** Amostragem e quantização de sinais analógicos.
    - **PAM:** Modulação de amplitude de pulsos.

23. **Funcionalidades da camada de enlace de dados**
    - Controle de acesso ao meio, detecção e correção de erros, enquadramento de dados.

24. **Enquadramento de bits na camada de enlace**
    - Necessário para delimitar pacotes; técnicas incluem contagem de caracteres, bytes especiais.

25. **Mecanismos de controle de erros mais comuns**
    - CRC, checksum, paridade.

26. **Distância de Hamming**
    - Medida de diferença entre duas sequências de bits; usada para detecção e correção de erros.

27. **Técnica de CRC e paridade longitudinal**
    - **CRC:** Detecção de erros por polinômios.
    - **Paridade:** Verificação simples de erros.

28. **Protocolo stop-and-wait**
    - Envia um quadro por vez e aguarda confirmação antes de enviar o próximo.

29. **Piggybacking em protocolos de enlace ponto-a-ponto**
    - Combina ACK com dados para eficiência.

30. **Relação entre bits para numerar quadros e tamanho da janela**
    - Mais bits permitem maior janela, mais quadros podem ser transmitidos antes de ACK.

31. **Diferença entre retransmissão seletiva e go-back-N**
    - **Seletiva:** Apenas quadros com erros.
    - **Go-back-N:** Retransmite a partir do erro.

32. **Diferença entre janela de transmissão e janela de recepção**
    - **Transmissão:** Quadros enviados.
    - **Recepção:** Quadros esperados.

33. **Protocolo ponto-a-ponto com go-back-N e retransmissão seletiva**
    - **Go-back-N:** Retransmite a partir do erro.
    - **Seletiva:** Retransmite apenas o quadro perdido.

34. **Mudanças do Ethernet para FastEthernet**
    - Aumento de velocidade (10 Mbps para 100 Mbps), melhorias em hardware e protocolos.

35. **Diferença entre acesso ao meio em Wi-Fi e redes cabeadas**
    - **Wi-Fi:** CSMA/CA, evita colisões.
    - **Cabeadas:** CSMA/CD, detecta colisões.

36. **Quadro Ethernet/IEEE802.3**
    - Campos: destino, origem, tipo/longitud, dados, FCS. Tamanho mínimo para detecção de colisões.

37. **Endereço MAC e tipos de endereçamento**
    - **MAC:** Identificador único.
    - **Unicast:** Um destinatário.
    - **Multicast:** Vários destinatários.
    - **Broadcast:** Todos na rede.

38. **Diferenças entre redes Simplex, half-duplex e full-duplex**
    - **Simplex:** Uma direção.
    - **Half-duplex:** Alterna direções.
    - **Full-duplex:** Ambas direções simultaneamente.

39. **Ethernet como TDM assíncrono**
    - Certo; Ethernet distribui tempo de transmissão de forma assíncrona.

40. **Protocolo IEEE802.5/Token Ring**
    - Estações transmitem em ordem, usando token.

41. **Token Ring: acesso ao meio determinístico ou não?**
    - Determinístico; ordem garantida pelo token.

42. **Diferença entre token e quadro de informações**
    - Token é pequeno, sem dados úteis; quadro contém dados.

43. **Diferenças entre redes Ethernet e Token Ring**
    - **Ethernet:** Acesso não determinístico.
    - **Token Ring:** Determinístico.

44. **Formato de um quadro IEEE802.11**
    - Campos: frame control, duration, addresses, sequence, data, FCS.