# Como se tornar um analista SOC

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.


## Um guia prático para iniciantes em operações de segurança, SIEM, triagem de alertas, caça a ameaças, resposta a incidentes e preparação para carreira

**Autor:** Alberto (Al) Leiva  
**Versão:** 1.0 - julho de 2026  
**Licença:** CC BY-NC-SA 4.0

COMO SE TORNAR UM ANALISTA SOC

# Aviso de finalidade e uso ético

Este manual fornece um caminho prático para operações de segurança. Use todas as ferramentas, registros, capturas de pacotes, amostras de malware e técnicas de investigação somente em sistemas de sua propriedade, laboratórios aprovados ou ambientes para os quais você tenha autorização explícita.
> Capacidade técnica não cria permissão. Proteja a privacidade, preserve evidências, siga o escopo e avance quando uma investigação puder afetar pessoas, obrigações legais ou operações comerciais.

# Índice

- 1. O que um analista SOC faz
- 2. Funções do SOC e progressão na carreira
- 3. Conhecimento fundamental
- 4. Logs e telemetria
- 5. Plataformas SIEM
- 6. Fluxo de trabalho de triagem de alerta
- 7. Investigações de endpoints
- 8. Investigações de identidade
- 9. Investigações de rede
- 10. Investigações de e-mail e phishing
- 11. Investigações na nuvem
- 12. MITRE ATT&CK e inteligência de ameaças
- 13. Engenharia de detecção
- 14. Caça a ameaças
- 15. Resposta a incidentes
- 16. Gestão e relatórios de casos
- 17. Laboratório doméstico e prática segura
- 18. Projetos de portfólio
- 19. Currículo e preparação para entrevistas
- 20. Plano 30/60/90-day
- 21. Acessibilidade e aprendizagem sustentável
- 22. Listas de verificação e modelos
- 23. Glossário
- 24. Recursos oficiais de aprendizagem

# 1. O que um analista SOC faz

Um analista do Security Operations Center (SOC) monitora dados de segurança, investiga atividades suspeitas, documenta descobertas e ajuda a coordenar a resposta. O analista transforma grandes volumes de sinais técnicos em decisões claras: fechar como benigno, continuar investigando, conter ou escalar.
| Responsabilidade | Exemplo prático |
| --- | --- |
| Monitorar | Revise filas SIEM, alertas de endpoint, eventos de risco de identidade e descobertas na nuvem. |
| Triagem | Determine se um alerta é uma atividade verdadeira positiva, falsa positiva, esperada ou não resolvida. |
| Investigar | Crie uma linha do tempo usando usuários, hosts, endereços IP, processos, arquivos e eventos de autenticação. |
| Responder | Contenha de acordo com a autoridade ou forneça recomendações claras à equipe do incidente. |
| Documento | Registre evidências, raciocínio, impacto nos negócios, ações e tarefas de acompanhamento. |
| Melhorar | Ajuste regras ruidosas, identifique lacunas de telemetria e proponha novas detecções. |

# 2. Funções do SOC e progressão na carreira

| Nível | Foco típico | Prova de preparação |
| --- | --- | --- |
| Nível 1 / Júnior | Monitoramento de filas, enriquecimento, triagem básica, revisão de phishing | Notas consistentes, escalação correta, consultas básicas, bom senso |
| Nível 2 / Analista | Investigação mais aprofundada de endpoint, identidade, rede e nuvem | Cronogramas, escopo, busca de ameaças, feedback de detecção |
| Nível 3 / Sênior | Investigações avançadas, caça a ameaças, engenharia de detecção | Casos complexos, mentoria, análise multiplataforma |
| Líder/Gerente | Operações, métricas, pessoal, qualidade, comunicação com as partes interessadas | Melhoria do programa, governança, relatórios executivos |
| Engenheiro de Detecção / Caçador | Analytics, desenvolvimento de regras, hipóteses, validação | Detecções versionadas, casos de teste, mapeamento de cobertura |

