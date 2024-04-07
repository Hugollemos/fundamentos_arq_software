RESILIENCIA
- Resiliencia é um conjunto de estratégias adotadas intencionalmente para a adaptação de um sistema quando uma falha ocorre.
- Ter estratégias de resiliencia nos possibilita minimizar os riscos de perda de dados e transacoes importantes para o negócio.

PROTEGER E SER PROTEGIDO
- Um sistema em uma arquitetura distribuída precisa adotar mecanismos de autopreservação para garantir ao máximo sua operação com qualidade.
- Um sistema precisa não pode ser "egoísta" ao ponto de realizar mais requisicoes em um sistema que está falhando
- Um sistema lento no ar muitas vezes é pior do que um sistema fora do ar.

Health check
- Sem sinais vitais, não é possível saber a "saúde" de um sistema
- Um sistema que não está saudável possui uma chance de se recuperar caso o tráfego pare de ser direcionado a ele temporariamente.
- Health check de qualidade

RATE LIMITING
- Protege o sistema baseado no que ele foi projetado para suportar
- Preferencia programada por tipo de client

CIRCUIT BREAKER
- protege o sistema fazendo com que as requisicoes feitas para ele sejam negadas. EX:500
- Circuito fechado = Requisicoes chegam normalmente
- Circuito aberto = Requisicoes não chegam ao sistema. Erro instantaneo ao client
- Meio aberto = Permite uma quantidade limitada de requisicoes para verificação se o sistema tem condicoes de voltar ao ar integralmente

API GATEWAY
- centralizar todas as requisicoes da aplicação
- Garante que requisicoes "inapropriadas" cheguem até o sistema: Ex: usuário não autenticado.
- Implementa políticas de Rate Limiting, Health check, etc.

SERVICE MESH
- Controla o tráfego de rede
- Evita implementacoes de proteção pelo próprio sistema.
- mTLS
- Circuit breaker, retry, timeout, fault injection, etc

TRABALHAR DE FORMA ASSÍNCRONA
- Evita perda de dados
- Não há perda de dados no envio de uma transação de o server estifer fora
- Servidor pode processar a transação em seu tempo quando estiver online
- Entender com profundidade o message broker / sistema de stream

GARANTIAS DE ENTREGA: RETRY

GARANTIAS DE ENTREGA: KAFKA

===============
SITUACOES COMPLEXAS
- O que acontece se o message broker cair?
- Haverá perda de mensagens?
- Seu sistema ficará fora do ar?
- Como garantir resiliencia?


