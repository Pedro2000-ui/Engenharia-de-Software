# 1. Visão Geral do Produto

## 1.1 Declaração do Problema e Oportunidade de Negócio

O setor de saúde enfrenta diversos desafios no gerenciamento de consultas médicas. Entre os principais problemas estão:
- **Tempos de espera longos**: Pacientes demoram para conseguir agendar consultas.
- **Falta de integração**: Dificuldades na comunicação entre clínicas, médicos e pacientes.
- **Gestão ineficiente de horários**: A agenda dos médicos e clínicas muitas vezes é mal organizada.
- **Histórico médico descentralizado**: Informações de saúde dos pacientes estão dispersas em diferentes sistemas.

Esses problemas geram:
- **Ineficiência operacional**: Processos manuais consomem tempo e recursos.
- **Insatisfação dos pacientes**: Dificuldades no agendamento e acesso a informações.
- **Perda de competitividade**: Clínicas que não adotam soluções modernas perdem pacientes.

A **oportunidade de negócio** está na criação de uma plataforma digital que:
- **Facilita o agendamento online**: Reduz o tempo de espera e melhora a experiência do paciente.
- **Automatiza processos**: Envio de lembretes e confirmações de consultas.
- **Centraliza o histórico médico**: Acesso rápido e seguro a informações de saúde.
- **Oferece ferramentas de análise**: Relatórios para médicos e clínicas monitorarem desempenho.

Essa solução resolve problemas atuais e abre portas para novas receitas, como parcerias com planos de saúde e integração com telemedicina.

---

## 1.2 Perspectiva do Produto

O produto será uma plataforma digital completa, disponível para **web** e **mobile**, atendendo três grupos principais:

1. **Pacientes**:
   - Agendamento de consultas de forma rápida e intuitiva.
   - Recebimento de lembretes automáticos por e-mail, SMS e WhatsApp.
   - Acesso a um histórico médico digital, incluindo exames e prescrições.
   - Possibilidade de avaliar médicos e clínicas.

2. **Médicos**:
   - Agenda digital para gerenciar consultas de forma eficiente.
   - Acesso a prontuários eletrônicos dos pacientes.
   - Notificações sobre cancelamentos ou reagendamentos.
   - Relatórios de desempenho, como taxa de ocupação e satisfação dos pacientes.

3. **Clínicas e Hospitais**:
   - Gerenciamento de múltiplos médicos e especialidades em uma única plataforma.
   - Ferramentas para otimizar a alocação de recursos, como salas e equipamentos.
   - Integração com sistemas de pagamento (via API) e planos de saúde.
   - Dados analíticos para tomada de decisões estratégicas.

A plataforma será desenvolvida com foco em **escalabilidade**, permitindo a inclusão de novos recursos, como telemedicina e integração com dispositivos vestíveis. (wearable)

---

## 1.3 Suposições e Dependências

Para o sucesso do projeto, foram identificadas as seguintes suposições e dependências:

1. **Suposições**:
   - Usuários (pacientes, médicos e clínicas) terão acesso à internet e dispositivos compatíveis.
   - Médicos e clínicas estarão dispostos a adotar a tecnologia e migrar de processos manuais para digitais.
   - Pacientes estarão familiarizados com o uso de aplicativos e plataformas digitais.
   - Haverá demanda suficiente para justificar o investimento no desenvolvimento e manutenção da plataforma.

2. **Dependências**:
   - Integração com APIs de terceiros para funcionalidades como pagamentos online (PayPal, Stripe, ASAAS, Safrapay) e autenticação (Google, Facebook).
   - Conformidade com regulamentações locais, como a Lei Geral de Proteção de Dados (LGPD) no Brasil. (projeto será inicialmente planejado para atuação no Brasil)
   - Parcerias com planos de saúde e laboratórios para integração de dados e serviços.
   - Infraestrutura de TI confiável, como servidores em nuvem e bancos de dados seguros, além das boas práticas de programação e uso de vpn.

---

## 1.4 Capacidades do Produto

O produto oferecerá as seguintes funcionalidades principais:

