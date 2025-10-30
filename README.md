# 🚀 DESAFIO-QA-BEEDOO-2025
## Desafio Técnico QA Júnior - Beedo

## 1. 🐞 Relatório de Bugs e Metodologia

### 1.1. Metodologia de Relato de Defeitos e Justificativa
* **Metodologia Utilizada:** **Relatório de Defeitos Padrão (Standard Bug Report)**, com foco na Estrutura de Comunicação: **Título, Severidade, Passos para Reprodução, Resultado Esperado e Resultado Atual.**
* **Justificativa da Escolha:**
    > Esta metodologia foi escolhida para aproveitar a prática que tenho ao usar ferramentas de gestão de testes (como JIRA e ClickUP). A estrutura detalhada garante que o bug seja **rastreável**, **reproduzível** e **priorizável**, elementos cruciais para a comunicação eficaz entre o QA e o time de Desenvolvimento.

### 1.2. Documentação de Casos de Teste e Relatório de Defeitos

A documentação do ciclo de testes foi organizada em um único documento Google Sheets, contendo duas abas essenciais para a rastreabilidade e gestão da qualidade:

* **Suíte de Casos de Teste:** Onde se encontra o planejamento completo, incluindo Cenários Positivos, Negativos e de Borda (Pass/Fail).
* **Relatório de Defeitos Priorizados:** O detalhamento dos bugs críticos encontrados (Severidade, Prioridade, Passos para Reprodução e Evidência).

O documento completo está acessível através do link abaixo:

[🔗 **ACESSAR DOCUMENTAÇÃO COMPLETA NO GOOGLE SHEETS**](https://docs.google.com/spreadsheets/d/1IBjWRWlh--4BsjkBT9HBMleoYSRXz-yNvevOVdG_7vA/edit?gid=4121115#gid=4121115)

---

## 2. 📝 User Story (História do Usuário)

**COMO** um Administrador da plataforma,
**EU QUERO** poder cadastrar um novo curso, definindo o nome, as datas e o limite de vagas,
**PARA QUE** os alunos possam se inscrever e eu possa gerenciar a oferta de conteúdo de forma eficaz.

### 2.1. Critérios de Aceitação (Formato Gherkin)

A funcionalidade de cadastro de cursos deve seguir os seguintes critérios para ser considerada aceita:

#### Cenário 1: Cadastro de Curso com Sucesso (Happy Path)
**Dado que** o Administrador está na tela de cadastro de curso,
**E** preencheu todos os campos obrigatórios (Nome, Datas, Vagas) com dados válidos,
**Quando** clica no botão "Criar Curso",
**Então** o curso deve ser registrado com sucesso no sistema,
**E** uma mensagem de confirmação de sucesso deve ser exibida.

---

#### Cenário 2: Preenchimento de Campo Obrigatório (Evita BUG-001)
**Dado que** o Administrador está na tela de cadastro de curso,
**E** o campo "Nome do Curso" está **vazio**,
**Quando** clica no botão "Criar Curso",
**Então** o curso **NÃO** deve ser registrado,
**E** uma mensagem de erro indicando que o campo é obrigatório deve ser exibida.

---

#### Cenário 3: Validação da Regra de Negócio (Evita BUG-002)
**Dado que** o Administrador está na tela de cadastro de curso,
**E** preencheu o campo "Vagas" com um valor **negativo** (ex: -1),
**Quando** clica no botão "Criar Curso",
**Então** o curso **NÃO** deve ser registrado,
**E** uma mensagem de erro informando que o número de vagas deve ser **positivo** deve ser exibida.

---

## 3. 🖼️ Evidências e Observações

### Evidências dos Bugs
Todas as *screenshots* que comprovam os bugs reportados estão organizadas no Google Drive para fácil acesso:

[🔗 **ACESSAR PASTA DE EVIDÊNCIAS NO GOOGLE DRIVE**](https://drive.google.com/drive/folders/1xplliF_CiLDB2SZncfKxID5OAIbv-Y3z?usp=sharing)
