# Como proteger agentes de IA, sistemas RAG e servidores MCP

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

Um manual prático de segurança para IA agente, geração aumentada de recuperação, ferramentas, memória, identidades e supervisão humana
Alberto (Al) Leiva
Versão 1.0 - julho de 2026
A segurança humana está em primeiro lugar. Este manual destina-se ao uso legal, autorizado e defensivo. Os agentes de IA podem atuar em sistemas reais. Sempre teste em ambientes aprovados e exija supervisão humana para ações de alto impacto.

## 1. O que este manual protege

- Agentes de IA que planejam, raciocinam, chamam ferramentas e executam ações.
- Pipelines RAG que recuperam documentos corporativos ou conteúdo de banco de dados.
- Hosts MCP, clientes, servidores, ferramentas, prompts e recursos.
- Memória do agente, estado da tarefa, credenciais, logs e fluxos de trabalho de aprovação.
- Sistemas monoagentes e multiagentes.

## 2. Princípios básicos de segurança

- O modelo propõe; a lógica do aplicativo confiável autoriza.
- Trate a entrada do usuário, o conteúdo recuperado, a saída da ferramenta e a memória como não confiáveis.
- Use identidades de carga de trabalho exclusivas e com menos privilégios.
- Recursos separados de leitura, gravação, execução e administração.
- Exigir confirmação explícita para ações confidenciais.
- Registrar ações sem reter desnecessariamente conteúdo confidencial.
- Projete para falha segura, reversão, desligamento e recuperação.

## 3. Arquitetura de referência

- O usuário ou o aplicativo de chamada é autenticado por meio de um provedor de identidade aprovado.
- Uma camada de orquestração valida entradas, aplica políticas e rastreia a sessão do usuário.
- O agente recebe apenas as ferramentas e dados necessários para a tarefa atual.
- A recuperação RAG impõe permissões de origem no momento da consulta.
- Os clientes MCP conectam-se apenas a servidores aprovados usando transporte autenticado e criptografado.
- Chamadas de ferramentas de alto impacto passam por portas determinísticas de autorização e aprovação.
- Acompanhamento de registros de identidade, decisão, ferramenta, parâmetros, resultado e aprovação.

## 4. IA agente de modelagem de ameaças

- Mapeie usuários, agentes, modelos, armazenamentos de memória, índices RAG, ferramentas, servidores MCP e serviços externos.
- Identifique todos os limites de confiança e todos os locais onde as instruções podem entrar.
- Documente o que cada ferramenta pode ler, modificar, executar, excluir, enviar, comprar ou aprovar.
- Estime o raio de explosão de uma identidade de agente comprometida ou memória envenenada.
- Identificar pessoas que possam ser prejudicadas por ações incorretas, tendenciosas, enganosas ou não autorizadas.

## 5. Identidade e autorização

- Dê a cada agente de produção ou serviço uma identidade única, quando houver suporte.
- Prefira tokens de curta duração, identidades gerenciadas, federação de identidade de carga de trabalho ou acesso baseado em OAuth.
- Não use uma credencial de administrador compartilhada entre agentes.
- Autorize cada chamada de ferramenta na lógica da aplicação e no serviço de destino.
- Vincule o usuário humano iniciador à ação para que o agente não possa exceder os direitos desse usuário.
- Revise regularmente identidades, permissões e credenciais inativas.

## 6. Segurança da ferramenta e controles de ação

- Use listas de permissões para ferramentas, métodos, destinos, caminhos de arquivos e classes de dados.
- Valide argumentos estruturados em relação a esquemas estritos.
- Rejeite campos inesperados, ações ambíguas, fragmentos de comando e caminhos inseguros.
- Aplique limites de taxa, tempos limite, limites de tamanho de saída e limites de transação.
- Use os modos de simulação ou visualização antes de alterações destrutivas.
- Exigir aprovação humana para ações financeiras, jurídicas, de pessoal, de segurança, de exclusão e de alteração de privilégios.
- Impedir que o modelo altere suas próprias permissões ou regras de aprovação.

## 7. Protegendo RAG

- Imponha a autorização no momento da consulta, não apenas quando os documentos são indexados.
- Preservar os controles de acesso à origem e usar cortes de segurança.
- Rastreie a procedência, o proprietário, a classificação, a data de atualização e o status de retenção.
- Digitalize uploads e rejeite tipos de arquivos não suportados ou perigosos.
- Trate as passagens recuperadas como dados em vez de instruções confiáveis.
- Limite o contexto recuperado e exija citações.
- Detecte conteúdo envenenado, injeção indireta de prompt, permissões obsoletas e vazamento entre locatários.
- Remova imediatamente o conteúdo excluído ou revogado dos índices.