1. **Agendamento Online**:
   - Interface intuitiva para agendamento de consultas.
   - Visualização em tempo real da disponibilidade de médicos e clínicas.
   - Opção de agendamento recorrente para consultas de acompanhamento.

2. **Notificações Automáticas**:
   - Lembretes de consultas por e-mail, SMS e WhatsApp.
   - Alertas para reagendamentos ou cancelamentos.

3. **Prontuário Eletrônico**:
   - Armazenamento seguro de histórico médico, incluindo diagnósticos, exames e prescrições.
   - Acesso controlado por médicos e pacientes.

4. **Gestão de Agenda**:
   - Ferramentas para médicos e clínicas gerenciarem horários e recursos.
   - Integração com calendários digitais (Google Calendar).

5. **Relatórios e Métricas**:
   - Dados sobre taxa de ocupação, satisfação do paciente e desempenho médico.
   - Ferramentas para análise de tendências e tomada de decisões.

6. **Integrações**:
   - APIs para pagamentos online e autenticação.
   - Conexão com sistemas de planos de saúde e laboratórios.

7. **Acessibilidade**:
   - Design responsivo para dispositivos móveis e desktops.
   - Conformidade com diretrizes de acessibilidade.

## 2. Descrição dos Stakeholders

Os stakeholders são todas as pessoas, grupos ou organizações que têm interesse no projeto ou que podem ser afetados por ele. No contexto do sistema de agendamento de consultas médicas, os principais stakeholders são:

### Stakeholders Principais

| **Stakeholder**       | **Descrição**                                                                 |
|------------------------|-------------------------------------------------------------------------------|
| **Pacientes**          | Pessoas que utilizam o sistema para agendar consultas e acessar serviços médicos. |
| **Médicos**            | Profissionais de saúde que utilizam a plataforma para gerenciar agendas e prontuários. |
| **Clínicas/Hospitais** | Instituições de saúde que adotam o sistema para melhorar a eficiência operacional. |
| **Desenvolvedores**    | Equipe responsável pela criação, manutenção e atualização do sistema.          |
| **Governo**            | Órgãos reguladores que definem normas e leis para sistemas de saúde digitais.  |

---

### Detalhamento dos Stakeholders

| **Stakeholder**       | **Tipo**          | **Interesse**                                                                 | **Poder/Influência** | **Requisitos/Expectativas**                          | **Estratégia de Engajamento**                          |
|------------------------|-------------------|-------------------------------------------------------------------------------|-----------------------|-------------------------------------------------------|--------------------------------------------------------|
| **Pacientes**          | Usuário final     | Facilidade no agendamento, acesso a histórico médico e lembretes de consultas. | Médio                 | Sistema intuitivo, rápido e seguro.                  | Pesquisas de satisfação e feedback contínuo.           |
| **Médicos**            | Usuário final     | Gestão eficiente de agendas e acesso a prontuários eletrônicos.               | Alto                  | Ferramentas de gestão de tempo e integração com outros sistemas. | Treinamentos e suporte técnico personalizado.          |
| **Clínicas/Hospitais** | Organização       | Melhoria na eficiência operacional e redução de custos.                       | Alto                  | Relatórios de desempenho e integração com sistemas existentes. | Reuniões periódicas para alinhamento de expectativas.  |
| **Desenvolvedores**    | Equipe técnica    | Desenvolver um sistema funcional, seguro e escalável.                         | Médio                 | Requisitos claros e feedback constante dos usuários.  | Reuniões de sprint e revisões de requisitos.           |
| **Governo**            | Regulador         | Garantir que o sistema cumpra normas de privacidade e segurança de dados.     | Alto                  | Conformidade com leis como a LGPD.                    | Consultas a especialistas e auditorias periódicas.     |

---

### Explicação dos Stakeholders

1. **Pacientes**:
   - São os principais usuários do sistema. Eles precisam de uma plataforma fácil de usar, que permita agendar consultas rapidamente e acessar informações médicas de forma segura.
   - Suas expectativas incluem notificações automáticas, histórico médico centralizado e uma experiência sem complicações.

2. **Médicos**:
   - Utilizam o sistema para gerenciar suas agendas e acessar prontuários dos pacientes.
   - Precisam de ferramentas que otimizem seu tempo, como integração com calendários e alertas de consultas.

