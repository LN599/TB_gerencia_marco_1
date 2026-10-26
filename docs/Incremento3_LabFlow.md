# LabFlow — Incremento 3: integração e encerramento (planejamento)

**Aluno:** Luiz Soares de Sousa Neto — matrícula 558546  
**Repositório:** https://github.com/LN599/TB_gerencia_marco_1  
**GitHub Projects:** https://github.com/users/LN599/projects/1  
**Período de entrega:** 01 a 04/12/2026

> **Natureza:** trabalho acadêmico de gerenciamento. Cronograma, orçamento, equipe, contratos e EVM são simulações de planejamento; não representam desenvolvimento ou despesas efetivos. Este documento complementa os Incrementos 1 e 2, sem alterar suas baselines. O Change Request oficial da docente ainda está pendente.

## 1. Contexto e baselines anteriores
O LabFlow propõe sistema web para reservas, aprovações, registro de incidentes e acompanhamento dos laboratórios de informática. O Incremento 1 definiu Business Case, stakeholders, escopo (RF01–RF12 e RNF01–RNF08), abordagem **híbrida** e EAP. O Incremento 2 estabeleceu baseline de **63,17 dias úteis**, com término administrativo previsto para **21/01/2027** e caminho crítico **A → B → C → E → F → H → I → J → L**. BAC: **R$ 34.000,00**, reserva contingencial de **R$ 4.000,00**; orçamento total: **R$ 38.000,00**. Cenário EVM simulado da semana 6: PV = R$ 16.256,25; EV = R$ 14.500; AC = R$ 16.500; CPI = 0,879; SPI = 0,892; EAC = R$ 38.689,66. A previsão excede o orçamento total em R$ 689,66, justificando controle reforçado.

## 2. Respostas aos riscos originais
As definições **R01–R08** e as exposições abaixo reproduzem a identificação do registro do Incremento 2; as **respostas** são novas propostas.

| ID | Risco | P×I | Estratégia | Responsável | Ação | Gatilho | Monitoramento |
|---|---|---|---|---|---|---|---|
| R01 | Regras de reserva inconsistentes | 4×5=20, alta | Mitigar | GP/coordenação | Oficinas de regras, matriz de conflitos e validação dos requisitos | Divergência entre grupos | Revisão semanal de decisões e aceite dos requisitos |
| R02 | Ambiente instável/indisponível | 3×4=12, média | Mitigar | DevOps | Teste de disponibilidade, restauração de backup e ambiente alternativo | Falha em testes | Checagem por execução e revisão de incidentes |
| R03 | Baixa adesão de docentes | 4×4=16, alta | Mitigar | UX/coordenação | Validação de protótipo, treinamento e piloto acompanhado | Baixo engajamento no piloto | Taxa de participação e feedback nas revisões |
| R04 | Falhas de privacidade/controle | 3×5=15, alta | Evitar | DevOps/QA | Controle de acesso por perfil, teste de autorização e bloqueio de liberação | Acesso indevido detectado | Testes de segurança e auditoria por release |
| R05 | Integração ou e-mail indisponível | 3×3=9, média | Transferir e mitigar | Desenvolvedor | SLA com provedor quando contratado, fila e retentativas | Atraso de API/fornecedor | Acompanhamento de falhas de entrega |
| R06 | Indisponibilidade de especialistas | 3×4=12, média | Mitigar | GP | Planejamento da capacidade, cobertura e documentação | Conflito de alocação | Revisão semanal de capacidade e impedimentos |
| R07 | Crescimento não controlado do escopo | 4×4=16, alta | Evitar | GP/Sponsor | Exigir registro e análise de impacto para mudanças na EAP | Solicitação fora da EAP | Log de mudanças e revisão da baseline |
| R08 | Sem janela para piloto acadêmico | 4×3=12, média | Mitigar | Coordenação | Reservar janela alternativa com antecedência | Turma não confirma data | Confirmação quinzenal até agendamento |

