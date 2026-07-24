# Segurança prática do Azure AI

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.


## Como proteger Microsoft Foundry, Copilot, Purview, Entra ID, RAG, Agents e MCP

**Autor:** Alberto (Al) Leiva  
**Versão:** 1.0 - julho de 2026  
**Licença:** CC BY-NC-SA 4.0
> A segurança humana está em primeiro lugar. Nenhum teste de segurança, prazo de implantação, objetivo comercial ou experimento técnico é mais importante do que a segurança, a dignidade, a privacidade e os direitos das pessoas afetadas por um sistema de IA.

## Conteúdo

1. Fundamentos de segurança da IA do Azure
2. Responsabilidade compartilhada e modelagem de ameaças
3. Arquitetura de referência segura
4. Identidade e acesso com Microsoft Entra ID
5. Isolamento de rede e conectividade privada
6. Proteção de dados com Microsoft Purview
7. Segurança do projeto Microsoft Foundry
8. Protegendo modelos, prompts e conteúdo
9. Sistemas RAG seguros
10. Agentes de IA e identidades não humanas
11. Servidor MCP e segurança de ferramentas
12. Segurança e governança co-piloto
13. Defender for Cloud e gerenciamento contínuo de postura
14. Teste, avaliação e equipe vermelha
15. Registro, monitoramento e resposta a incidentes
16. Governança, conformidade e evidências de auditoria
17. Roteiro de implementação prática
18. Lista de verificação de prontidão de produção
19. Glossário
20. Referências oficiais

## 1. Fundamentos de segurança da IA ​​do Azure

Uma solução Azure AI normalmente inclui identidades, aplicações, redes, avisos, fontes de dados, índices de pesquisa, armazenamento, APIs, agentes, ferramentas, monitorização e pontos de decisão humanos. Proteja todo o sistema, não apenas o modelo.
Princípios fundamentais:
- Faça um inventário de todos os ativos e proprietários de IA.
- Use o Microsoft Entra ID e identidades gerenciadas em vez de segredos de longa duração sempre que houver suporte.
- Aplicar o mínimo de privilégios no âmbito prático mais restrito.
- Use conectividade privada e acesso de saída controlado para cargas de trabalho confidenciais.
- Classifique e proteja os dados antes de conectá-los à IA.
- Trate os prompts, o conteúdo recuperado, as ferramentas e a saída do modelo como não confiáveis.
- Teste antes do lançamento e após alterações significativas.
- Monitorar continuamente e reter evidências.

## 2. Responsabilidade compartilhada e modelagem de ameaças

Os clientes continuam responsáveis ​​pela configuração, identidades, aplicativos, dados, prompts, permissões de ferramentas, monitoramento, governança e decisões tomadas com resultados de IA.
Perguntar:
- Quem pode enviar prompts, fazer upload de arquivos, implantar modelos, alterar configurações ou invocar ferramentas?
- Quais dados confidenciais podem inserir prompts, índices, logs, saídas ou avaliações?
- O que acontece se o conteúdo recuperado contiver instruções ocultas?
- O modelo pode modificar registros, enviar mensagens, executar códigos ou aprovar transações?
- Qual é o raio máximo de explosão de uma identidade, agente, índice ou segredo comprometido?

## 3. Arquitetura de referência segura

Utilize Entra ID, Azure RBAC, identidades geridas, pontos finais privados, DNS privado, saída controlada, fontes de dados protegidas, controlos de conteúdo, Purview, Defender for Cloud e monitorização centralizada.

## 4. Identidade e acesso com Microsoft Entra ID

- Exigir MFA e acesso condicional para usuários humanos.
- Use o Privileged Identity Management para administração por tempo limitado.
- Separe a administração da produção das contas diárias.
- Prefira identidades gerenciadas para cargas de trabalho hospedadas no Azure.
- Use a federação de identidade de carga de trabalho para CI/CD compatíveis e cargas de trabalho externas.
- Evite atribuições amplas em nível de assinatura.
- Revise as permissões do plano de gerenciamento e do plano de dados.

## 5. Isolamento de rede

- Desative o acesso à rede pública sempre que for prático.
- Use endpoints privados para Foundry, armazenamento, pesquisa, Key Vault e bancos de dados.
- Validar DNS privado.
- Rota de saída através de controles aprovados.
- Permitir apenas destinos obrigatórios.
- Revise toda a cadeia de dependências.

