PERSPECTIVAS PARA ARQUITETAR SOFTWARE DE QUALIDADE

- Performance
- Escalabilidade
- Resiliencia

PERFORMANCE

- É o desempenho que um software possui para completar um determinado worload
- As unidades de medida para avaliarmos a performance de um software são:
	- Latencia ou "response time"
	- Throughput

- Ter um software performático é diferente de ter um software escalável

MÉTRICAS PARA MEDIR A PERFORMANCE

- Diminuindo a latencia
	- Normalmente medida em milliseconds
	- É afetada pelo tempo de processamento da aplicação, rede e chamadas externas

- Aumentando throughput
	- Quantidade de requisiçoes

PRINCIPAIS RAZOES PARA BAIXA PERFORMANCE

- processamento ineficiente
- Recursos computacionais limitados
- Trabalhar de forma bloqueante
- Acesso serial a recursos

PRINCIPAIS FORMAS PARA AUMENTAR A EFICIENCIA

- ESCALA DA CAPACIDADE COMPUTACIONAL(CPU, Disco, Memória, Rede)
- Lógica por trás do software (Algoritmo, queries, overhead de frameworks)
- Concorrencia e paralelismo
- Banco de dados (Tipos de bancos, schema)
- Caching

CAPACIDADE COMPUTACIONAL:
ESCALA VERTICAL VS HORIZONTAL


DIFERENÇA ENTRE CONCORRENCIA E PARALELISMO
- "Concorrencia é sobre lidar com muitas coisas ao mesmo tempo. Paralelismo é fazer muitas coisas ao mesmo tempo"

CACHING
- Cache na borda/Edge computing
- Dados estáticos
- Páginas web
- Funcoes internas
 - Evita reprocessamento de algoritmos pesados
 - Acesso ao banco de dados
- Objetos

CACHING: EXCLUSIVO VS COMPARTILHADO

EXCLUSIVO

- Baixa latencia
- Duplicado entre os nós
- Problemas relacionados a sessoes

COMPARTILHADO

- Maior latencia
- Não há duplicação
- Sessoes compartilhadas
- Banco de dados externo
 - MySQL
 - Redis
 - Memcache

CACHING:EDGE COMPUTING
- Cache realizado mais próximo ao usuário
- Evita a requisição chegar até o cloud Provider / Infra
- Normalmente arquivos estáticos
- CDN - Content Delivery Network
- Cloudflare workers
- Vercel

