# Governança, Organizações e Permissões no GitHub - DIO

Repositório desenvolvido como desafio prático da formação **GitHub Certification** na Digital Innovation One (DIO), consolidando os conceitos de administração de organizações, estruturação hierárquica de equipes e controle de acesso a repositórios.

---

## 🎯 Objetivo do Projeto

Demonstrar na prática como estruturar uma organização no GitHub de forma segura e escalável, aplicando o princípio do privilégio mínimo (*Least Privilege*) através de papéis organizacionais, equipes aninhadas (*Nested Teams*) e níveis granulares de permissão.

---

## 🏢 Papéis em uma Organização no GitHub

| Papel | Responsabilidades Principais |
| :--- | :--- |
| **Owner (Proprietário)** | Controle administrativo total da organização: gerencia faturamento, cria/remove repositórios e equipes, e define políticas globais de segurança. |
| **Member (Membro)** | Papel padrão para colaboradores da organização; pode criar repositórios (se permitido) e visualizar membros e equipes visíveis. |
| **Billing Manager** | Gerencia exclusivamente configurações financeiras, faturas e métodos de pagamento, sem acesso ao código-fonte. |
| **Security Manager** | Gerencia alertas de segurança e configurações de proteção em todos os repositórios da organização. |
| **Outside Collaborator** | Usuário externo (ex.: consultor ou prestador de serviço) com acesso restrito apenas a repositórios específicos, sem ser membro da organização. |

---

## 👥 Estrutura Hierárquica de Equipes (*Nested Teams*)

A criação hierárquica permite espelhar o organograma da empresa e herdar permissões automaticamente das equipes pai para as equipes filhas:

```text
Organização (Ex: TechCorp-Org)
└── Engenharia (Equipe Pai - Acesso de leitura aos repositórios base)
    ├── Backend-Team (Equipe Filha - Permissão Write nos microsserviços)
    ├── Frontend-Team (Equipe Filha - Permissão Write nas aplicações web)
    └── DevOps-SRE (Equipe Filha - Permissão Maintain/Admin na infraestrutura)