# 3. Conhecimento básico

- Rede: TCP/IP, DNS, HTTP/S, portas, NAT, VPNs, proxies, firewalls e protocolos comuns.
- Windows: processos, serviços, registro, logs de eventos, PowerShell, tarefas agendadas e autenticação.
- Linux: processos, permissões, serviços, logs, histórico de shell, SSH, cron e gerenciamento de pacotes.
- Identidade: usuários, grupos, MFA, SSO, tokens, acesso condicional, acesso privilegiado e contas de serviço.
- Nuvem: accounts/subscriptions, IAM, logs de auditoria, armazenamento, computação, rede e responsabilidade compartilhada.
- Fundamentos de segurança: malware, phishing, roubo de credenciais, movimentação lateral, persistência, exfiltração e ransomware.
- Habilidades profissionais: redação concisa, curiosidade, escalada calma, preservação de evidências e respeito à privacidade.

# 4. Registros e telemetria

| Fonte | O que pode responder |
| --- | --- |
| Ponto final / EDR | Qual processo foi executado? Qual arquivo foi alterado? Qual conexão de rede foi feita? |
| Logs de eventos do Windows | Quem fez login? Qual serviço, tarefa, grupo ou política foi alterado? |
| Provedor de identidade | Foi utilizado MFA? O login foi arriscado, incomum ou de um novo dispositivo? |
| DNS | Quais domínios foram consultados, por qual host e quando? |
| Firewall/proxy | Quais conexões foram permitidas ou bloqueadas? Quantos dados foram movidos? |
| Segurança de e-mail | Quem enviou a mensagem? Quais URLs, anexos e resultados de autenticação estavam presentes? |
| Auditoria em nuvem | Quem alterou um recurso, uma função, uma política, uma chave ou uma regra de rede? |
| Registros de aplicativos | Que ação ocorreu dentro do aplicativo de negócios? |
Uma boa análise depende da sincronização de tempo, de identificadores estáveis ​​de host e de usuário, de retenção útil, de campos normalizados e de uma compreensão dos dados ausentes. A ausência de um registro não é prova de que um evento não ocorreu.

# 5. Plataformas SIEM

Um SIEM coleta, normaliza, pesquisa, correlaciona e apresenta dados de segurança. As plataformas comuns incluem Microsoft Sentinel, Splunk Enterprise Security, Elastic Security, Wazuh e Security Onion. Aprenda primeiro os conceitos: ingestão de dados, esquemas, consultas, detecções, filas de alertas, casos, enriquecimento, automação e retenção.
| Plataforma | Foco iniciante |
| --- | --- |
| Microsoft Sentinela | Consultas KQL, regras analíticas, incidentes, entidades, pastas de trabalho, automação. |
| Splunk | Pesquisas SPL, campos, modelos de dados, eventos notáveis, painéis. |
| Segurança Elástica | KQL/Lucene, alertas, cronogramas, casos, endpoint e dados em nuvem. |
| Wazuh | Eventos de agente, integridade de arquivos, descobertas de vulnerabilidades, regras, painel. |
| Cebola de segurança | Monitoramento de segurança de rede, Zeek, Suricata, análise de pacotes, cases. |

# 6. Fluxo de trabalho de triagem de alerta

1. Leia o título do alerta, a lógica da regra, o intervalo de tempo, a gravidade e a origem.
1. Confirme o usuário, host, endereço IP, aplicativo e classificação de dados afetados.
1. Valide se a telemetria foi concluída e se os carimbos de data/hora usam o fuso horário correto.
1. Enriquecer com a criticidade dos ativos, a função do usuário, a reputação, a inteligência sobre ameaças e as mudanças recentes.
1. Crie um cronograma antes de chegar a uma conclusão.
1. Compare o comportamento com uma linha de base conhecida e uma atividade aprovada.
1. Decida: falso positivo, benigno verdadeiro positivo, incidente suspeito, confirmado ou evidência insuficiente.
1. Contenha ou escale de acordo com a autoridade e o manual.
1. Documente fatos, raciocínios, ações e incertezas remanescentes.
1. Fornece feedback de ajuste de detecção ou lacuna de telemetria.

