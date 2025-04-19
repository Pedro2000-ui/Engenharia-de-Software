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

---

### RF-MED-005 – Login e Autenticação de Usuários
- **Descrição**: Permite que pacientes, médicos e administradores acessem o sistema por meio de login com autenticação segura.
- **Extensões**: Recuperação de senha e autenticação por dois fatores.
- **Critérios de Aceitação**:
  - Login com e-mail e senha válidos.
  - Redirecionamento para o painel correspondente ao perfil.
- **Dependências**: Cadastro de usuário.
- **Fonte**: Equipe de TI da clínica.
- **Prioridade**: Alta

---

### RF-MED-006 – Painel Administrativo
- **Descrição**: Permite ao administrador visualizar estatísticas, gerenciar usuários, médicos e agendamentos.
- **Extensões**: Geração de relatórios.
- **Critérios de Aceitação**:
  - Acesso restrito ao perfil de administrador.
  - Exibição de dados em gráficos e tabelas.
- **Dependências**: Dados registrados no sistema.
- **Fonte**: Gerente administrativo.
- **Prioridade**: Alta

---

### RF-MED-007 – Notificações de Consulta
- **Descrição**: Envia lembretes automáticos de consultas próximas aos pacientes e médicos.
- **Extensões**: Notificações via SMS ou WhatsApp.
- **Critérios de Aceitação**:
  - Envio de e-mail 24 horas antes da consulta.
- **Dependências**: Consulta agendada.
- **Fonte**: Secretária da clínica.
- **Prioridade**: Média

---

### RF-MED-008 – Registro de Prontuário Médico
- **Descrição**: Permite ao médico registrar anotações clínicas, prescrições e observações relacionadas à consulta.
- **Extensões**: Anexar arquivos (exames, receitas, etc.).
- **Critérios de Aceitação**:
  - Prontuário associado a uma consulta específica.
  - Acesso restrito ao médico responsável.
- **Dependências**: Consulta realizada.
- **Fonte**: Médico da clínica.
- **Prioridade**: Alta

---

### RF-MED-009 – Avaliação do Atendimento
- **Descrição**: Permite que o paciente avalie o atendimento médico após a consulta.
- **Extensões**: Comentários opcionais.
- **Critérios de Aceitação**:
  - Nota de 1 a 5 com possibilidade de feedback textual.
- **Dependências**: Consulta finalizada.
- **Fonte**: Paciente.
- **Prioridade**: Baixa

---

### RF-MED-010 – Visualização de Agenda por Especialidade
- **Descrição**: Permite a filtragem da agenda de médicos por especialidade para facilitar o agendamento.
- **Extensões**: Filtros adicionais (local, data, horário).
- **Critérios de Aceitação**:
  - Exibição de todos os médicos disponíveis da especialidade selecionada.
- **Dependências**: Cadastro de especialidades e médicos.
- **Fonte**: Secretária da clínica.
- **Prioridade**: Média

---

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

### NF-MED-005 – Escalabilidade
- **Descrição**: O sistema deve ser capaz de suportar aumento no número de usuários simultâneos sem perda significativa de desempenho.
- **Entrada**: Crescimento no volume de acessos.
- **Processamento**: Requisições simultâneas.
- **Saída**: Respostas dentro do tempo aceitável.
- **Restrições**: Arquitetura escalável (ex: cloud computing).
- **Critérios de Aceitação**: Testes com simulação de carga.
- **Fonte**: Equipe de infraestrutura.

---

### NF-MED-006 – Backup Diário
- **Descrição**: O sistema deve realizar backups automáticos diários dos dados, armazenados com segurança.
- **Entrada**: Base de dados do sistema.
- **Processamento**: Geração do backup e envio a local seguro.
- **Saída**: Arquivo de backup completo e recuperável.
- **Restrições**: Armazenamento criptografado, preferencialmente em nuvem.
- **Critérios de Aceitação**: Log de backup e teste de restauração mensal.
- **Fonte**: Administrador do sistema.

---

### NF-MED-007 – Usabilidade
- **Descrição**: A interface deve ser intuitiva para facilitar o uso, mesmo por usuários com pouca familiaridade com tecnologia.
- **Entrada**: Interações básicas como cadastro, agendamento e login.
- **Processamento**: Navegação fluida com feedback visual.
- **Saída**: Execução da tarefa com facilidade.
- **Restrições**: Design simplificado, sem sobrecarga cognitiva.
- **Critérios de Aceitação**: Sucesso ≥ 85% nos testes com usuários reais.
- **Fonte**: Pacientes idosos e secretárias da clínica.

---

### NF-MED-008 – Acessibilidade
- **Descrição**: O sistema deve seguir diretrizes de acessibilidade (WCAG 2.1), permitindo uso por pessoas com deficiência.
- **Entrada**: Navegação com teclado, leitores de tela.
- **Processamento**: Interface sem barreiras de navegação.
- **Saída**: Acesso completo ao conteúdo e funcionalidades.
- **Restrições**: Compatibilidade com tecnologias assistivas.
- **Critérios de Aceitação**: Validação por ferramentas e usuários reais.
- **Fonte**: Representante de acessibilidade da clínica.

---

### NF-MED-009 – Modularidade
- **Descrição**: O sistema deve ser desenvolvido de forma modular, facilitando manutenção e expansão.
- **Entrada**: Novos requisitos ou correções.
- **Processamento**: Alterações localizadas por módulo.
- **Saída**: Sistema adaptado com baixo impacto em outras partes.
- **Restrições**: Arquitetura em camadas ou microserviços.
- **Critérios de Aceitação**: Novos módulos implementados sem quebra dos existentes.
- **Fonte**: Equipe de desenvolvimento.

---

### NF-MED-010 – Atualizações Automatizadas
- **Descrição**: O sistema deve permitir atualizações automáticas sem necessidade de reinstalação manual.
- **Entrada**: Nova versão disponível.
- **Processamento**: Verificação, download e aplicação da atualização.
- **Saída**: Sistema atualizado com sucesso.
- **Restrições**: Conectividade ativa e permissões corretas.
- **Critérios de Aceitação**: Atualizações sem perda de dados e sem erros críticos.
- **Fonte**: Equipe de DevOps.

---