O GP acompanha risco residual, probabilidade, impacto e eficácia das ações; mudanças de prazo/custo dependem de aprovação. Transferência contratual de parte dos efeitos de R05 não transfere a responsabilidade gerencial pelo resultado.

## 3. Aquisições — Make-or-Buy
**MAKE:** regras de reserva, fluxos de aprovação, telas, integração funcional e testes na equipe fictícia, pois constituem o conhecimento central do produto. **BUY:** hospedagem/backup gerenciado e serviço de mensagens, quando necessários, devido ao ganho de suporte e capacidade de operação.

| Aquisição | Modelo proposto | Critério de escolha/aceite |
|---|---|---|
| Hospedagem e backup | Preço fixo por período/plano | SLA ≥ 99,5%, teste de restauração, portabilidade, proteção de dados |
| Mensageria transacional | Tempo e material/consumo com teto | Entrega observável, limite de gastos, suporte e alternativa |
| Avaliação externa de segurança (condicional) | Preço fixo por laudo | Checklist de vulnerabilidades e evidência de revisão |

**Custo reembolsável** foi avaliado e não é recomendado para aquisições pequenas com escopo bem definido, pela menor previsibilidade. As aquisições devem ser detalhadas e autorizadas **dentro do BAC de R$ 34 mil**; a reserva de R$ 4 mil não é verba adicional de contratação automática. Esta é uma análise, não comprovação de compra.

## 4. Project Charter — Carta do Projeto
**Justificativa:** reduzir conflitos de agendamento e dar rastreabilidade à gestão dos laboratórios. **Objetivo:** planejar a entrega de sistema web de reserva, aprovação, incidentes e indicadores para o contexto acadêmico definido no Business Case. **Patrocinador:** direção institucional fictícia; **GP:** Luiz Soares de Sousa Neto, no exercício acadêmico; **stakeholders centrais:** coordenação, docentes, suporte TI e equipe técnica simulada. **Escopo:** funcionalidades e requisitos aprovados no Incremento 1; exclusões devem seguir a EAP original. **Critérios de êxito:** fluxos críticos homologados, requisitos de segurança e desempenho aceitos e implantação-piloto autorizada. **Limites de referência:** BAC R$ 34 mil, contingência R$ 4 mil, prazo 63,17 dias úteis, término previsto 21/01/2027. **Autoridade:** GP coordena trabalho dentro da baseline; Sponsor aprova alterações que modifiquem baseline ou mobilizem reserva. **Autorização formal:** proposta de carta, sem assinatura ou aceite real.

## 5. Project Management Plan integrado
- **Integração:** charter, decisões, rastreabilidade e registro de mudanças supervisionados pelo GP.
- **Escopo:** RF01–RF12, RNF01–RNF08, histórias e EAP do Inc. 1; aceitar entregáveis apenas mediante critérios documentados.
- **Cronograma:** PERT/PDM/CPM e marcos do Inc. 2; acompanhar caminho crítico e folgas semanalmente.
- **Custos:** BAC R$ 34 mil, reserva R$ 4 mil; EVM e nova EAC em cada ciclo; sem rebaseline automática.
- **Qualidade:** ISO/IEC 25010, testes funcionais, segurança, desempenho, usabilidade; ciclo PDCA e registro de não conformidades.
- **Recursos:** equipe simulada de seis papéis/pessoas (GP, 2 devs, QA, UX e DevOps), com matriz de responsabilidades e revisão de capacidade.
- **Comunicação:** relatório quinzenal ao Sponsor, alinhamento semanal com coordenação, Issues/board para execução.
- **Riscos:** registro R01–R08, planos de resposta, gatilhos, donos e acompanhamento por prioridade.
- **Aquisições:** análise Make-or-Buy, seleção, contrato, inspeção e encerramento de fornecimento.
- **Stakeholders:** engajamento contínuo da coordenação/docentes, comunicação por interesse e influência.
- **Mudanças:** solicitação → análise integrada → decisão Sponsor → atualização da baseline autorizada → comunicação → verificação.