## Perguntas de triagem

- O que exatamente desencadeou o alerta?
- Que evidências apoiam intenções maliciosas?
- Poderia ser administração, automação, testes ou viagens legítimas?
- O que aconteceu imediatamente antes e depois?
- A atividade está isolada ou presente em outros usuários ou hosts?
- Qual é o impacto potencial nos negócios?
- Que ação está autorizada neste momento?

# 7. Investigações de endpoints

- Identifique árvore de processos, linha de comando, relacionamentos pai-filho, contexto do usuário, hashes, assinaturas, persistência e conexões de rede.
- Verifique se o executável é esperado para esse host e usuário.
- Revise downloads recentes, histórico do navegador, anexos de e-mail, mídia removível e instalações de software quando autorizado.
- Procure tarefas agendadas, serviços, entradas de inicialização, chaves de execução do registro, persistência WMI e PowerShell incomum.
- Evite excluir evidências antes da preservação e coordenação.

# 8. Investigações de identidade

- Revise logins bem-sucedidos e com falha, eventos de MFA, dispositivo, localização, IP, agente do usuário, uso de token e detecções de risco.
- Compare com o padrão normal do usuário e viagens aprovadas ou uso de VPN.
- Verifique redefinições de senha, alterações de grupo, novas credenciais, regras de caixa de correio, concessões OAuth, atribuições de funções e atividades de contas de serviço.
- Trate viagens impossíveis como uma pista e não como uma prova automática; VPNs, redes móveis e serviços em nuvem podem distorcer a localização.
- Contenha revogando sessões, redefinindo credenciais, desabilitando contas ou removendo concessões somente quando autorizado.

# 9. Investigações de rede

- Comece com origem, destino, protocolo, porta, direção, bytes, duração e ação allow/block.
- Use DNS, proxy, firewall, VPN, Zeek, Suricata e dados de pacote juntos, quando disponíveis.
- Procure beacons incomuns, destinos raros, novos domínios, protocolos inesperados, movimentos laterais e grandes transferências de saída.
- Não rotule o tráfego como malicioso apenas porque uma porta é incomum. Valide o aplicativo e o contexto.
- As capturas de pacotes podem conter credenciais e dados pessoais; restringir o acesso e a retenção.

# 10. Investigações de e-mail e phishing

- Preserve a mensagem e os cabeçalhos originais.
- Revise o domínio do remetente, resposta, caminho de retorno, SPF, DKIM, DMARC, URLs, anexos, fraude de nome de exibição e roteamento de mensagens.
- Utilize um ambiente de análise seguro; nunca abra anexos suspeitos em uma estação de trabalho de produção.
- Procure outros destinatários e mensagens relacionadas.
- Determine se alguém clicou, inseriu credenciais, executou um arquivo ou aprovou a MFA.
- Bloqueie indicadores e remova mensagens somente dentro dos procedimentos autorizados.
- Comunique-se claramente com o usuário, sem culpa.

# 11. Investigações na nuvem

- Identifique a conta da nuvem, o locatário, subscription/project, o recurso, a identidade, a ação, o IP de origem, o agente do usuário e o horário.
- Revise alterações de IAM, novas chaves, exposição pública, alterações nas regras de rede, acesso ao armazenamento, criação incomum de computação e alterações no log de auditoria.
- Distinguir ações do plano de gestão de acesso a dados.
- Verifique a infraestrutura como código e os pipelines de implantação aprovados antes de presumir que a alteração foi feita por um ser humano.
- Preservar evidências de auditoria em nuvem e registrar identificadores de recursos.

# 12. MITRE ATT&CK e inteligência de ameaças

