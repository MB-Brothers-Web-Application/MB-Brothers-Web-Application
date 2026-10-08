<div align="center">

# 🥊 MB BROTHERS

### Academia • Musculação • Artes Marciais • Saúde

**Sistema de gestão e atendimento para academia, disponível via site e aplicativo.**

![Status](https://img.shields.io/badge/status-em%20planejamento-F59E0B?style=for-the-badge)
![Plataformas](https://img.shields.io/badge/plataformas-web%20%7C%20mobile-1F2937?style=for-the-badge)
![Segmento](https://img.shields.io/badge/segmento-fitness%20%26%20lutas-E85D04?style=for-the-badge)

</div>

---

## 📖 Sobre o projeto

O **MB BROTHERS** é um projeto de plataforma digital para uma academia que integra **musculação, jiu-jitsu, muay-thai e boxe**, além de serviços complementares de **fisioterapia, nutrição e avaliações físicas periódicas**.

A proposta é facilitar a experiência dos alunos e centralizar a administração da academia em um único sistema, com informações sobre modalidades, planos, matrículas, turmas, horários, vagas e agendamentos.

O projeto também contempla turmas voltadas à **formação de atletas de MMA**, desde categorias infantis até faixas etárias mais avançadas, respeitando critérios de idade e nível técnico.

> [!NOTE]
> Este repositório documenta a **especificação e o planejamento** do sistema. As funcionalidades descritas representam o escopo pretendido e não necessariamente recursos já implementados.

## 🎯 Objetivos

- Facilitar o cadastro e o atendimento aos alunos.
- Exibir **grade fixa de aulas** e **disponibilidade de vagas** por turma.
- Organizar turmas por modalidade, idade, capacidade e professor.
- Permitir agendamentos para serviços de saúde e acompanhamento físico.
- Centralizar a gestão de alunos, matrículas, planos e horários.
- Divulgar oportunidades esportivas por meio de um mural de campeonatos.

## 🧩 Módulos do sistema

O projeto prevê **dois ambientes integrados**, que compartilham os mesmos dados:

| Ambiente | Público | Responsabilidade |
| --- | --- | --- |
| **Portal do Aluno** | Alunos e responsáveis | Cadastro, dados pessoais, consulta de turmas, matrículas, pagamentos e agendamentos. |
| **Painel Administrativo** | Equipe autorizada | Gestão de alunos, turmas, horários, profissionais, serviços, planos e matrículas. |

### 👤 Portal do Aluno

- **Cadastro e acesso:** criação de conta, login, recuperação de senha e atualização cadastral.
- **Matrículas:** visualização de modalidades, planos, turmas e solicitação de matrícula.
- **Horários:** consulta da grade fixa por dia da semana e modalidade.
- **Vagas:** identificação de turmas disponíveis ou lotadas.
- **Classificação etária:** apresentação automática de turmas compatíveis com a data de nascimento do aluno.
- **Serviços de saúde:** consulta e agendamento de fisioterapia, nutrição e avaliações físicas.
- **Pagamentos:** cadastro e atualização de informações de pagamento, conforme a integração definida.
- **Atendimento:** acesso a canais de WhatsApp e e-mail para dúvidas, matrícula e cancelamento.
- **Responsáveis legais:** identificação de responsável para alunos menores de idade.

### 🛠️ Painel Administrativo

- **Alunos:** consulta e manutenção de dados, situação cadastral e modalidades contratadas.
- **Turmas:** criação e atualização de modalidades, faixas etárias, professores e capacidade máxima.
- **Horários:** organização da grade fixa, com alterações restritas a pessoas autorizadas.
- **Agendamentos:** gestão de profissionais, horários, confirmações, cancelamentos e reagendamentos.
- **Planos e matrículas:** manutenção dos planos e acompanhamento das solicitações e vínculos dos alunos.
- **Visão geral:** indicadores operacionais, como alunos cadastrados, turmas ativas, vagas e atendimentos.

## 🏋️ Modalidades e serviços

| Tipo | Oferta | Disponibilidade no sistema |
| --- | --- | --- |
| Treinamento | Musculação | Informações, planos e matrícula. |
| Artes marciais | Jiu-jitsu, muay-thai e boxe | Turmas, horários, faixas etárias e vagas. |
| Formação esportiva | Preparação de atletas de MMA | Turmas por idade e nível de formação. |
| Saúde | Fisioterapia | Cadastro e agendamento. |
| Saúde | Nutrição | Cadastro e agendamento. |
| Acompanhamento | Avaliações físicas periódicas | Cadastro e agendamento. |

## 📅 Grade de aulas e vagas

- Os **horários das aulas são fixos**, definidos pela administração.
- Cada turma possui modalidade, professor, dia, horário, faixa etária e **limite de vagas**.
- O aluno consegue consultar as turmas e verificar sua disponibilidade.
- Não será permitido ultrapassar a capacidade máxima de uma turma.
- Mudanças administrativas devem refletir nas informações apresentadas ao aluno.

### Classificação automática por idade

A data de nascimento informada no cadastro será utilizada para calcular a idade do aluno e identificar turmas elegíveis. Os limites etários serão configurados pela administração.

**Exemplo de funcionamento:** cadastro do aluno → cálculo da idade → verificação dos limites da turma → exibição das opções elegíveis.

> As faixas etárias exatas e os critérios de progressão técnica serão definidos com a academia antes da implementação.

## 🩺 Agendamentos

Os serviços de **fisioterapia, nutrição e avaliações físicas** exigirão cadastro no sistema. O fluxo previsto é:

1. O aluno acessa sua conta.
2. Seleciona o serviço desejado.
3. Consulta as datas e os horários disponibilizados pelo profissional.
4. Solicita um agendamento.
5. Acompanha sua situação e eventuais alterações.

O sistema deverá impedir conflitos de horário para um mesmo profissional e respeitar a disponibilidade cadastrada.

## 🏆 Mural de campeonatos — funcionalidade futura

Espaço dedicado à divulgação de competições de **jiu-jitsu, muay-thai, boxe e MMA**, com:

- Nome, modalidade, data e local do evento.
- Categoria ou faixa etária, quando aplicável.
- Prazo de inscrição, caso informado.
- **Link para a página oficial do campeonato**, onde o atleta poderá se inscrever.

Inicialmente, os eventos poderão ser cadastrados manualmente pelos administradores. Integrações automáticas dependerão da disponibilidade de fontes ou APIs oficiais.

## 📋 Regras de negócio

| ID | Regra |
| --- | --- |
| **RN01** | Cadastro obrigatório para solicitar matrícula e agendar serviços de saúde. |
| **RN02** | A elegibilidade das turmas deve considerar automaticamente a idade do aluno. |
| **RN03** | Uma turma não pode ultrapassar sua capacidade máxima. |
| **RN04** | Somente administradores autorizados podem alterar a grade fixa. |
| **RN05** | Agendamentos devem respeitar a disponibilidade e evitar conflitos. |
| **RN06** | Alunos podem atualizar seus dados cadastrais e informações de pagamento editáveis. |
| **RN07** | Operações administrativas exigem autenticação e permissão apropriadas. |
| **RN08** | Menores de idade devem possuir vínculo com responsável legal. |
| **RN09** | O horário comercial de atendimento divulgado é das **8h às 18h**. |
| **RN10** | Inscrições em campeonatos ocorrem por links externos oficiais. |

## 🔐 Requisitos não funcionais

- **Responsividade:** navegação adequada em computadores, tablets e smartphones.
- **Segurança:** autenticação, autorização por perfil e proteção de dados.
- **Privacidade:** conformidade com a **LGPD**, com cuidados especiais para informações de saúde e dados de menores.
- **Integridade:** prevenção de matrículas acima do limite e de agendamentos conflitantes.
- **Usabilidade:** interface clara e acessível para alunos e administradores.
- **Manutenibilidade:** estrutura organizada para facilitar correções e evolução do produto.
- **Integração:** possibilidade de conectar provedores de pagamento, comunicação e plataformas de eventos.

## 🏗️ Arquitetura prevista

A proposta inicial é manter os dois ambientes ligados a uma **API e a uma base de dados centralizadas**, com responsabilidades bem separadas.

```text
              MB BROTHERS
                    |
         +----------+----------+
         |                     |
   Portal do Aluno       Painel Admin
         |                     |
         +----------+----------+
                    |
                   API
                    |
             Banco de Dados
```

**Tecnologias:** a stack de front-end, back-end, banco de dados, autenticação e hospedagem ainda será definida. Esta seção será atualizada conforme as decisões técnicas do projeto.

### Entidades iniciais para modelagem

`Usuario` · `Aluno` · `Responsavel` · `Modalidade` · `Turma` · `Horario` · `Matricula` · `Profissional` · `Servico` · `Agendamento` · `Plano` · `Pagamento` · `Campeonato`

> A modelagem final, os relacionamentos e os campos de cada entidade serão estabelecidos na etapa de análise e desenho do banco de dados.

## 🚀 Roadmap

- [ ] **Fase 1 — Base do sistema:** autenticação, alunos, modalidades, turmas, horários, identificação etária, vagas e administração.
- [ ] **Fase 2 — Serviços e gestão:** agendamentos, profissionais, planos, pagamentos, matrículas e atendimento.
- [ ] **Fase 3 — Expansão:** mural de campeonatos, integrações externas e melhorias para o acompanhamento esportivo.

## ❓ Definições pendentes

Antes de iniciar as implementações, será necessário definir com a academia:

- Faixas etárias e critérios de evolução técnica das turmas.
- Capacidade máxima, professores e horários fixos.
- Planos, preços, condições e meios de pagamento.
- Fluxo de aprovação da matrícula e políticas de cancelamento.
- Regras de agendamento e periodicidade das avaliações físicas.
- Acesso e autorizações dos responsáveis legais.
- Contatos oficiais e canais de atendimento.

## 📞 Contato e atendimento

Para dúvidas, informações sobre matrícula ou solicitações de cancelamento, a proposta é disponibilizar links diretos para **WhatsApp** e **e-mail** no site.

**Horário comercial:** 8h às 18h.

*Os endereços oficiais de contato serão adicionados após sua definição.*

---

<div align="center">

**MB BROTHERS**  
*Treinamento, saúde e desenvolvimento esportivo em uma só plataforma.*

</div>