3. **Clínicas/Hospitais**:
   - Buscam melhorar a eficiência operacional e reduzir custos com processos manuais.
   - Esperam relatórios detalhados sobre o desempenho do sistema e dos profissionais.

4. **Desenvolvedores**:
   - Responsáveis por criar e manter o sistema. Precisam de requisitos claros e feedback constante para garantir que o produto atenda às necessidades dos usuários.

5. **Governo**:
   - Define as normas e leis que o sistema deve seguir, como a Lei Geral de Proteção de Dados (LGPD).
   - Sua influência é alta, pois o sistema precisa estar em conformidade com as regulamentações.

---

### Exemplo de Stakeholder Específico

| **Stakeholder**       | **Descrição**                                                                 |
|------------------------|-------------------------------------------------------------------------------|
| **ID Stakeholder**     | 31-001                                                                       |
| **Tipo**               | Diretor de Clínica                                                           |
| **Interesse**          | Redução de custos operacionais e melhoria na experiência do paciente.        |
| **Poder/Influência**   | Alto                                                                         |
| **Requisitos/Expectativas** | Sistema econômico, rápido e com relatórios de desempenho detalhados.       |
| **Estratégia de Engajamento** | Reuniões mensais para apresentação de resultados e ajustes no sistema.   |

---

## 3. Descrição dos Usuários

Os usuários do sistema de agendamento de consultas médicas são divididos em três grupos principais:

### 1. **Pacientes**
- **Quem são**: Pessoas que buscam agendar consultas e acessar serviços médicos.
- **Necessidades**:
  - Agendar consultas de forma rápida e fácil.
  - Receber lembretes sobre consultas marcadas.
  - Acessar histórico médico, como resultados de exames e prescrições.
- **Expectativas**: Uma plataforma simples, segura e que economize tempo.

### 2. **Médicos**
- **Quem são**: Profissionais de saúde que utilizam o sistema para gerenciar suas agendas e prontuários.
- **Necessidades**:
  - Visualizar e gerenciar horários de consultas.
  - Acessar prontuários eletrônicos dos pacientes.
  - Receber alertas sobre cancelamentos ou reagendamentos.
- **Expectativas**: Ferramentas que ajudem a otimizar o tempo e a melhorar o atendimento.

### 3. **Recepcionistas/Administradores de Clínicas**
- **Quem são**: Funcionários responsáveis por administrar agendas, confirmar consultas e gerenciar recursos das clínicas.
- **Necessidades**:
  - Gerenciar agendas de múltiplos médicos.
  - Confirmar consultas e enviar lembretes aos pacientes.
  - Gerar relatórios sobre o desempenho das clínicas.
- **Expectativas**: Um sistema que facilite a organização e reduza o trabalho manual.

---

### Resumo dos Usuários

| **Grupo de Usuários**       | **Principais Necessidades**                                                                 |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Pacientes**                | Agendamento rápido, lembretes automáticos e acesso ao histórico médico.                    |
| **Médicos**                  | Gestão de agendas, acesso a prontuários e alertas de consultas.                            |
| **Recepcionistas/Administradores** | Gerenciamento de agendas, confirmação de consultas e geração de relatórios.           |

---

## 4. Restrições do Projeto e do Produto

### 4.1 Tecnologia e Padrões
O desenvolvimento do sistema de agendamento de consultas médicas está sujeito a algumas restrições tecnológicas e de padrões:

1. **Tecnologias Utilizadas**:
   - O sistema deve ser desenvolvido usando tecnologias modernas, como HTML5, CSS3, JavaScript (React para o front-end e Node.js para o back-end).
   - O banco de dados deve ser seguro e escalável, como PostgreSQL ou MongoDB.

2. **Padrões de Desenvolvimento**:
   - O código deve seguir boas práticas de programação, como clean code e versionamento com Git.
   - O sistema deve ser responsivo, funcionando bem em dispositivos móveis e desktops.

3. **Integrações**:
   - O sistema precisa se integrar com APIs de terceiros, como gateways de pagamento (ex.: PayPal, Stripe) e serviços de autenticação (ex.: Google, Facebook).
   - Deve ser compatível com sistemas de planos de saúde e laboratórios.

