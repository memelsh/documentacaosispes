# Documento de Arquitetura — Projeto SISPES

---

## 1. Introdução

Este documento descreve a arquitetura do sistema **SISPES – Sistema Integrado de Planejamento de Dimensionamento de Pessoal**, que visa permitir a coleta, consolidação e análise de dados sobre a necessidade de profissionais nas unidades do Ministério da Saúde.

---

## 2. Visão Geral da Arquitetura

O sistema foi projetado utilizando a arquitetura baseada em **camadas e microsserviços**, para garantir escalabilidade, manutenibilidade e integração com sistemas externos.

### Diagrama Lógico (Representação Textual)

Usuário → [Frontend Web React]
↓ API REST
[Backend Node.js + Express]
↓
[Banco de Dados PostgreSQL]
↓
Integração com E-ORG


*(Se quiser, pode depois criar um diagrama visual no Draw.io ou Lucidchart e anexar ao repositório)*

---

## 3. Componentes do Sistema

- **Frontend (React.js)**  
  Interface web responsiva, acessada pelos usuários autenticados.

- **Backend (Node.js + Express)**  
  API RESTful responsável pela lógica de negócio e validação de dados.

- **Banco de Dados (PostgreSQL)**  
  Armazena as informações de usuários, formulários preenchidos, parâmetros e relatórios.

- **Módulo de Importação/Exportação**  
  Permite integração com planilhas externas e com o sistema E-ORG.

- **Sistema de Autenticação**  
  Controle de acesso com base em permissões de perfil (JWT).

---

## 4. Tecnologias Utilizadas

| Camada        | Tecnologia           |
|---------------|----------------------|
| Frontend      | React.js             |
| Backend       | Node.js + Express    |
| Banco de Dados| PostgreSQL           |
| Autenticação  | JWT                  |
| Integração    | REST API + E-ORG     |
| Infraestrutura| Docker + AWS         |

---

## 5. Decisões Arquiteturais

- Utilizar **React** para garantir uma experiência fluida no navegador.
- Usar **Node.js** pela compatibilidade com JSON e escalabilidade em APIs.
- Adotar **PostgreSQL** por confiabilidade e estrutura relacional.
- Implementar **JWT** por ser leve, seguro e amplamente suportado.
- Contêineres Docker para facilitar deploy e portabilidade.
- Integração com **E-ORG** por meio de API padronizada.

---

## 6. Qualidades Arquiteturais

| Qualidade             | Implementação                                                   |
|-----------------------|-----------------------------------------------------------------|
| **Desempenho**        | Requisições assíncronas via API, uso de cache no frontend       |
| **Segurança**         | Login com senha, controle por perfis, autenticação JWT          |
| **Usabilidade**       | Interface clara, compatível com celulares e tablets             |
| **Disponibilidade**   | Implantação em nuvem (AWS), backups automáticos                 |
| **Manutenibilidade**  | Separação em módulos independentes, uso de boas práticas        |

---
