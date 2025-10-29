# Projeto

## Caso proposto: Modelagem de Dados de um Sistema de Gestão de Hospital Universitário

## Contexto geral

O hospital universitário oferece serviços de atendimento médico, ensino e pesquisa. Seu sistema deve gerenciar informações de pacientes, médicos, enfermeiros, procedimentos, leitos, setor de laboratório, agendamento, faturamento e histórico médico.

---

## Direcionamento para o projeto e documentação

---

## 1) Requisitos iniciais (levantamento)

1. **IDEF0**
2. **Modelagem do caso em cima das 5 visões da ISO 10746**
   - Cadastro e controle de pacientes (dados pessoais, CPF, endereço, plano de saúde)
   - Cadastro de profissionais (médicos, enfermeiros, técnico de laboratório)
   - Gestão dos setores do hospital (emergência, internação, laboratório, ambulatório, cirurgia)
   - Agendamento de consultas e procedimentos, incluindo prioridade de atendimento
   - Registro de atendimentos: diagnóstico, exames solicitados
   - Controle e agendamento de leitos por setor, ocupação, alta hospitalar
   - Controle financeiro: procedimentos realizados, faturamento por convênio ou particular
   - Histórico completo e seguro dos pacientes, com controle de acessos
   - Relatórios gerenciais (ex: taxa de ocupação, procedimentos realizados por médico, custo por setor)
   - Sistema de auditoria para registros alterados

---

## 2) Modelagem Conceitual (Diagrama ER)

- Entidades principais
- Relacionamentos
- Atributos chaves, atributos simples e compostos, multi valores e derivados
- Normalização preliminar para evitar redundância

---

## 3) Modelagem Lógica (Modelo relacional)

- Conversão do ER para tabelas relacionais
- Definição das chaves primárias e estrangeiras
- Restrições de integridade, regras de negócio (ex: o mesmo leito não pode estar ocupado por dois pacientes simultaneamente)
- Definição de índices para otimização das consultas (ex: índice no CPF do paciente, código do procedimento)

---

## 4) Modelagem Física no Oracle

- Criação das tabelas no Oracle, com tipos de dados adequados (VARCHAR2, NUMBER, DATE, etc)
- Scripts de criação de tabelas, constraints (PK, FK, UNIQUE)
- Triggers para manter integridade complexa (por exemplo, status automatizado do leito, controle de histórico)
- Procedimentos armazenados para operações comuns (cadastrar paciente, agendar consulta)
- Views para simplificar consultas complexas (ex: resumo de consulta para médicos)
- Funções e pacotes para encapsular regras de negócio
- Controle de transações para garantir atomicidade de operações
- Backup e manutenção (tarefa extra)

---

## 5) Consultas avançadas para simular relatórios e o que o sistema irá fazer

- Consultas SQL complexas: junções, subconsultas, agrupamentos com HAVING
- Análise de desempenho, explicação dos planos de execução
- Otimização usando índices e hints

---

## 6) Documentação entregue pelos alunos

- Documento com o diagrama ER e justificativas das escolhas
- Script SQL completo para criação do esquema físico
- Procedimentos e triggers comentados
- Problemas encontrados e soluções adotadas
- Relatório com consultas SQL feitas e análise dos resultados
- Apresentação oral explicando o sistema e as decisões técnicas

---

## Dicas para ir além e receber 10 se for bem feito

- Inserir requisitos não-funcionais bem explicados nas 5 visões
- Cobrir aspectos de concorrência, bloqueios e transações isoladas

---

# Links

- [Link de Entrega do Projeto](https://docs.google.com/forms/d/e/1FAIpQLSfWQHnP5bsSn6dmx21TX-ENZhkcm1OdGCBACYutUmFH5QDhbQ/viewform?usp=dialog)
- [Desafios das Aulas](https://docs.google.com/forms/d/e/1FAIpQLSdSPn55KyCTdmc5ZDU8QB-5miGJ-AvsIGTnWJDi8c_X-JqNBQ/viewform?usp=dialog)