4. **Segurança**:
   - O sistema deve usar criptografia para proteger dados sensíveis, como informações médicas e pessoais.
   - Deve seguir padrões de segurança, como HTTPS e proteção contra ataques cibernéticos.

---

### 4.2 Legislação e Regulamentações
O sistema deve estar em conformidade com as seguintes leis e regulamentações:

1. **Lei Geral de Proteção de Dados (LGPD)**:
   - O sistema deve garantir a privacidade e segurança dos dados dos usuários, seguindo as diretrizes da LGPD.
   - Os usuários devem consentir com o uso de seus dados, e o sistema deve permitir que eles solicitem a exclusão de suas informações.

2. **Regulamentações Médicas**:
   - O sistema deve seguir as normas do Conselho Federal de Medicina (CFM) para prontuários eletrônicos e armazenamento de dados médicos.
   - Deve garantir a confidencialidade das informações de saúde dos pacientes.

3. **Acessibilidade**:
   - O sistema deve ser acessível a todos os usuários, incluindo pessoas com deficiência, seguindo as diretrizes do WCAG (Web Content Accessibility Guidelines).

---

### Resumo das Restrições

| **Categoria**               | **Restrições**                                                                 |
|------------------------------|--------------------------------------------------------------------------------|
| **Tecnologia e Padrões**     | Uso de tecnologias modernas, integrações com APIs, segurança e responsividade. |
| **Legislação e Regulamentações** | Conformidade com LGPD, normas do CFM e acessibilidade |

---

## 5. Análise de Riscos e Mitigação

Abaixo estão os principais riscos identificados para o projeto do sistema de agendamento de consultas médicas, juntamente com estratégias para mitigá-los:

---

### Tabela de Riscos e Mitigação

| **Risco**                     | **Impacto**       | **Probabilidade** | **Estratégia de Mitigação**                                                                 |
|--------------------------------|-------------------|-------------------|--------------------------------------------------------------------------------------------|
| **Vazamento de dados**         | Alto              | Média             | Implementar criptografia de dados, usar protocolos seguros (HTTPS) e realizar auditorias regulares de segurança. |
| **Falha na integração com APIs** | Médio            | Alta              | Realizar testes extensivos nas integrações e ter planos de contingência para APIs alternativas. |
| **Baixa adoção por médicos e clínicas** | Alto      | Média             | Oferecer treinamentos, suporte técnico e demonstrar os benefícios do sistema para os usuários. |
| **Atrasos no desenvolvimento** | Médio             | Alta              | Usar metodologias ágeis (como Scrum) para gerenciar prazos e priorizar funcionalidades essenciais. |
| **Ataques cibernéticos**       | Alto              | Baixa             | Implementar firewalls, sistemas de detecção de intrusões e manter o software sempre atualizado. |
| **Não conformidade com leis**  | Alto              | Média             | Consultar especialistas em LGPD e outras regulamentações desde o início do projeto.         |

---

### Explicação dos Riscos

1. **Vazamento de dados**:
   - **Impacto**: Perda de confiança dos usuários e possíveis multas por violação de privacidade.
   - **Mitigação**: Usar criptografia e protocolos seguros, além de realizar auditorias frequentes.

2. **Falha na integração com APIs**:
   - **Impacto**: Funcionalidades essenciais, como pagamentos ou autenticação, podem parar de funcionar.
   - **Mitigação**: Testar todas as integrações e ter APIs de backup.

3. **Baixa adoção por médicos e clínicas**:
   - **Impacto**: O sistema pode não atingir o público-alvo, resultando em prejuízos financeiros.
   - **Mitigação**: Oferecer treinamentos e suporte para facilitar a transição para o sistema.

4. **Atrasos no desenvolvimento**:
   - **Impacto**: O projeto pode ultrapassar o prazo e o orçamento.
   - **Mitigação**: Usar metodologias ágeis para gerenciar o tempo e priorizar tarefas.