MITRE ATT&CK fornece uma linguagem comum para táticas e técnicas adversárias. Use-o para descrever o comportamento observado e identificar lacunas de detecção, e não para forçar todos os alertas a uma técnica. A inteligência contra ameaças acrescenta contexto, mas uma correspondência de indicadores é uma pista e não uma prova final.
- Fonte de registro, confiança, first/last visto, escopo e expiração dos indicadores.
- Prefira comportamento e múltiplos sinais corroborantes a uma única pontuação de reputação.
- Mapeie as detecções para técnicas ATT&CK e analise a cobertura honestamente.
- Remova ou expire indicadores obsoletos para reduzir o ruído.

# 13. Engenharia de detecção

1. Defina o comportamento da ameaça e a telemetria necessária.
1. Escreva uma hipótese analítica clara.
1. Crie a consulta ou regra e documente as suposições do campo.
1. Teste com dados simulados seguros e em boas condições.
1. Meça falsos positivos, pontos cegos, latência e custo.
1. Adicione gravidade, entidades, enriquecimento, orientação de resposta e mapeamento ATT&CK.
1. Versão da detecção e retenção de evidências de teste.
1. Sintonize com cuidado; não suprima um alerta apenas porque é inconveniente.
| Pergunta de qualidade de detecção | Exemplo |
| --- | --- |
| Especificidade | A regra identifica o comportamento em vez de apenas um nome de ferramenta comum? |
| Contexto | Considera a função do usuário, a criticidade dos ativos e a administração esperada? |
| Testabilidade | Um teste seguro pode reproduzir o sinal pretendido? |
| Acionabilidade | Um analista pode entender o que investigar a seguir? |
| Manutenibilidade | O proprietário, a versão, a fonte de dados e a data de revisão estão documentados? |

# 14. Caça a ameaças

A caça a ameaças é uma busca estruturada por atividades ainda não identificadas por alertas. Comece com uma hipótese baseada no comportamento da ameaça, no contexto comercial, na inteligência ou em uma lacuna de controle.
- Apresentar a hipótese e as evidências esperadas.
- Identificar fontes de dados e limitações.
- Execute pesquisas amplas e restrinja por tempo, entidade, raridade e sequência.
- Valide as descobertas com telemetria adicional.
- Documentar resultados negativos e pontos cegos.
- Converta descobertas repetíveis em detecções ou controles.

# 15. Resposta a incidentes

| Fase | Contribuição SOC |
| --- | --- |
| Preparação | Playbooks, contatos, ferramentas, acesso, registro, exercícios. |
| Detecção e análise | Validar, definir o escopo, classificar, preservar evidências, notificar. |
| Contenção | Recomendar ou executar isolamento, bloqueio e revogação de sessão aprovados. |
| Erradicação e recuperação | Apoie a remoção, restauração, validação e monitoramento aprimorado. |
| Lições aprendidas | Cronograma, causa raiz, lacunas de controle, métricas e ações atribuídas. |
> Não exceda sua autoridade. Um analista júnior que escala rapidamente com fortes evidências está tendo um desempenho correto.

# 16. Gerenciamento e relatórios de casos

- Use um título preciso com entidade e comportamento afetados.
- Escreva carimbos de data / hora com fuso horário.
- Separe fatos, suposições e conclusões.
- Registre cada consulta, fonte de evidência, ação e comunicação.
- Explique o impacto nos negócios em linguagem simples.
- Indique o que permanece desconhecido.
- Proteja dados pessoais e confidenciais.
- Use uma linguagem neutra e evite culpar os usuários.

## Exemplo de resumo do caso

Às 14h22 UTC, a plataforma de identidade registrou um login bem-sucedido para o usuário jdoe a partir de um endereço IP não associado anteriormente à conta. O MFA foi aprovado. Cinco minutos depois, uma nova regra de encaminhamento de caixa de correio foi criada. O usuário confirmou que não realizou nenhuma das ações. A conta foi desativada e as sessões foram revogadas de acordo com o manual de comprometimento de identidade. O caso foi escalado para revisão da caixa de correio e avaliação de notificação.

