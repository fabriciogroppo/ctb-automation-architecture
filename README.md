# ctb-automation-architecture
CTB Automation, responsável por processos de ETL, integrações via SFTP e automação de transferência de arquivos.
Descrição do Sistema

O sistema possui os seguintes componentes principais:

Scheduler responsável pelas execuções agendadas.
Serviço ETL para extração, transformação e carga de dados.
Serviço de Sincronização de Arquivos.
API Cisco para obtenção de dados.
Servidor SFTP para troca de arquivos.
Banco de dados SQL Server.
Serviço de Notificação por E-mail.
Camada de Logging e Observabilidade.
Diagrama Estrutural (Mermaid)
<img width="4032" height="2107" alt="image" src="https://github.com/user-attachments/assets/f30d664d-f26d-42ce-bc45-e08549ea569d" />

Diagrama Comportamental (Sequência)
<img width="4032" height="1959" alt="image" src="https://github.com/user-attachments/assets/5106dbe1-7225-46f8-aeb4-c699fe690ab4" />

O que o modelo inferiu corretamente

A IA conseguiu identificar corretamente:

A separação entre processamento ETL e sincronização de arquivos.
A necessidade de tratar API e SFTP como integrações externas.
A importância de observabilidade e notificações.
O papel do agendamento automatizado no fluxo.
O que precisei ajustar

Algumas inferências precisaram de correção:

O modelo inicialmente assumiu microsserviços independentes, quando a solução atual é modular.
Foi necessário explicitar que os serviços compartilham componentes comuns de logging e configuração.
A IA também sugeriu múltiplos bancos de dados, quando o cenário real utiliza um SQL Server centralizado.
O que faltaria para um agente implementar o sistema sem inventar decisões

Para permitir que um agente de desenvolvimento implementasse a solução com maior precisão, eu adicionaria:

ADRs documentando decisões arquiteturais.
Requisitos não funcionais verificáveis.
Contratos das APIs externas.
Estrutura de diretórios do projeto.
Fluxos de tratamento de erro.
Estratégias de retry e timeout.
Regras de observabilidade.
Diagramas de componentes internos.
Glossário de domínio.
Modelo de dados e dicionário de tabelas.

Essas informações reduziriam as lacunas de contexto e diminuiriam a probabilidade de o agente criar implementações baseadas em suposições não validadas.