## 6. Visão da Microsoft

Use o Purview para descobrir dados confidenciais, aplicar rótulos, impor DLP, investigar atividades arriscadas e avaliar a postura de segurança de dados relacionada à IA.
Fluxo de trabalho:
1. Solicitação de inventário, aterramento, ajuste fino, avaliação e registro de dados.
2. Classificar dados e identificar requisitos legais ou contratuais.
3. Aplique controles de acesso e rótulos de confidencialidade.
4. Configure o DLP.
5. Usar os recursos atuais do DSPM para identificar uso arriscado de IA e dados desprotegidos.
6. Registrar exceções e controles compensatórios.

## 7. Segurança do projeto Microsoft Foundry

- Desenvolvimento, teste e produção separados.
- Use infraestrutura como código.
- Restringir permissões de implantação, conexão e publicação de agentes.
- Use chaves gerenciadas pelo cliente quando a política exigir e o serviço oferecer suporte a elas.
- Habilite as configurações de diagnóstico.
- Aplique tags, políticas, cotas, limites de taxas e orçamentos.
- Armazene segredos inevitáveis ​​no Key Vault.

## 8. Modelos, prompts e conteúdo

Camada de defesas de injeção imediata:
- Instruções do sistema separadas, entrada do usuário, conteúdo recuperado e resultados da ferramenta.
- Trate o conteúdo recuperado como dados e não como instruções confiáveis.
- Use ferramentas com menos privilégios.
- Validar parâmetros estruturados da ferramenta.
- Use proteções de segurança de conteúdo e contra ataques imediatos, quando apropriado.
- Exigir confirmação ou aprovação para ações de alto impacto.
- Teste cenários de jailbreak, injeção indireta e exfiltração.

## 9. RAG seguro

- Aplicar autorização no momento da consulta.
- Preservar permissões de origem.
- Use recorte de segurança.
- Separar inquilinos ou classificações quando necessário.
- Digitalize e valide arquivos.
- Rastrear procedência.
- Limitar o contexto recuperado.
- Retornar citações.
- Monitorar enumeração e padrões de recuperação incomuns.

## 10. Agentes e identidades não humanas

Dê a cada agente de produção uma identidade exclusiva, quando houver suporte. Ferramentas separadas somente leitura e com capacidade de gravação. Imponha a autorização no código do aplicativo e nos sistemas de destino. O modelo pode propor uma ação, mas a lógica confiável deve autorizá-la.

## 11. Segurança MCP

- Inventário de servidores e proprietários MCP aprovados.
- Autenticar e criptografar conexões.
- Use autorização por ferramenta.
- Validar esquemas e parâmetros.
- Ferramentas e destinos da lista de permissões.
- Execute com permissões mínimas.
- Desenvolvimento e produção separados.
- Registrar e correlacionar todas as chamadas de ferramentas.
- Exigir aprovação para ações de alto impacto.
- Retorne apenas os dados mínimos necessários.

## 12. Governança do copiloto

Corrija dados compartilhados em excesso e permissões excessivas antes da implantação ampla. Aplique rótulos e DLP, controle plug-ins e agentes, treine usuários, revise sinais de auditoria e avalie riscos junto com a adoção.

## 13. Defender para nuvem

Use o Defender for Cloud para descoberta de carga de trabalho de IA compatível, recomendações de postura, análise de caminho de ataque e proteção contra ameaças em tempo de execução. Atribua descobertas aos proprietários, integre alertas em fluxos de trabalho de incidentes e valide a cobertura após alterações.

## 14. Testes e red teaming

Teste o controle de acesso, ataques imediatos, vazamento de dados, integridade RAG, ferramentas de agente, segurança de aplicativos, abuso, disponibilidade e fatores humanos. Registre o comportamento esperado, os resultados reais, as versões, a gravidade, os proprietários e as evidências de reteste.

## 15. Monitoramento e resposta a incidentes

Identidades de log, alterações administrativas, metadados de invocação, chamadas de ferramentas, bloqueios de políticas, autorização de recuperação, cotas e alertas de segurança. Evite reter avisos totalmente confidenciais por padrão.
Etapas do incidente:
1. Identifique e classifique.
2. Conter identidades, ferramentas, endpoints ou agentes afetados.
3. Preservar evidências.
4. Avalie a exposição e os danos.
5. Revogue credenciais e corrija permissões.
6. Remova o conteúdo envenenado e reconstrua os índices, se necessário.
7. Controles de patches.
8. Notifique as partes necessárias.
9. Teste novamente.
10. Documente as lições aprendidas.

