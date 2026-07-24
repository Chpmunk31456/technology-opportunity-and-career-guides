# Como se preparar para uma auditoria SOC 2

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.


## Um guia prático para preparação, controles, evidências, testes e conformidade contínua

**Autor:** Alberto (Al) Leiva  
**Versão:** 1.0 - julho de 2026  
**Licença:** CC BY-NC-SA 4.0
> Somente uma empresa de CPA independente qualificada pode emitir um relatório SOC 2. Este manual é educacional e não substitui orientação oficial da AICPA ou aconselhamento profissional.

## Conteúdo

- [1. Compreendendo o SOC 2](#1-compreendendo-o-soc-2)
- [2. Relatórios Tipo 1 e Tipo 2](#2-relatórios-tipo-1-e-tipo-2)
- [3. Governança e propriedade de prontidão](#3-governança-e-propriedade-de-prontidão)
- [4. Definindo escopo e limites do sistema](#4-definindo-escopo-e-limites-do-sistema)
- [5. Critérios de serviços de confiança e mapeamento de controle](#5-critérios-de-serviços-de-confiança-e-mapeamento-de-controle)
- [6. Avaliação de risco](#6-avaliação-de-risco)
- [7. Políticas e padrões](#7-políticas-e-padrões)
- [8. Controles de acesso lógico](#8-controles-de-acesso-lógico)
- [9. Gestão de mudanças e desenvolvimento seguro](#9-gestão-de-mudanças-e-desenvolvimento-seguro)
- [10. Operações de segurança e resposta a incidentes](#10-operações-de-segurança-e-resposta-a-incidentes)
- [11. Disponibilidade e continuidade dos negócios](#11-disponibilidade-e-continuidade-dos-negócios)
- [12. Confidencialidade, privacidade e ciclo de vida dos dados](#12-confidencialidade-privacidade-e-ciclo-de-vida-dos-dados)
- [13. Gerenciamento de fornecedores e organizações de subserviços](#13-gerenciamento-de-fornecedores-e-organizações-de-subserviços)
- [14. Gerenciamento de evidências](#14-gerenciamento-de-evidências)
- [15. População, amostragem e exceções](#15-população-amostragem-e-exceções)
- [16. A descrição do sistema](#16-a-descrição-do-sistema)
- [17. Trabalhando com o auditor de serviço](#17-trabalhando-com-o-auditor-de-serviço)
- [18. Falhas comuns de prontidão](#18-falhas-comuns-de-prontidão)
- [19. Plano de prontidão 30/60/90-day](#19-plano-de-prontidão-306090-day)
- [20. Lista de verificação pronta para produção e projeto de portfólio](#20-lista-de-verificação-pronta-para-produção-e-projeto-de-portfólio)

## 1. Compreendendo o SOC 2

SOC 2 é um exame dos controles em uma organização de serviços relevantes para segurança, disponibilidade, integridade de processamento, confidencialidade ou privacidade. Um auditor de serviço realiza o exame; a administração prepara a descrição do sistema, faz afirmações, possui os controles e fornece evidências. SOC 2 não é uma certificação de produto e não é uma verificação técnica única.
- A segurança é o critério comum e está incluída em todos os compromissos do SOC 2.
- Disponibilidade, integridade de processamento, confidencialidade e privacidade são selecionadas quando relevantes para compromissos e requisitos do sistema.
- O escopo deve corresponder aos serviços, componentes do sistema, locais, pessoas, processos, dados e organizações de subserviços que são importantes para os usuários.

## 2. Relatórios Tipo 1 e Tipo 2

Um relatório Tipo 1 aborda a concepção e implementação de controles em uma data específica. Um relatório Tipo 2 também aborda a eficácia operacional durante um determinado período de revisão. Os clientes normalmente solicitam o Tipo 2 porque fornece evidência de operação sustentada.
- Escolha o tipo de relatório com base nas necessidades do cliente, maturidade, histórico operacional disponível e aconselhamento do auditor.
- Não descreva um controle como operando por um período, a menos que a organização possa produzir evidências completas e consistentes.
- Planeje tempo suficiente para remediação antes do início do período de exames.

## 3. Governança e propriedade de prontidão

A preparação para SOC 2 é um programa multifuncional. A segurança pode coordená-lo, mas a operação de evidências e controle geralmente depende de engenharia, TI, recursos humanos, jurídico, privacidade, finanças, instalações, operações de clientes e liderança executiva.
- Nomeie um patrocinador executivo, líder do programa, proprietários de controle, fornecedores de evidências, proprietário da descrição do sistema e proprietários de remediação.
- Criar uma matriz RACI e uma reunião de preparação recorrente.
- Escalar antecipadamente evidências perdidas, remediações atrasadas e alterações de escopo não controladas.

## 4. Definindo escopo e limites do sistema

Um escopo defensável começa com os compromissos de serviço assumidos com os clientes e o sistema usado para cumprir esses compromissos. Evite definir o escopo apenas do aplicativo de produção, ignorando identidades de suporte, serviços de nuvem, processos de suporte, pipelines de desenvolvimento, monitoramento ou fornecedores principais.
- Documentar produtos e serviços no escopo.
- Identificar infraestrutura, software, pessoas, procedimentos e dados.
- Identificar limites físicos e lógicos.
- Liste as organizações de subserviços e escolha a apresentação separada ou inclusiva com o auditor.
- Documentar os controles complementares da entidade usuária que os clientes devem realizar.

## 5. Critérios de serviços de confiança e mapeamento de controle

Mapeie riscos e controles de acordo com os Critérios de Serviços de Confiança aplicáveis, sem tratar os critérios como uma lista de verificação de tecnologias prescritas. Os controles devem responder aos riscos, compromissos e requisitos de sistema reais da organização.
- Comece com riscos e compromissos e depois identifique os controles.
- Mapeie cada controle para um ou mais critérios e explique o relacionamento.
- Evite controles duplicados com nomes diferentes, a menos que as atividades sejam genuinamente distintas.
- Utilizar pontos focais como considerações de implementação, e não como controles obrigatórios separados.

## 6. Avaliação de risco

Um programa SOC 2 precisa de um processo documentado para identificar objetivos, ameaças, vulnerabilidades, riscos de fraude, mudanças, terceiros e impactos potenciais. A avaliação de risco deve informar o projeto do controle e deve ser atualizada após alterações materiais.
- Definir critérios de risco e propriedade.
- Conectar riscos a controles e decisões de tratamento.
- Inclui nuvem, identidade, cadeia de fornecimento de software, privacidade, disponibilidade e riscos internos.
- Registrar os riscos aceitos e a aprovação da administração.

## 7. Políticas e padrões

As políticas estabelecem expectativas de gestão; padrões e procedimentos explicam como o trabalho é executado. Uma política que não é comunicada, aprovada, revista e apoiada por provas operacionais é uma prova de auditoria fraca.
- Manter versão, proprietário, aprovador, data de vigência e data de revisão.
- Treinar o pessoal afetado.
- Conectar declarações de política aos controles implementados.
- Remover documentos obsoletos ou contraditórios.

## 8. Controles de acesso lógico

Os controles de acesso devem abranger usuários da força de trabalho, usuários privilegiados, contas de serviço, aplicativos, agentes, prestadores de serviços e terceiros em todo o ciclo de vida.
- Documentar integração, mudanças de função e rescisão.
- Exija autenticação forte e proteja o acesso privilegiado.
- Revise o acesso periodicamente.
- Monitore contas inativas, compartilhadas, emergenciais e não humanas.
- Retenha evidências de solicitações, aprovações, provisionamento, revisões e remoções.

## 9. Gestão de mudanças e desenvolvimento seguro

Os controles de alterações devem mostrar que as alterações são autorizadas, testadas, revisadas, rastreáveis ​​e separadas da aprovação da produção, quando apropriado.
- Use tickets ou pull requests com aprovações.
- Proteja filiais de produção e credenciais de implantação.
- Documentar alterações emergenciais e revisão retrospectiva.
- Conecte correções de vulnerabilidades e atualizações de dependências para alterar registros.
- Reter evidências de implantação durante todo o período de exame.

## 10. Operações de segurança e resposta a incidentes

O monitoramento da segurança, o gerenciamento de vulnerabilidades, a triagem de eventos, a resposta a incidentes e as lições aprendidas devem funcionar como um processo conectado.
- Definir gravidade e escalonamento.
- Retenha verificações de vulnerabilidades, registros de remediação, alertas, casos, cronogramas de incidentes e análises pós-incidentes.
- Testar o plano de resposta a incidentes.
- Acompanhe problemas recorrentes e ações corretivas.

## 11. Disponibilidade e continuidade dos negócios

Quando a disponibilidade está no âmbito, os controlos devem abordar compromissos de capacidade, resiliência, backups, recuperação, monitorização e continuidade.
- Definir objetivos de recuperação que apoiem os compromissos do cliente.
- Teste backups e restauração, não apenas a conclusão do backup.
- Exercer planos de continuidade de negócios e recuperação de desastres.
- Documentar incidentes, tempo de inatividade, tendências de capacidade e ações corretivas.

## 12. Confidencialidade, privacidade e ciclo de vida dos dados

A confidencialidade protege as informações designadas como confidenciais. A privacidade aborda informações pessoais durante a coleta, uso, retenção, divulgação e descarte. As duas categorias se sobrepõem, mas não são intercambiáveis.
- Inventário de dados sensíveis e pessoais.
- Definir regras de classificação, retenção, exclusão, criptografia e acesso.
- Rever as disposições relativas à partilha de dados e aos subprocessadores.
- Documente avisos de privacidade, escolhas, solicitações e procedimentos de incidentes quando a privacidade estiver no escopo.

## 13. Gerenciamento de fornecedores e organizações de subserviços

As organizações continuam responsáveis ​​por compreender as dependências de provedores de nuvem, processadores, fornecedores de suporte e outras organizações de subserviços.
- Realize a devida diligência baseada em risco antes da integração.
- Revise contratos e compromissos de segurança.
- Obter e avaliar relatórios de garantia relevantes.
- Rastrear controles complementares da organização de subserviços.
- Monitorar mudanças, incidentes, desempenho e rescisão.

## 14. Gerenciamento de evidências

Boas evidências são relevantes, completas, precisas, atribuíveis, com prazo determinado e protegidas contra alterações. As capturas de tela por si só costumam ser fracas porque podem não mostrar a população, o intervalo de datas, o proprietário, a aprovação ou o histórico operacional.
- Definir requisitos de evidência para cada controle antes do início do período.
- Preservar as populações e as exportações geradas pelo sistema.
- Fonte do registro, proprietário, data, escopo e revisor.
- Proteja evidências confidenciais e controle o acesso do auditor.
- Use nomenclatura consistente e um índice de evidências.

## 15. População, amostragem e exceções

Para controlos recorrentes, o auditor pode selecionar amostras de uma população completa. A gestão deve ser capaz de produzir a população completa e explicar como ela foi gerada.
- Reconciliar contagens populacionais com sistemas de origem.
- Não selecione ou remova itens com falha.
- Investigar exceções e identificar a causa raiz.
- Distinguir lacunas de evidência isoladas de falhas de controlo.
- Correção de documentos e se testes adicionais são necessários.

## 16. A descrição do sistema

A administração prepara a descrição do sistema da organização de serviços. Deve ser preciso, equilibrado e consistente com as operações reais e os compromissos do cliente.
- Descrever serviços, limites, infraestrutura, software, pessoas, procedimentos, dados e eventos significativos.
- Explicar critérios aplicáveis, atividades de controle, organizações de subserviços e controles complementares de entidades usuárias.
- Evite linguagem de marketing que exagere nas capacidades.
- Atualize a descrição quando o sistema mudar.

## 17. Trabalhando com o auditor de serviço

Selecione uma empresa de CPA qualificada com experiência relevante no setor e em tecnologia. Combine o escopo, o prazo, os critérios, o tipo de relatório, o tratamento dos subserviços, os marcos, os métodos de evidência e os protocolos de comunicação.
- Fornecer informações precisas e divulgar incidentes conhecidos ou problemas de controle.
- Esclareça as solicitações com antecedência, em vez de enviar documentos não relacionados.
- Rastreie solicitações abertas, perguntas, exceções e respostas de gerenciamento.
- A gestão possui prontidão; o auditor deve permanecer independente.

## 18. Falhas comuns de prontidão

Os problemas frequentes incluem âmbito pouco claro, populações em falta, controlos que existem apenas nas políticas, aprovações inconsistentes, provas criadas após o facto, acesso obsoleto, recuperação não testada e declarações não suportadas na descrição do sistema.
- Realize uma avaliação de lacunas pré-período.
- Execute coleções de evidências simuladas.
- Teste os controles antes de confiar neles.
- Não congelar o sistema nem o processo de provas; em vez disso, use o controle de alterações.
- Trate as exceções repetidas como problemas sistêmicos.

## 19. Plano de prontidão 30/60/90-day

Um roteiro prático ajuda a organização a passar de controles fragmentados para um modelo operacional auditável.
- Dias 1 a 30: confirmar a necessidade do negócio, selecionar o escopo preliminar, atribuir proprietários, sistemas de inventário, mapear compromissos e identificar lacunas críticas.
- Dias 31 a 60: finalizar a matriz de controle, corrigir lacunas de alto risco, criar procedimentos de evidências, redigir a descrição do sistema e realizar testes simulados.
- Dias 61-90: operar controles de forma consistente, resolver exceções, validar populações, concluir a revisão de prontidão e confirmar o momento do exame com o auditor.

## 20. Lista de verificação pronta para produção e projeto de portfólio

A decisão final de prontidão deve ser baseada em evidências. Para um projeto de portfólio seguro, os alunos podem criar uma organização de serviço fictícia, declaração de escopo, registro de risco, matriz de controle, índice de evidências, revisão de acesso de amostra, registro de incidente e esboço de descrição do sistema higienizado.
- Nunca carregue evidências confidenciais de clientes, dados reais de funcionários, capturas de tela de produção, segredos ou documentos de auditoria reais em um repositório público.
- Rotule os artefatos fictícios com clareza.
- Explique suposições, limitações e como cada controle reduz um risco declarado.

## Referências oficiais

- [Visão geral do AICPA SOC para organizações de serviços](https://www.aicpa-cima.com/resources/download/soc-for-service-organizations-engagements-overview)
- [Recursos AICPA SOC 2](https://www.aicpa-cima.com/topic/audit-assurance/audit-and-assurance-greater-than-soc-2)
- [Guia de relatórios AICPA SOC 2](https://www.aicpa-cima.com/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy)
