# Azure-git-version
Este projeto integra o Azure Data Factory com o GitHub para versionamento de artefatos como pipelines, datasets e linked services. A estrutura permite controle de mudanças, auditoria e padronização dos ambientes de dados. Toda edição é rastreada no repositório GitHub, garantindo governança no ciclo de desenvolvimento e facilitando a futura implementação de CI/CD com GitHub Actions.

# 🌐 Azure Data Factory com GitHub – Versionamento de Pipelines

Este projeto demonstra como integrar o **Azure Data Factory (ADF)** ao **GitHub** para versionamento de pipelines, controle de mudanças e governança de dados.

---


## ✅ Objetivos

- Integrar o ADF com GitHub como repositório Git
- Criar e versionar pipelines com rastreabilidade
- Preparar o ambiente para práticas de CI/CD futuras

---

## 🔧 Configuração do GitHub no Azure Data Factory

1. Acesse o recurso do **Azure Data Factory** no portal Azure
2. Vá em **Manage** (ícone de engrenagem no canto inferior esquerdo)
3. Selecione **Git Configuration**
4. Clique em **Configure Git**
5. Preencha os campos:
   - **Repository Type**: GitHub
   - Faça login na sua conta GitHub
   - Escolha o **repositório** e o **branch de colaboração** (ex: `dev`)
   - Defina o **Root Folder** (ex: `/adf`)
   - Marque a opção: `Import existing Data Factory resources to repository`
6. Clique em **Apply**

🖼️ *Exemplo de tela de configuração do Git:*

![Configuração Git no ADF](https://github.com/Rodrigo-Antonio-Silva/Azure-git-version/blob/57bb45ac8d97df14480741ef1103ee26892c3984/Captura%20de%20tela%202025-05-24%20131940.png)

---

## 🚀 Criando um Pipeline com GitHub conectado

### Exemplo: Pipeline de cópia de dados do Azure Blob para Azure SQL Database

1. No menu lateral, clique em **Author**
2. Clique em **+ > Pipeline**
3. Renomeie o pipeline para: `Pipeline_CopiaBlobParaSQL`
4. No painel de atividades, arraste **Copy Data** para o canvas
5. Clique na atividade e configure:
   - **Source**: crie um dataset apontando para o arquivo no Azure Blob Storage
   - **Sink**: crie um dataset apontando para a tabela no Azure SQL Database

🖼️ *Exemplo da atividade Copy Data:*

![Copy Data](https://github.com/Rodrigo-Antonio-Silva/Azure-git-version/blob/3368a2509c1e91f97334339e27a82fc8125bb839/Captura%20de%20tela%202025-05-24%20132319.png)

---


## 🛠️ Publicação no ADF (Publish)

Após salvar os pipelines no GitHub, clique em **Publish** no ADF para aplicar as alterações no ambiente ativo.

🖼️ *Botão Publish no ADF:*

![Botão Publish](https://github.com/Rodrigo-Antonio-Silva/Azure-git-version/blob/dcc1dbe482e6f6ee914bc8a3c0cf5f97dc3dd985/Captura%20de%20tela%202025-05-24%20132904.png)

---

## 📌 Requisitos

- Azure Subscription
- Repositório no GitHub
- Azure Data Factory provisionado
- Linked Services criados (Blob Storage, My SQL etc.)

---

## 📬 Contato

Para dúvidas ou sugestões, entre em contato com [rodrigo2013.rs33@gmail.com].

