## Resumo de Camada de Aplicacao

**OBS: Antes que o cliente e servidor possam começar a enviar dados um pro outro, eles precisam se apresentar e estabelecer uma conexão TCP - uma ponta é conectada ao socket cliente e a outra é conectada ao socket servidor; No UDP o servidor precisa anexar um endereço de destino ao pacote antes de deixá-lo no socket.**

- Objetivo
    - Permitir ter acesso a rede
    - Foco na comunicacao entre processos localizados em hosts distintos

- Arquitetura
    - Cliente-Servidor
        - Servidor: Precisa estar "escutando" na porta
        - Cliente: Faz a solicitacao
    - Peer-to-Peer  
        - Ambos podem enviar e receber dados
    - Hibrida
        - Clientes contactam servidores para obter informacoes
        - Clientes se comunicam entre si - Skype
    
- Comunicacao
    - Socket
        - Ponto de comunicacao
        - Interface entre processo de aplicacao e camada de transp
    - Enderecamento de Processos
        - Endereco do hospedeiro + numero de porta (identificador do processo)
    
- Protocolo de aplicacao
    - O que e definido pelo protocolo
        - Tipos de mensagens
        - Sintaxe das mensagens
        - Semantica das mensagens
        - Regras de sincronizacao
    - Necessidade de servico de uma aplicacao
        - Leva em consideracao : Confiabilidade, Largura da banda, temporizacao, seguranca
    - HTTP
        - Transferencia de hipertexto
        - Baseado na arquitetura cliente-servidor
        - Componentes : Pagina Web, Cliente Web (Browser), Servidor Web, URL, HTML
        - Tipos de Docs Web : Estaticos(ARQUIVOS HTML), Dinamicos(PHP), Ativos(JavaScript)
        - Protocolo : 
            - Requer transmissao confiavel - TCP
            - Nao especifica como a pagina e interpretada
            - Nao ha controle de estado de comunicacao
            - Conexoes nao persistentes (desvantagem : estabelecer conexao a cada requisicao)
            - Conexoes persistentes (HTTP/1.1)
        - Formato de Mensagem
            - Requisicao
            - Resposta
        - Metodos: GET, POST, PUT, DELETE 
    - FTP
        - Transferencia de arquivos
    - SMTP
        - Transferencia de correio eletronico
    - POP3 E IMAP
        - Acesso a correio eletronico
    - DNS
        - Resolucao de nomes de dominio

- DNS
    - Servico usado para mapear nomes usados por aplicacoes em enderecos IP
    - Hierarquia de nomes servidores DNS
        - Root DNS Servers
        - Top-Level Domain (TLD) Servers
        - Authoritative DNS Servers
        - Local DNS Servers
    - Servidores DNS
        - Primarios : mantem os registros
        - Secundarios : copia dos registros do servidor primario
        - Secundarios Caching only : mantem caches de consultas feitas
    - Protocolo DNS
        - Resolver usa a porta TCP ou UDP 53
        - Um pedido de resolucao pode ser feito pelo NS ou reencaminhado para o NS root
        - Vai para o NS responsavel
        - O NS responsavel responde com o endereco IP