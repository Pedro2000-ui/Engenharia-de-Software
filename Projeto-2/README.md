# 🏥 Sistema de Consultas Médicas – Especificação de Requisitos

Este documento apresenta a especificação dos requisitos funcionais e não funcionais para o desenvolvimento de um sistema voltado à gestão de consultas médicas. O objetivo é garantir clareza e alinhamento entre as partes interessadas, além de estabelecer critérios sólidos para implementação e validação do sistema.

---

## 📌 Sumário

- [1. Introdução](#1-introdução)
- [2. Requisitos Funcionais](#2-requisitos-funcionais)
- [3. Requisitos Não Funcionais](#3-requisitos-não-funcionais)

---

## 1. Introdução

O sistema de consultas médicas tem como propósito facilitar o agendamento, controle e histórico de atendimentos entre pacientes e profissionais da saúde. O sistema será utilizado por três perfis principais: pacientes, médicos e administradores, cada um com permissões e funcionalidades específicas.

---

## 2. Requisitos Funcionais

### RF-MED-001 – Agendamento de Consulta
- **Descrição**: Permite que o paciente visualize a disponibilidade dos médicos e agende uma consulta em um horário livre.
- **Extensões**: Cancelamento e reagendamento de consultas.
- **Critérios de Aceitação**:
  - Apenas horários livres devem ser exibidos.
  - Confirmação automática via e-mail após agendamento.
- **Dependências**: Cadastro prévio de paciente e médico.
- **Fonte**: Paciente/Secretária da clínica.
- **Prioridade**: Alta

---

### RF-MED-002 – Cadastro de Pacientes
- **Descrição**: Permite o registro de pacientes no sistema com dados pessoais e informações de contato.
- **Extensões**: Atualização de dados cadastrais/Inativação de Pacientes.
- **Critérios de Aceitação**:
  - Validação de CPF e e-mail únicos.
  - Preenchimento obrigatório de campos essenciais.
- **Dependências**: Cadastro prévio de Secretárias.
- **Fonte**: Secretária da clínica.
- **Prioridade**: Alta

---

### RF-MED-003 – Cadastro de Médicos
- **Descrição**: Permite o cadastro de médicos com suas especialidades, registro profissional (CRM) e agenda de atendimento.
- **Extensões**: Alteração de especialidade ou horários disponíveis/Inativação de Médicos.
- **Critérios de Aceitação**:
  - CRM deve ser válido e não duplicado.
- **Dependências**: Cadastro prévio de Gerentes adm da clínica.
- **Fonte**: Gerente administrativo da clínica.
- **Prioridade**: Alta

---

### RF-MED-004 – Histórico de Consultas
- **Descrição**: Permite a visualização do histórico de consultas tanto por médicos quanto por pacientes.
- **Extensões**: Exportação do histórico em formato PDF.
- **Critérios de Aceitação**:
  - As consultas devem ser exibidas em ordem cronológica.
- **Dependências**: Existência de consultas registradas.
- **Fonte**: Médico responsável.
- **Prioridade**: Média

## 3. Requisitos Não Funcionais

### NF-MED-001 – Tempo de Resposta
- **Descrição**: O sistema deve garantir que 95% das requisições de usuários sejam respondidas em até 3 segundos.
- **Entrada**: Ações como login, cadastro e agendamento.
- **Processamento**: Interações com banco de dados e serviços de autenticação.
- **Saída**: Retorno de páginas ou mensagens.
- **Restrições**: A métrica considera conexões estáveis.
- **Critérios de Aceitação**: Resultados validados por testes de desempenho.

---

### NF-MED-002 – Segurança da Informação
- **Descrição**: O sistema deve garantir a integridade e confidencialidade das informações por meio de autenticação, controle de acesso e criptografia de dados sensíveis.
- **Entrada**: Dados pessoais, médicos e de saúde dos usuários.
- **Processamento**: Armazenamento seguro e políticas de permissão.
- **Saída**: Visualização e manipulação restrita a perfis autorizados.
- **Restrições**: Deve seguir diretrizes de segurança da informação e proteção de dados.
- **Critérios de Aceitação**: Dados não acessíveis por perfis não autorizados.

---

### NF-MED-003 – Compatibilidade entre Navegadores
- **Descrição**: A aplicação deve funcionar de forma consistente nos principais navegadores web.
- **Entrada**: Acesso via navegadores como Chrome, Firefox, Safari e Edge.
- **Processamento**: Carregamento e renderização da interface.
- **Saída**: Interface plenamente funcional.
- **Restrições**: Compatibilidade com versões recentes dos navegadores.
- **Critérios de Aceitação**: Interface responsiva, sem quebras ou falhas.

---

### NF-MED-004 – Responsividade
- **Descrição**: O sistema deve se adaptar adequadamente a diferentes resoluções de tela, proporcionando boa experiência em desktop, tablets e smartphones.
- **Entrada**: Acesso por diferentes dispositivos.
- **Processamento**: Aplicação de estilos e layout responsivo.
- **Saída**: Interface ajustada conforme o tamanho da tela.
- **Restrições**: Design mínimo para resoluções de 320px.
- **Critérios de Aceitação**: Usabilidade comprovada em dispositivos móveis.

---