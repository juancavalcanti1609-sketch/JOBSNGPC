# 📊 SNGPC MS Automation

![SQL Server](https://img.shields.io/badge/SQL%20Server-T--SQL-blue)
![Status](https://img.shields.io/badge/status-production-brightgreen)
![Automation](https://img.shields.io/badge/process-automated-success)
![Data Quality](https://img.shields.io/badge/data-quality%20driven-blueviolet)

---

--> Sobre o Projeto

Automação desenvolvida em **T-SQL (SQL Server)** para validação e atualização de registros do Ministério da Saúde (MS) em produtos farmacêuticos.

O projeto foi criado para atender exigências do **SNGPC (Sistema Nacional de Gerenciamento de Produtos Controlados)**, eliminando processos manuais e reduzindo riscos operacionais.

---

--> Problema

O SNGPC exige que os registros de medicamentos estejam sempre atualizados.

Desafios encontrados:

- Atualizações frequentes nos registros (ANVISA/MS)
- Alto volume de produtos
- Processo manual sujeito a erros
- Risco regulatório

---

--> Solução

A automação realiza:

- 🔍 Consulta e validação de dados
- 🔗 Integração entre múltiplas bases via Linked Servers
- 🔄 Comparação entre registros internos e ANVISA
- ✏️ Atualização automática de divergências
- 🛡️ Regras de validação para garantir integridade

---

--> Regras de Negócio

A atualização só ocorre quando:

- Registro ANVISA ≠ Registro interno
- Produto é de venda controlada
- Registro ANVISA:
  - Possui 13 dígitos
  - Contém apenas números
  - Não é `0000000000000`
  - Não é igual ao EAN

---

--> Execução

A solução é executada como uma **JOB no SQL Server**, sendo acionada conforme necessidade de validação e atualização.

---

--> Benefícios

- ⏱️ Redução significativa de tempo operacional  
- 🎯 Maior confiabilidade nos dados  
- 🔄 Processo automatizado  
- ⚖️ Redução de riscos regulatórios
