# Como construir um programa de resposta a incidentes de segurança cibernética

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

Um guia prático para preparação, detecção, análise, contenção, recuperação e melhoria.
**Autor / Autor:** Alberto (Al) Leiva  
**Versão / Versão:** 1.0 - Julho / Julho 2026  
**Licença/Licença:** CC BY-NC-SA 4.0

## Finalidade e uso responsável

Este manual explica como construir, operar, testar e melhorar um programa de resposta a incidentes de segurança cibernética. Destina-se ao uso defensivo legal, autorizado e ético.
A segurança humana, a privacidade, a integridade das provas e as obrigações legais devem permanecer centrais em todas as investigações.

## 1. Fundamentos de resposta a incidentes

A resposta a incidentes é uma capacidade de toda a organização para preparar, detectar, analisar, conter, erradicar, recuperar e aprender com incidentes de segurança cibernética.
O NIST SP 800-61 Revisão 3 integra a resposta a incidentes em todo o gerenciamento de riscos de segurança cibernética e alinha a capacidade com o NIST Cybersecurity Framework 2.0.

## 2. Governança e estatuto do programa

Defina a missão do programa, autoridade, escopo, patrocinador executivo, horas de serviço, autoridade de escalonamento, direitos de decisão, limites legais e expectativas de relatórios.
A carta deve identificar quem pode isolar sistemas, desativar contas, preservar provas, contratar advogados externos, contactar as autoridades e comunicar externamente.

## 3. Funções e responsabilidades

Crie uma equipe multifuncional que inclua operações de segurança, TI, nuvem, identidade, jurídico, privacidade, recursos humanos, comunicações, continuidade de negócios, segurança física e liderança executiva.
Use uma matriz RACI para que cada tarefa crítica tenha um proprietário responsável e uma cobertura de backup clara.

## 4. Categorias e gravidade do incidente

Defina categorias como malware, ransomware, comprometimento de identidade, exposição de dados, uso indevido da nuvem, atividade interna, negação de serviço, comprometimento de aplicativos, incidente de fornecedor e incidente de sistema de IA.
A gravidade deve considerar o impacto nos negócios, a sensibilidade dos dados, a segurança, o escopo, a persistência, a exposição regulatória, a interrupção operacional e a capacidade do invasor.

## 5. Preparação e prontidão

Mantenha inventários precisos, sistemas robustos, backups protegidos, registro centralizado, horário sincronizado, contatos testados, diagramas atuais, acesso de emergência e manuais documentados.
Prepare métodos seguros de comunicação fora de banda caso o email normal ou as ferramentas de colaboração sejam comprometidas.

## 6. Detecção e relatórios

Crie vários canais de denúncia para funcionários, clientes, fornecedores, ferramentas automatizadas de segurança e pesquisadores externos.
Defina as informações mínimas exigidas em um relatório de incidente: relator, horário, ativos afetados, comportamento observado, localização das evidências, impacto nos negócios e ações já tomadas.

## 7. Triagem e análise inicial

Valide se o evento é um incidente, determine o escopo e a urgência, identifique as identidades e os sistemas afetados, preserve as evidências voláteis e designe um comandante do incidente.
Evite conclusões prematuras. Registre fatos confirmados, hipóteses de trabalho, incógnitas e níveis de confiança separadamente.

## 8. Estratégia de contenção

A contenção deve reduzir os danos, preservando ao mesmo tempo as provas e evitando perturbações desnecessárias dos negócios.
As opções incluem desabilitar contas, revogar tokens, isolar endpoints, bloquear indicadores, restringir caminhos de rede, suspender integrações, alternar credenciais e colocar serviços vulneráveis ​​off-line.

## 9. Erradicação e remediação

Remova artefatos maliciosos, feche mecanismos de persistência, corrija pontos fracos explorados, corrija configurações inseguras, reconstrua sistemas comprometidos quando a confiança estiver baixa e invalide credenciais roubadas.
Não declare a erradicação completa até que a equipe tenha testado a persistência alternativa e o comprometimento relacionado.

## 10. Recuperação e restauração

Restaure serviços em uma sequência controlada, valide a integridade, aumente o monitoramento, confirme a aceitação dos negócios e mantenha um plano de reversão.
Os critérios de recuperação devem ser mensuráveis ​​e aprovados pelos proprietários técnicos e empresariais.

## 11. Tratamento de evidências e análise forense

Preserve as evidências de maneira apropriada aos requisitos legais, regulatórios, de seguros e internos. Tempo de coleta de documentos, coletor, fonte, método, valores de hash quando apropriado, transferências, armazenamento e acesso.
Use pessoal treinado e ferramentas aprovadas. Não altere as evidências originais desnecessariamente.

## 12. Comunicações e notificações