## 8. Protegendo memória e estado

- Separe o estado de conversação de curto prazo da memória durável.
- Armazene apenas as informações necessárias para uma finalidade aprovada.
- Não coloque segredos, credenciais irrestritas ou dados pessoais confidenciais na memória do agente.
- Identifique a memória com origem, proprietário, classificação, confiança e expiração.
- Exigir validação antes que a memória possa influenciar uma ação de alto impacto.
- Fornece mecanismos para inspecionar, corrigir e excluir memória armazenada.

## 9. Segurança MCP

- Manter um inventário aprovado de servidores MCP, proprietários, versões e finalidades comerciais.
- Use conexões autenticadas e criptografadas.
- Implemente o OAuth 2.1 ou outro método de autorização aprovado para servidores remotos.
- Não utilize identificadores de sessão como autenticação.
- Use identificadores de sessão seguros e não previsíveis e verifique cada solicitação recebida.
- Valide todas as entradas da ferramenta, aplique controle de acesso, limite de taxa de chamadas e higienize as saídas.
- Mostre aos usuários entradas confidenciais da ferramenta antes da execução e obtenha confirmação.
- Valide os resultados da ferramenta antes de serem repassados ​​ao modelo.
- Fixe dependências e monitore servidores MCP de terceiros em busca de alterações inesperadas.

## 10. Injeção imediata e envenenamento por ferramenta

- Instruções separadas do sistema, instruções do usuário, conteúdo recuperado, memória e saída da ferramenta.
- Nunca permita que documentos ou descrições de ferramentas redefinam políticas silenciosamente.
- Trate os metadados da ferramenta e as descrições fornecidas pelo servidor como potencialmente maliciosos.
- Detecte tentativas de revelar segredos, invocar ferramentas ocultas, ignorar aprovações ou redirecionar dados.
- Use verificações de políticas independentes que não podem ser substituídas por texto em linguagem natural.
- Teste cenários de injeção direta, injeção indireta, envenenamento de descrição de ferramenta, envenenamento de memória e puxão de tapete.

## 11. Sistemas multiagentes

- Defina qual agente tem permissão para delegar, aprovar ou encerrar trabalho.
- Evite o acúmulo de privilégios quando um agente liga para outro.
- Autentique mensagens entre agentes e preserve o contexto original do usuário.
- Limite a recursão, a profundidade da tarefa, o uso de tokens, as chamadas de ferramentas e o tempo decorrido.
- Detecte instruções conflitantes e fluxos de trabalho circulares.
- Fornece uma parada de emergência que interrompe todo o fluxo de trabalho.

## 12. Supervisão humana e acessibilidade

- Apresentar ações propostas, recursos afetados, parâmetros, impacto esperado e opções de reversão.
- Use linguagem simples e telas de confirmação acessíveis.
- Não use padrões escuros ou urgência enganosa.
- Permita que os usuários contestem, corrijam ou apelem de resultados importantes.
- Fornecer fluxos de trabalho alternativos para pessoas que usam tecnologia assistiva.
- Exigir revisão humana treinada onde os erros possam afetar materialmente os direitos, a segurança, o emprego, as finanças ou o acesso aos serviços.

## 13. Registro, monitoramento e detecção

- Registre o usuário inicial, a identidade do agente, a versão do modelo ou configuração, a ferramenta, os parâmetros, o resultado, a aprovação e o carimbo de data/hora.
- Monitore sequências de ferramentas incomuns, negações repetidas, recuperação de alto volume, alterações de privilégios e novos servidores MCP.
- Alerta sobre acesso a dados confidenciais, proteções desativadas, destinos de rede inesperados e grandes transferências de saída.
- Proteja os logs contra alterações e defina a retenção com base nos requisitos de risco e privacidade.
- Evite armazenar prompts e resultados completos, a menos que haja necessidade justificada.

## 14. Testes e red teaming

- Teste somente com autorização por escrito e escopo definido.
- Teste o vazamento de dados entre usuários e locatários.
- Teste a injeção imediata direta e indireta.
- Uso indevido de ferramentas de teste, manipulação de parâmetros, injeção de comandos e delegação não autorizada.
- Teste memória envenenada, documentos envenenados, descrições de ferramentas maliciosas e servidores MCP comprometidos.
- Teste de negação de serviço, loops não controlados, amplificação de custos e autonomia excessiva.
- Registre o comportamento esperado, o comportamento real, a gravidade, o proprietário, a correção e as evidências de reteste.

