### domain
Contém o código de negócio e sua lógica e não tem dependência externa: nem em frameworks (NestJS no nosso caso), nem de use_cases ou pacotes de infraestrutura.

### use_cases
Casos de uso é como um condutor. Dependerá apenas do pacote de domínio para executar a lógica de negócios. use_cases não deve ter nenhuma dependência de infraestrutura (incluindo framework ou módulo npm).

### infrastructure
infraestrutura contém todos os detalhes técnicos, configuração, implementações (banco de dados, serviços web, módulo npm, etc.), e não deve conter nenhuma lógica de negócio. infraestrutura tem dependências de domínio, use_cases e frameworks.