# 17. Laboratório doméstico e prática segura

- Use um laboratório virtual isolado sem rota para sistemas de produção.
- Use usuários e dados sintéticos. Nunca importe registros de empregadores ou clientes sem permissão.
- Tire fotos antes de testar.
- Utilizar sistemas intencionalmente vulneráveis ​​e plataformas de formação autorizadas.
- Não exponha os serviços do laboratório diretamente à internet.
- Mantenha amostras de malware fora de laboratórios para iniciantes, a menos que sejam supervisionadas e devidamente isoladas.
- Escopo do documento, controles de segurança e limpeza.

## Laboratório sugerido

- Uma máquina virtual Windows gerando logs de eventos.
- Uma máquina virtual Linux.
- Wazuh ou Elastic em um laboratório isolado ou em um ambiente de aprendizagem Sentinel controlado.
- Sysmon no Windows quando apropriado.
- Uma pequena coleção de eventos simulados seguros.
- Um repositório GitHub contendo consultas limpas, capturas de tela, notas de caso e lições aprendidas.

# 18. Projetos de portfólio

| Projeto | Entregáveis ​​|
| --- | --- |
| Investigação de phishing | Cabeçalhos higienizados, cronograma, indicadores, conclusão, recomendações de resposta. |
| Investigação de log do Windows | IDs de eventos, cronograma de processos, consultas, mapeamento ATT&CK, limitações. |
| Detecção SIEM | Regra, dados de teste, resultado esperado, análise falso-positiva, notas de ajuste. |
| Caça a ameaças | Hipóteses, fontes de dados, consultas, descobertas, lacunas, detecção proposta. |
| Relatório de incidente | Resumo executivo, cronograma técnico, impacto, contenção, lições aprendidas. |
| Painel SOC | Finalidade, fontes de dados, métricas, capturas de tela, considerações de privacidade. |
Nunca publique credenciais reais, dados de clientes, endereços IP internos, indicadores privados, regras proprietárias ou capturas de tela de produção não editadas.

# 19. Currículo e preparação para entrevista

- Descrever investigações com ações, evidências e resultados.
- Liste as plataformas honestamente e distinga a experiência de laboratório da experiência de produção.
- Mostre consultas, relatórios e detecções em um portfólio higienizado.
- Prepare-se para explicar um alerta desde o sinal inicial até a disposição final.
- Pratique a comunicação de incertezas e decisões de escalada.
- Não reivindique certificações, ferramentas ou experiência em incidentes que você não possui.

## Exemplo de marcadores de currículo

- Investigou alertas simulados de endpoint e identidade em um laboratório controlado, criou cronogramas a partir de várias fontes de log e documentou decisões de escalonamento.
- Criei e testei análises SIEM mapeadas para MITRE ATT&CK, incluindo análises de falsos positivos e notas de ajuste.
- Produziu relatórios higienizados de phishing e incidentes demonstrando o tratamento de evidências, comunicação de impacto nos negócios e recomendações de remediação.

## Perguntas comuns em entrevistas

- Acompanhe-me em seu processo de triagem de alertas.
- Como você distingue um falso positivo de um verdadeiro positivo benigno?
- Quais registros você usaria para suspeita de comprometimento da conta?
- Como você investigaria um alerta suspeito do PowerShell?
- Quando você escalaria um incidente?
- Como você lida com a falta de telemetria?
- Descreva uma detecção que você criou ou melhorou.
- Como você protege a privacidade durante uma investigação?

# 20. Plano de aprendizagem 30/60/90-day

## Dias 1 a 30: fundações

- Estude redes, Windows, Linux, identidade e ataques comuns.
- Aprenda a sintaxe básica de consulta em um SIEM.
- Conclua investigações simples de registro e phishing.
- Criar um glossário e um caderno de investigação.
- Publicar um relato de caso higienizado.