## 15. Resposta a incidentes

- Desabilite o agente, ferramenta, servidor MCP, identidade ou conector afetado.
- Preservar logs, estado da memória, prompts, fontes recuperadas, resultados de ferramentas e versões de configuração.
- Revogar tokens e girar segredos.
- Remova conteúdo envenenado e reconstrua índices ou armazenamentos de memória quando necessário.
- Avalie ações não autorizadas, exposição de dados e impacto nas pessoas.
- Notifique o departamento jurídico, de privacidade, conformidade, clientes ou reguladores de acordo com a política e a lei.
- Teste novamente os controles antes de restaurar o serviço.

## 16. Governança e evidências

- Manter um inventário de agentes, sistemas RAG, servidores MCP, ferramentas, proprietários, dados e níveis de risco.
- Documentar a finalidade aprovada, usos proibidos, supervisão humana e autoridade de desligamento.
- Manter diagramas de arquitetura, diagramas de fluxo de dados, modelos de ameaças, avaliações e aceitações de riscos.
- Revise fornecedores, componentes de código aberto, fornecedores de modelos e servidores MCP.
- Mapear controles para NIST AI RMF, NIST CSF, orientação OWASP e requisitos organizacionais aplicáveis.

## 17. Plano de implementação 30/60/90-day

- Dias 1 a 30: inventariar sistemas, identificar proprietários, remover agentes e servidores abandonados, ativar logs e bloquear acesso público ou excessivo.
- Dias 31 a 60: implementar identidades exclusivas, privilégios mínimos, corte de segurança RAG, autorização MCP, listas de permissões de ferramentas e portas de aprovação.
- Dias 61-90: realizar testes contraditórios, integrar monitoramento, exercitar resposta a incidentes, automatizar evidências e estabelecer revisões periódicas.

## 18. Lista de verificação de prontidão de produção

☐ Proprietários comerciais e técnicos nomeados
☐ Finalidade aprovada e usos proibidos
☐ Agente, RAG, MCP, ferramentas e inventário de dados
☐ Modelo de ameaça revisado
☐ Identidades únicas e menos privilégios
☐ Autorização RAG em tempo de consulta testada
☐ Autorização MCP e sessões seguras
☐ Esquemas de ferramentas, listas de permissões e limites
☐ Aprovação humana para ações de alto impacto
☐ Testes de injeção imediata e envenenamento
☐ Registros, alertas e controles de privacidade
☐ Parada de emergência e reversão testada
☐ Resposta a incidentes exercida
☐ Acessibilidade e recurso revisados
☐ Aprovação final de segurança registrada

## 19. Exemplo de registro de risco

## 20. Referências oficiais

- Ameaças e mitigações de IA agente OWASP: https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/
- Guia de proteção de aplicativos Agentic OWASP: https://genai.owasp.org/resource/securing-agentic-applications-guide-1-0/
- OWASP Top 10 para aplicações Agentic 2026: https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/
- Práticas recomendadas de segurança do protocolo de contexto do modelo: https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices
- Autorização MCP: https://modelcontextprotocol.io/docs/tutorials/security/authorization
- Considerações de segurança da ferramenta MCP: https://modelcontextprotocol.io/specification/2025-06-18/server/tools
- NIST AI RMF: https://www.nist.gov/itl/ai-risk-management-framework
- Perfil de IA generativo NIST AI RMF: https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence
- Planejamento de segurança da Microsoft para aplicativos LLM: https://learn.microsoft.com/ai/playbook/technology-guidance/generative-ai/mlops-in-openai/security/security-plan-llm-application

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
| Risco | Impacto | Controles | Proprietário |
|---|---|---|---|
| Documento RAG envenenado altera comportamento do agente | Divulgação de dados ou uso não autorizado de ferramentas | Validação de fonte, separação de instruções, autorização em tempo de consulta, testes | Proprietário da plataforma de IA |
| Servidor MCP de terceiros altera comportamento da ferramenta | Transferência inesperada de dados ou ação destrutiva | Inventário aprovado, fixação de versão, autorização, validação de saída, monitoramento | Proprietário da Integração |
| Agente usa privilégios excessivos | Grande raio de explosão | Identidade única, privilégio mínimo, portas de aprovação, revisão periódica | Engenharia de Segurança |