Crie planos de comunicação internos, executivos, de clientes, regulatórios, policiais, seguradoras e de mídia antes que ocorra um incidente.
Use fatos verificados, proteja informações privilegiadas, evite especulações, coordene o tempo e mantenha um registro de decisões para notificações.

## 13. Manual de ransomware

As prioridades incluem vida e segurança, contenção, proteção de identidade, preservação de evidências, restauração de backups confiáveis, coordenação legal e regulatória e avaliação de roubo de dados.
Não presuma que a criptografia seja o único impacto. Investigue roubo de credenciais, persistência, movimento lateral e exfiltração.

## 14. Incidentes de nuvem e identidade

Os incidentes na nuvem geralmente envolvem tokens roubados, permissões excessivas, segredos expostos, automação comprometida, aplicativos OAuth maliciosos ou registros alterados.
Revise os logs do provedor de identidade, o acesso condicional, a ativação de funções privilegiadas, as entidades de serviço, as identidades da carga de trabalho, a atividade do plano de controle da nuvem e o acesso ao plano de dados.

## 15. Incidentes de terceiros e na cadeia de suprimentos

Exigir que os fornecedores forneçam notificação oportuna, escopo, indicadores, serviços afetados, status de contenção e evidências necessárias para avaliação do cliente.
Mantenha contatos alternativos e opções de continuidade para fornecedores críticos.

## 16. Incidentes no sistema de IA

Os incidentes de IA podem incluir injeção imediata, vazamento de dados confidenciais, ações autônomas inseguras, envenenamento de modelo ou recuperação, ferramentas de agente comprometidas e abuso de identidades não humanas.
Contém agentes, ferramentas, índices de dados, credenciais e endpoints de modelo afetados. Preserve prompts, metadados de chamadas de ferramentas, versões de configuração e registros de aprovação enquanto protege a privacidade.

## 17. Exercícios e testes

Use exercícios de mesa, simulações técnicas, exercícios de comunicação, testes de restauração de backup e exercícios de fornecedores.
Cada exercício deve produzir resultados documentados, proprietários, datas de vencimento, resultados de novos testes e alterações nos planos ou controles.

## 18. Métricas e melhoria contínua

Meça a prontidão, o tempo de detecção, o tempo de análise, o tempo de contenção, o tempo de recuperação, a recorrência, a qualidade das evidências, a conclusão do exercício, as ações atrasadas e a satisfação das partes interessadas.
Use métricas para melhorar a capacidade em vez de punir indivíduos por relatarem incidentes.

## 19. Plano de implementação 30/60/90-day

Primeiros 30 dias: estabeleça patrocínio, estatuto, contatos, modelo de gravidade, canal de denúncia, principais manuais e requisitos mínimos de registro.
Dias 31 a 60: definir funções, procedimentos de evidência, planos de comunicação, expectativas do fornecedor, exercícios e capacidades técnicas de contenção.
Dias 61-90: conduzir uma mesa completa, corrigir lacunas, automatizar evidências e métricas, integrar lições aprendidas e obter aprovação executiva.

## 20. Lista de verificação de prontidão de produção

Use a lista de verificação abaixo antes de declarar o programa operacional.

## Lista de verificação de prontidão

- [] Patrocinador executivo atribuído
- [] Estatuto do programa aprovado
- [] Caminhos de contato e escalação 24/7 testados
- [] Matriz de gravidade aprovada
- [] Principais manuais de incidentes documentados
- [] Comunicações fora de banda seguras disponíveis
- [] Registro e sincronização de horário verificados
- [] Procedimento de tratamento de evidências aprovado
- [] Contatos jurídicos, de privacidade, seguros e comunicações confirmados
- [] Autoridade de contenção documentada
- [] Restauração de backup testada
- [] Procedimentos de emergência de nuvem e identidade testados
- [ ] Requisitos de notificação do fornecedor estabelecidos
- [] Procedimentos de incidente de IA incluídos quando aplicável
- [] Exercício de mesa concluído
- [] Ações corretivas rastreadas até o fechamento
- [ ] Métricas e relatórios executivos estabelecidos
- [] Data da revisão anual agendada

## Referências oficiais

- [NIST SP 800-61 Rev. 3 - Recomendações e considerações sobre resposta a incidentes](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
- [Estrutura de segurança cibernética do NIST 2.0](https://www.nist.gov/cyberframework)
- [Manuais de resposta a incidentes e vulnerabilidades de segurança cibernética da CISA] (https://www.cisa.gov/resources-tools/resources/federal-government-cybersecurity-incident-and-vulnerability-response-playbooks)
- [Planejamento de resposta a incidentes da Microsoft](https://learn.microsoft.com/security/operations/incident-response-planning)
- [Benchmark de segurança em nuvem da Microsoft – Resposta a incidentes](https://learn.microsoft.com/security/benchmark/azure/mcsb-incident-response)
