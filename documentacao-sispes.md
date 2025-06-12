# Documentação Técnica — SISPES

Sistema Integrado de Planejamento de Dimensionamento de Pessoal


## 1. Introdução

O sistema SISPES tem como finalidade apoiar o planejamento da alocação de profissionais nas unidades do Ministério da Saúde. Ele será um sistema online, acessível por diferentes secretarias, permitindo o preenchimento padronizado, a consolidação e a análise de dados de dimensionamento de pessoal.


## 2. Arquitetura Geral

O sistema será desenvolvido em uma arquitetura web moderna, baseada em microsserviços. Abaixo estão descritos os principais componentes:

### 2.1 Visão Geral da Arquitetura

- **Frontend**: Aplicação web responsiva desenvolvida em React.
- **Backend**: API RESTful utilizando Node.js com Express.
- **Banco de Dados**: PostgreSQL.
- **Serviços de Integração**: Comunicação com o sistema E-ORG.
- **Autenticação**: JWT (JSON Web Token).
- **Infraestrutura**: Hospedagem na AWS, com containers Docker.

### 2.2 Componentes Principais

- **Formulário de Dimensionamento**: campos dinâmicos e configuráveis.
- **Módulo de Relatórios**: geração de relatórios em tempo real.
- **Gerenciador de Usuários**: controle de permissões e segurança.
- **Módulo de Importação/Exportação**: integração com planilhas e sistemas externos.


## Tecnologias Envolvidas

| Camada           | Tecnologia           |
|------------------|----------------------|
| Frontend         | React.js             |
| Backend          | Node.js + Express    |
| Banco de Dados   | PostgreSQL           |
| Integração       | API REST + E-ORG     |
| Segurança        | JWT + HTTPS          |
| Infraestrutura   | Docker + AWS         |


## Observações

- Upload limitado a 5MB por arquivo.
- Envio de e-mails para notificações automáticas.
- Interface compatível com dispositivos móveis.
- Sistema disponível 24/7, com backup diário.
