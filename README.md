# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 22 de janeiro de 2026

**Empresa:** Abstergo Industries

**Responsável:** Pedro de Oliveira Pinto

---

## 1. Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Pedro**. O objetivo primordial do projeto foi selecionar e configurar 3 serviços da AWS com foco estratégico na **diminuição de custos imediatos** e otimização da infraestrutura em nuvem.

## 2. Descrição do Projeto

O projeto foi executado em três etapas distintas, focando em armazenamento, banco de dados e computação.

### Etapa 1: Centralização de Registros e Documentação Fiscal

* **Ferramenta:** Amazon S3 (Simple Storage Service) com S3 Intelligent-Tiering.
* **Foco:** Eliminação de custos com servidores de arquivos físicos e manutenção de hardware local.
* **Descrição de Caso de Uso:** Migração de todos os registros de distribuição, laudos técnicos de medicamentos e notas fiscais de entrada/saída para buckets do S3. Ao utilizar o Intelligent-Tiering, o sistema move automaticamente documentos antigos (que precisam ser guardados por questões regulatórias, mas raramente acessados) para camadas de custo ínfimo, reduzindo drasticamente o gasto com armazenamento em comparação ao armazenamento físico ou servidores locais.

### Etapa 2: Automação da Comunicação B2B com Parceiros

* **Ferramenta:** AWS Lambda (Arquitetura Serverless).
* **Foco:** Redução de custos operacionais com servidores ligados 24/7.
* **Descrição de Caso de Uso:** Implementação de funções serverless para gerenciar a troca de dados entre o hub da Abstergo e as empresas farmacêuticas parceiras. Em vez de manter um servidor ligado o dia inteiro apenas para processar pedidos esporádicos, o Lambda executa o código apenas quando um dado é recebido (via API ou arquivo), cobrando somente pelos milissegundos de processamento. Isso elimina o custo de ociosidade de infraestrutura.

### Etapa 3: Gestão de Inventário e Rastreabilidade de Lotes

* **Ferramenta:** Amazon DynamoDB (On-Demand).
* **Foco:** Banco de dados de alta performance com custo variável baseado em demanda.
* **Descrição de Caso de Uso:** Utilização de uma tabela NoSQL para rastrear o fluxo de medicamentos (lote, validade e destino) em tempo real. O modelo "On-Demand" é ideal para a Abstergo, pois a empresa paga apenas pelas leituras e gravações realizadas durante os horários de pico de distribuição. Isso evita o investimento inicial pesado em licenças de bancos de dados relacionais tradicionais e hardware dedicado, garantindo que o custo acompanhe o crescimento do volume de negócios.

---

## 3. Conclusão

A implementação destas ferramentas na **Abstergo Industries** tem como expectativa uma redução direta nos custos operacionais mensais de nuvem e a eliminação de desperdícios de recursos. O aumento da eficiência técnica permitirá que a equipe foque em inovação em vez de manutenção de infraestrutura ociosa.

Recomenda-se a revisão trimestral das políticas de ciclo de vida e a análise contínua através do AWS Cost Explorer para identificar novas oportunidades de economia.

## 4. Anexos

1. Planilha de Previsão de Gastos (Forecast).
2. Guia de Configuração de Lifecycle do S3.
3. Políticas de IAM para o Instance Scheduler.

---

**Assinatura do Responsável pelo Projeto:**

---

**Pedro de Oliveira Pinto**