## 6. KPIs e rotina
| Indicador | Fórmula / meta planejada | Periodicidade | Responsável |
|---|---|---|---|
| SPI | EV/PV, alerta <0,95 | Semanal | GP |
| CPI | EV/AC, alerta <0,95 | Semanal | GP |
| EAC | BAC/CPI (se projeção pertinente); alerta se >R$ 38 mil | Quinzenal | GP |
| Conclusão de trabalho | Itens concluídos/previstos ×100 | Semanal | GP |
| Cobertura de aceite | Fluxos críticos aprovados/previstos ×100; meta 100% | A cada revisão | QA |
| Defeitos críticos | Abertos na liberação; meta 0 | A cada revisão | QA |
| Participação no piloto | Docentes participantes/convidados ×100; meta ≥80% | Piloto | UX/coordenação |
| Tempo de fluxo | Lead Time Ready→Done e Cycle Time In Progress→Done, somente com timestamps reais | Quinzenal | GP |

O GP consolida um painel quinzenal, registra variações em Issues e escala exceções ao patrocinador.

## 7. Controle integrado de mudanças
O enunciado exige analisar ao menos um **Change Request recebido da docente**. Até seu recebimento, a análise a seguir é **exemplo didático, não o pedido oficial**: adicionar integração com calendário institucional. **Impactos hipotéticos:** escopo + nova integração e testes; prazo +5 dias úteis, sujeitos a recálculo do CPM; custos +R$ 2.000 estimados, fora da baseline original; qualidade + risco de interoperabilidade e segurança; recursos + capacidade de integração/QA; riscos + dependência de API, autenticação e privacidade. **Decisão sugerida no exemplo:** adiar para fase posterior, dada EAC simulada acima do teto, salvo patrocínio com nova autorização de orçamento e prazo. Registrar justificativa e decisão real somente após avaliação do caso oficial.

## 8. Kanban na abordagem híbrida
A baseline preditiva continua; a visualização e o fluxo de gestão adotam **Kanban**: Backlog → Ready → In Progress → Review/Test → Done. Políticas WIP: Ready ≤5; In Progress ≤2; Review/Test ≤2. O trabalho é puxado conforme capacidade, as dependências críticas e os bloqueios ficam visíveis. **Lead Time** e **Cycle Time** exigem datas observadas no histórico real do board; não fabricar métricas. Não confundir movimentação de tarefas acadêmicas com conclusão do desenvolvimento fictício.

## 9. Encerramento planejado
Conferir requisitos/aceite, consolidar desvios e resultados EVM, registrar lições aprendidas, validar entregáveis com Sponsor, concluir contratos quando houver, arquivar riscos e decisões, fechar pendências, apresentar relatório de encerramento e desmobilização fictícia. O encerramento do projeto de software é cenário planejado, distinto da **entrega acadêmica do Incremento 3**, que requer PDF dentro de ZIP no SIGAA entre 01–04/12/2026 e URL do board na primeira página.

## 10. Pendências para entrega final
1. Substituir o Change Request ilustrativo pelo caso **efetivamente atribuído** pela docente.
2. Conferir board, labels, assignees, milestone AP3 e histórico verdadeiro (documentação no Git não altera automaticamente o board).
3. Confirmar acesso da docente ao projeto, sem inventar identidade ou permissões.
4. Gerar PDF final consolidado e compactá-lo isoladamente em ZIP, com nome regulamentar, antes do envio pelo SIGAA.

**Fontes internas:** `README.md`, `docs/Incremento2_LabFlow.md`, `dados/Incremento2_Riscos.csv`, `docs/Incremento2_GitHub_Projects.md`, além das instruções acadêmicas do Projeto Integrador.