## Dias 31-60: investigação

- Pratique cronogramas de endpoint, identidade, rede e nuvem.
- Mapear observações para ATT&CK.
- Construa duas detecções básicas com evidências de teste.
- Complete um exercício de caça a ameaças.
- Pratique mensagens de escalonamento concisas.

## Dias 61-90: preparação para o trabalho

- Conclua três projetos de portfólio.
- Revise dez descrições de cargos e identifique habilidades recorrentes.
- Adapte o currículo sem exageros.
- Praticar entrevistas técnicas e comportamentais.
- Aplicar-se a funções de SOC, monitoramento de segurança, resposta a incidentes e detecção júnior que correspondam à localização e à autorização de trabalho.

# 21. Acessibilidade e aprendizagem sustentável

- Use transcrições de texto, legendas, laboratórios acessíveis por teclado, documentos fáceis de ler na tela e tamanho de texto ajustável.
- Divida as investigações em listas de verificação repetíveis.
- Use modelos para reduzir a carga da memória de trabalho.
- Solicite acomodações razoáveis ​​para entrevistas, treinamento e trabalho.
- Programe pausas durante longas filas de alerta e investigações emocionalmente difíceis.
- Um bom analista é medido pelo julgamento, evidências e comunicação - não pela velocidade de digitação ou memorização de cada comando.

# 22. Listas de verificação e modelos

## Lista de verificação de triagem de alerta

- Lógica de alerta compreendida
- Fuso horário confirmado
- Entidades identificadas
- Contexto de ativo e usuário adicionado
- Completude da telemetria verificada
- Linha do tempo construída
- Alertas relacionados pesquisados
- Hipóteses testadas
- Disposição selecionada
- Ações e evidências documentadas
- Escalação ou encerramento aprovado
- Feedback de detecção registrado

## Modelo de nota de investigação

| Campo | Conteúdo |
| --- | --- |
| ID do caso |  |
| Alerta/hipótese |  |
| Data e analista |  |
| Usuários e ativos afetados |  |
| Fatos conhecidos |  |
| Linha do tempo |  |
| Consultas e evidências |  |
| Avaliação e confiança |  |
| Acções tomadas |  |
| Perguntas restantes |  |
| Escalação/encerramento |  |

# 23. Glossário

| Prazo | Definição |
| --- | --- |
| Alerta | Um sinal gerado por uma regra, análise, produto ou controle que requer revisão. |
| Caso/incidente | Um registro gerenciado que combina evidências, análises, decisões e respostas. |
| EDR | Detecção e resposta de endpoint. |
| Falso positivo | Um alerta que indica incorretamente o comportamento direcionado. |
| Benigno verdadeiro positivo | A regra observou corretamente o comportamento, mas a atividade foi autorizada ou inofensiva. |
| COI | Indicador de comprometimento, como hash, domínio, IP ou artefato. |
| SIEM | Informações de segurança e gerenciamento de eventos. |
| VOAR | Orquestração, automação e resposta de segurança. |
| Triagem | Validação inicial, enriquecimento, priorização e disposição. |
| Caça a ameaças | Pesquisa baseada em hipóteses para comportamento malicioso não detectado. |

# 24. Recursos oficiais de aprendizagem

Microsoft Sentinela
MITRE ATT&CK
Resposta a incidentes CISA
Segurança Elástica
Guia de início rápido do Wazuh
Segurança Corporativa Splunk
Sigma
YARA
Wireshark
Cebola de segurança
Ciberdefensores
Vamos defender
Laboratórios da Equipe Azul Online
Treinamento Microsoft Learn Sentinel
Verifique a disponibilidade, os preços, o acesso regional e o comportamento atual do produto antes de confiar em qualquer plataforma externa. As interfaces e o licenciamento dos produtos podem mudar.

# Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob Creative Commons Atribuição-NãoComercial-Compartilhamento pela mesma Licença 4.0 Internacional (CC BY-NC-SA 4.0).