## 16. Governança e evidências de auditoria

Manter:
- Inventário de IA
- Proprietários nomeados
- Finalidade aprovada e usos proibidos
- Arquitetura e diagrama de fluxo de dados
- Avaliações de privacidade e risco
- Modelo de ameaça
- Documentação de fornecedor e modelo
- Plano de controle de segurança
- Resultados da avaliação
- Projeto de supervisão humana
- Monitoramento e plano de incidentes
- Registro de alterações
- Plano de aposentadoria

## 17. Roteiro de 30/60/90 dias

### Primeiros 30 dias

Os sistemas de inventário identificam a exposição e privilégios excessivos, permitem o registro e a visibilidade básica, removem recursos abandonados e criam um padrão mínimo.

### Dias 31-60

Mude para identidades gerenciadas, restrinja o RBAC, implemente conectividade privada, classifique dados, configure DLP prioritário, agentes de modelo de ameaça e RAG e corrija descobertas de alto risco.

### Dias 61-90

Automatize políticas e evidências, integre alertas, estabeleça revisões periódicas, defina métricas executivas e treine as partes interessadas.

## 18. Lista de verificação de prontidão de produção

- [] Proprietários nomeados
- [ ] Finalidade aprovada e usos proibidos
- [] Classificação de dados
- [] Modelo de ameaça
- [] Autenticação de entrada
- [] Identidades gerenciadas
- [] RBAC com menor privilégio
- [] Exposição de rede revisada
- [] Endpoints privados testados
- [] Key Vault usado para segredos inevitáveis
- [] Controles de alcance definidos
- [] Corte de segurança RAG testado
- [] Ferramentas de agente e MCP permitidas
- [ ] Aprovação para ações de alto impacto
- [] Controles de prompt e conteúdo testados
- [] Defender e monitoramento ativados
- [] Manual de incidentes exercido
- [] Reversão e desligamento testados
- [] Acessibilidade e supervisão humana revisadas
- [] Aprovação de segurança registrada

## 19. Glossário

- **Agente:** componente de IA que pode recuperar informações, chamar ferramentas e executar ações.
- **DSPM:** Gerenciamento de Postura de Segurança de Dados.
- **Foundry:** plataforma Microsoft Azure para criar e operar aplicativos e agentes de IA.
- **Identidade gerenciada:** identidade de carga de trabalho gerenciada pelo Azure.
- **MCP:** Protocolo de Contexto do Modelo.
- **Injeção de prompt:** Entrada projetada para substituir instruções, expor dados ou usar ferramentas indevidamente.
- **RAG:** Geração aumentada por recuperação.
- **Recorte de segurança:** Filtragem do conteúdo recuperado de acordo com a autorização do usuário.

## 20. Referências oficiais

- [Práticas recomendadas de segurança da IA do Azure](https://learn.microsoft.com/azure/security/fundamentals/ai-security-best-practices)
- [Linha de base de segurança do Azure para Microsoft Foundry](https://learn.microsoft.com/security/benchmark/azure/baselines/azure-ai-foundry-security-baseline)
- [Isolamento de rede do Microsoft Foundry](https://learn.microsoft.com/azure/foundry/how-to/configure-private-link)
- [RBAC do Microsoft Foundry](https://learn.microsoft.com/azure/foundry/concepts/rbac-foundry)
- [Identidades gerenciadas](https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/overview)
- [ID da carga de trabalho do Microsoft Entra](https://learn.microsoft.com/entra/workload-id/workload-identities-overview)
- [Proteções do Microsoft Purview para IA](https://learn.microsoft.com/purview/ai-microsoft-purview)
- [DSPM para IA](https://learn.microsoft.com/purview/dspm-for-ai)
- [Postura de segurança do Defender para Cloud AI](https://learn.microsoft.com/azure/defender-for-cloud/ai-security-posture)
- [Defender para proteção contra ameaças de IA na nuvem](https://learn.microsoft.com/azure/defender-for-cloud/ai-threat-protection)
- [Segurança de conteúdo de IA do Azure](https://learn.microsoft.com/azure/ai-services/content-safety/overview)
- [Serviço do Agente Microsoft Foundry](https://learn.microsoft.com/azure/foundry/agents/overview)
Copyright © 2026 Alberto (Al) Leiva.
