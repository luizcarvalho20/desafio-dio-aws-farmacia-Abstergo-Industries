# 🧩 Arquitetura Proposta – Farmácia Virtual Abstergo Industries

Este documento descreve a **arquitetura conceitual** proposta para a farmácia virtual da **Abstergo Industries**, utilizando serviços da **Amazon Web Services (AWS)** com foco em **redução de custos**, **simplicidade operacional** e **escalabilidade**.

---

## 🏗️ Visão Geral da Arquitetura

A arquitetura proposta é baseada em três pilares principais:

- Armazenamento em nuvem de baixo custo
- Gerenciamento eficiente de dados
- Processamento sob demanda sem servidores fixos

Os serviços utilizados são:
- Amazon S3
- Amazon RDS
- AWS Lambda

---

## 🗂️ Componentes da Arquitetura

### 🔹 Amazon S3 – Armazenamento de Arquivos

O Amazon S3 é responsável pelo armazenamento de arquivos estáticos e documentos utilizados pela farmácia virtual, tais como:

- Imagens de produtos
- Notas fiscais
- Relatórios administrativos
- Documentos internos

**Benefícios arquiteturais:**
- Alta durabilidade dos dados
- Escalabilidade automática
- Baixo custo de armazenamento
- Eliminação de servidores locais

---

### 🔹 Amazon RDS – Banco de Dados Relacional

O Amazon RDS é utilizado como banco de dados principal da aplicação, armazenando informações críticas do negócio, como:

- Cadastro de clientes
- Produtos disponíveis
- Pedidos realizados
- Informações de pagamento

**Benefícios arquiteturais:**
- Backups automáticos
- Alta disponibilidade
- Menor esforço de manutenção
- Redução de falhas operacionais

---

### 🔹 AWS Lambda – Processamento Serverless

O AWS Lambda é responsável por executar funções específicas da aplicação de forma automatizada, sendo acionado apenas quando necessário.

**Exemplos de uso:**
- Envio de e-mails de confirmação de pedidos
- Atualização automática de estoque
- Geração de relatórios simples

**Benefícios arquiteturais:**
- Ausência de servidores dedicados
- Cobrança apenas por execução
- Escalabilidade automática
- Redução de custos com infraestrutura ociosa

---

## 🔄 Fluxo Simplificado da Arquitetura

1. O usuário acessa a farmácia virtual
2. Dados de produtos e pedidos são armazenados no Amazon RDS
3. Arquivos e imagens são armazenados no Amazon S3
4. Eventos específicos acionam funções no AWS Lambda
5. As funções executam tarefas pontuais sem manter servidores ativos

---

## 💰 Impacto na Redução de Custos

A arquitetura proposta contribui diretamente para a redução de custos ao:

- Eliminar servidores físicos e infraestrutura própria
- Utilizar pagamento sob demanda
- Reduzir necessidade de equipe dedicada para manutenção
- Evitar custos com recursos ociosos

---

## 📌 Considerações Finais

Esta arquitetura foi projetada para atender às necessidades de uma farmácia virtual de médio porte, priorizando simplicidade, eficiência e controle de custos. A utilização de serviços gerenciados da AWS permite que a empresa foque no negócio, deixando a complexidade da infraestrutura sob responsabilidade da nuvem.