5. **Ataques cibernéticos**:
   - **Impacto**: Roubo de dados ou interrupção do serviço.
   - **Mitigação**: Implementar medidas de segurança robustas e manter o sistema atualizado.

6. **Não conformidade com leis**:
   - **Impacto**: Multas e problemas legais.
   - **Mitigação**: Consultar especialistas em regulamentações desde o início do projeto.

---

### Resumo dos Riscos

| **Categoria de Risco**         | **Estratégia de Mitigação**                                                                 |
|--------------------------------|--------------------------------------------------------------------------------------------|
| **Vazamento de dados**         | Criptografia, protocolos seguros e auditorias regulares.                                   |
| **Falha na integração com APIs** | Testes extensivos e planos de contingência.                                               |
| **Baixa adoção**               | Treinamentos, suporte técnico e demonstração de benefícios.                                |
| **Atrasos no desenvolvimento** | Uso de metodologias ágeis e priorização de tarefas.                                       |
| **Ataques cibernéticos**       | Firewalls, detecção de intrusões e atualizações constantes.                               |
| **Não conformidade com leis**  | Consultoria com especialistas em regulamentações desde o início.                           |

---
**Referências**:

1. Problemas de gestão médica que um software pode resolver. Disponível em: [https://www.doctormax.com.br/problemas-na-gestao-medica/](https://www.doctormax.com.br/problemas-na-gestao-medica/)
2. CLÍNICAS. Clínicas privadas perdem até R$ 144 mil por problemas com agendamento de consultas. Disponível em [https://medicinasa.com.br/agendamento-consultas/](https://medicinasa.com.br/agendamento-consultas/)
3. O Uso de Software Médico é Decisivo para o Futuro das Clínicas Médicas. Disponível em [https://emed.com.br/o-uso-de-software-medico-e-decisivo-para-o-futuro-das-clinicas-medicas/](https://emed.com.br/o-uso-de-software-medico-e-decisivo-para-o-futuro-das-clinicas-medicas/)
4. Lei Geral de Proteção de Dados (LGPD). Disponível em: [https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm).
5. Web Serviços Amazon (AWS). Disponível em: [https://aws.amazon.com/pt/health/](https://aws.amazon.com/pt/health/).
6. Documentação API Google Calendar. Disponível em: [https://developers.google.com/calendar](https://developers.google.com/calendar).
7. Documentação API Safrapay. Disponível em: [https://developers.safrapay.com.br](https://developers.safrapay.com.br)
8. Documentação API Asaas. Disponível em: [https://docs.asaas.com/docs/visao-geral](https://docs.asaas.com/docs/visao-geral)
9. O que é um **Wearable**?. Disponível em: [https://www.iberdrola.com/inovacao/tecnologia-wearable](https://www.iberdrola.com/inovacao/tecnologia-wearable)
10. Documentação API Blip. Disponível em: [https://docs.blip.ai/#introduction](https://docs.blip.ai/#introduction)
11. WCAG - As diretrizes de acessibilidade para o conteúdo da web de forma descomplicada. Disponível em: [https://mwpt.com.br/wcag-as-diretrizes-de-acessibilidade-para-o-conteudo-da-web-de-forma-descomplicada/](https://mwpt.com.br/wcag-as-diretrizes-de-acessibilidade-para-o-conteudo-da-web-de-forma-descomplicada/)
12. Partes interessadas primárias e secundárias em um projeto de software. Disponível em: [https://www.exposit.com/blog/primary-secondary-stakeholders-software-project/](https://www.exposit.com/blog/primary-secondary-stakeholders-software-project/)
13. Stakeholders: o que são, quais os tipos e como gerenciá-los? [https://rockcontent.com/br/blog/stakeholder/](https://rockcontent.com/br/blog/stakeholder/)
14. Normas CFM. Disponível em: [https://portal.cfm.org.br/](https://portal.cfm.org.br/)
15. Metodologia SCRUM. Disponível em: [https://pt.semrush.com/blog/scrum/](https://pt.semrush.com/blog/scrum/)
16. Mitigação de riscos. Disponível em: [https://www.atlassian.com/work-management/project-management/risk-mitigation](https://www.atlassian.com/work-management/project-management/risk-mitigation)
---
