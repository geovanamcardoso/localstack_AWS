# Hands-on AWS Local com LocalStack

Repositório criado como parte do **Módulo 11: Automação e DevOps na AWS - Executando Tarefas Automatizadas com Lambda Function e S3** do **Bootcamp Santander Code Girls + DIO**.

Este projeto documenta a prática de criar e testar **S3, Lambda, DynamoDB e API Gateway** localmente, incluindo scripts, templates de configuração e prints do console mostrando o fluxo completo de upload -> processamento -> armazenamento -> API.

---

## Conceitos Principais

**LocalStack** é uma ferramenta que simula serviços AWS localmente, permitindo testar aplicações sem custo.  
Com ele podemos criar e validar recursos como **S3, DynamoDB, Lambda e API Gateway** antes de executar na AWS real.

Vantagens:
- Testes e desenvolvimento sem custo de nuvem;  
- Simulação realista de serviços AWS;  
- Integração com scripts CLI e linguagens como Python;  
- Permite validar triggers, funções e APIs sem precisar de AWS real.

Principais termos:
- **LocalStack:** ambiente AWS simulado localmente.  
- **Lambda:** função serverless para processar eventos.  
- **S3:** armazenamento de arquivos/buckets.  
- **DynamoDB:** banco NoSQL simulado localmente.  
- **API Gateway:** expõe funções Lambda como endpoints HTTP.  

Outros pontos importantes:
- Permite aprender a integrar serviços AWS de forma prática.  
- Pode ser usado via Docker ou CLI do LocalStack.  
- Ideal para desenvolvimento e testes antes de produção.

---

## Fluxo do Hands-on

1. Instalação e validação do LocalStack  
2. Configuração do AWS CLI local com credenciais fictícias  
3. Criação dos recursos:
   - Bucket S3  
   - Tabela DynamoDB  
   - Função Lambda  
4. Integração S3 -> Lambda (gatilho e permissões)  
5. Teste de upload no S3 (Lambda processa e grava no DynamoDB)  
6. Criação da API Gateway e integração com Lambda  
7. Testes POST e GET da API local  

---

## Resumo do fluxo Técnico
Upload de arquivo no S3 -> Lambda acionada -> Registro no DynamoDB -> API Gateway expõe dados via HTTP

1. Arquivo JSON enviado para bucket S3
2. Lambda processa o arquivo e grava registros no DynamoDB
3. API Gateway local expõe endpoints POST/GET para envio e consulta de dados
4. Possibilidade de expandir fluxo com triggers adicionais ou integração com outros serviços

--- 

## Boas práticas
- Validar comandos e endpoints antes de testes
- Versionar scripts e arquivos de configuração em Git
- Documentar cada etapa do hands-on
- Testar triggers e permissões localmente antes de migrar para AWS real
- Manter backups e logs de execução de funções Lambda

--- 

## Créditos

**Autora:** Geovana Maria da Silva Cardoso  
**Bootcamp:** DIO  
**Módulo**: Automação e DevOps na AWS
