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
