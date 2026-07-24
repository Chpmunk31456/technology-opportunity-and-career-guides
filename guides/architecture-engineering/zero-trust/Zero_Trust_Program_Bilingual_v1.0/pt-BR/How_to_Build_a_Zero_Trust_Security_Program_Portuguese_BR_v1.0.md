# Como construir um programa de segurança Zero Trust

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

Um guia prático para identidade, dispositivos, redes, aplicativos, dados, cargas de trabalho, visibilidade, automação e governança
Alberto (Al) Leiva
Versão 1.0 - julho de 2026
A segurança humana está em primeiro lugar. A Zero Trust deve reduzir o risco sem criar barreiras desnecessárias de vigilância, discriminação ou acessibilidade.

## 1. O que significa Confiança Zero

- Zero Trust é um conjunto de princípios e uma abordagem de arquitetura empresarial, não um único produto.
- Não conceda confiança implícita devido à localização da rede, propriedade do dispositivo, cargo ou login anterior bem-sucedido.
- Avaliar continuamente sinais de identidade, dispositivo, aplicativo, dados, comportamento e ambiente.
- Proteja recursos individuais com decisões políticas explícitas e privilégios mínimos.

## 2. Resultados de negócios e governança

- Conectar o programa à resiliência empresarial, proteção de dados, trabalho remoto, adoção da nuvem, deveres regulatórios e contenção de incidentes.
- Criar patrocínio executivo, um grupo diretor multifuncional, proprietários de pilares responsáveis ​​e um processo de decisão documentado.
- Definir escopo, prioridades, financiamento, dependências, aceitação de riscos, exceções e resultados mensuráveis.
- Evite tratar o Zero Trust como um projeto apenas de rede ou apenas de identidade.

## 3. Arquitetura lógica NIST

- O Policy Engine decide se o acesso deve ser concedido, negado ou limitado.
- O Administrador da Política estabelece ou encerra a conexão de acordo com a decisão.
- O Policy Enforcement Point permite, monitora e encerra o acesso entre um sujeito e um recurso.
- As decisões políticas devem utilizar dados de identidade, dispositivos, recursos, ameaças, comportamento e políticas organizacionais.

## 4. Descoberta do estado atual

- Inventariar usuários, contas privilegiadas, contas de serviço, cargas de trabalho, dispositivos, aplicativos, repositórios de dados, redes, APIs, SaaS, recursos de nuvem, OT/ICS e terceiros.
- Mapear serviços comerciais críticos e suas dependências.
- Identifique autenticação legada, credenciais compartilhadas, dispositivos não gerenciados, exposição pública, redes planas, privilégios excessivos e fluxos de dados não monitorados.
- Registre a propriedade da tecnologia, o status do ciclo de vida e a aposentadoria planejada.

## 5. Proteja identidades

- Use MFA resistente a phishing para acesso privilegiado e de alto risco sempre que possível.
- Aplicar políticas de acesso baseadas em riscos e sensíveis ao contexto.
- Use gerenciamento de acesso privilegiado, elevação just-in-time, contas administrativas separadas e aprovação para funções confidenciais.
- Gerencie identidades não humanas, segredos, certificados, chaves de API e identidades de carga de trabalho com a mesma disciplina das contas humanas.
- Remova contas inativas e revise os direitos regularmente.

## 6. Dispositivos e endpoints seguros

- Exigir inventário de dispositivos, propriedade, sistemas operacionais suportados, criptografia, configuração segura, proteção de endpoint e aplicação de patches em tempo hábil.
- Use a integridade e a conformidade do dispositivo como sinais de acesso.
- Políticas separadas corporativas, pessoais, contratantes, compartilhadas, de servidor, móveis e de dispositivos especializados.
- Fornecer alternativas restritas para usuários que não podem usar um dispositivo gerenciado padrão.
- Isole ou corrija dispositivos que se tornem arriscados durante uma sessão.

## 7. Proteja redes e ambientes

- Reduza a dependência de uma rede interna confiável.
- Segmente por serviço de negócios, sensibilidade, carga de trabalho e risco, em vez de apenas por VLANs amplas.
- Use conexões criptografadas, proxies autenticados, controles com reconhecimento de aplicativos, proteção DNS e saída controlada.
- Limitar o movimento lateral e as vias administrativas.
- Proteja conexões remotas, de filiais, de nuvem, de data center, OT/ICS e de parceiros.

## 8. Proteja aplicativos e cargas de trabalho

- Inventário de aplicativos, proprietários, métodos de autenticação, dados, integrações, dependências de software e caminhos de implantação.
- Modernize aplicativos legados por meio de gateways, proxies, segmentação ou controles de compensação.
- Use identidades de carga de trabalho e credenciais de curta duração.
- Aplique desenvolvimento seguro, verificação de dependências, assinatura de código, gerenciamento de segredos, proteção de tempo de execução e controle de alterações.
- Autorize o acesso à API e serviço a serviço em cada solicitação.

## 9. Proteja os dados

- Descubra, classifique, rotule e atribua propriedade a dados confidenciais.
- Aplique privilégios mínimos, criptografia, prevenção contra perda de dados, retenção, exclusão e gerenciamento de direitos.
- Utilizar a sensibilidade dos dados como entrada para decisões de acesso.
- Monitore downloads incomuns, acesso em massa, compartilhamento externo e tentativas de contornar controles.
- Impedir que ambientes inferiores recebam dados de produção irrestritos.

## 10. Visibilidade, análise e detecção

- Centralize identidade, endpoint, aplicativo, nuvem, rede, dados e telemetria administrativa.
- Normalize tempo, identidade, dispositivo, recurso e contexto de sessão.
- Detecte viagens impossíveis, abuso de token, uso anômalo de privilégios, dispositivos arriscados, movimentos laterais e acesso incomum a dados.
- Proteja os logs contra alterações e defina a retenção com base no risco e na privacidade.
- Crie ciclos de feedback para que os incidentes melhorem as políticas.

## 11. Automação e orquestração

- Automatize o enriquecimento de rotina, pontuação de risco, contenção, revogação de credenciais, isolamento de dispositivos e criação de tickets.
- Exigir aprovação humana para ações com impacto material nos negócios, jurídico, segurança ou disponibilidade.
- Teste a automação em etapas e forneça procedimentos de reversão e parada de emergência.
- Evite que a automação amplifique um falso positivo em toda a empresa.

## 12. Terceiros e acesso remoto

- Use acesso baseado em identidade e específico de aplicativo, em vez de acesso amplo à rede, sempre que possível.
- Exigir contas nomeadas, MFA, dispositivos gerenciados ou verificados, limites de tempo, monitoramento de sessão e aprovação do patrocinador.
- Restringir os fornecedores aos sistemas e horários exigidos.
- Remova o acesso imediatamente no final do contrato ou mudança de função.
- Incluir responsabilidades de Zero Trust em contratos e procedimentos de incidentes.

## 13. TO, ICS, IoT e sistemas legados

- Priorize segurança e disponibilidade.
- Use a descoberta passiva onde a verificação ativa puder interromper as operações.
- Segmente zonas e conduítes, restrinja o acesso remoto, monitore o comportamento do protocolo e proteja estações de trabalho de engenharia.
- Use hosts de salto, gateways unidirecionais, listas de permissões, controles de compensação e janelas de manutenção planejada.
- Não force controles modernos em sistemas não suportados sem revisão de engenharia.

## 14. Nuvem e multinuvem

- Aplique princípios consistentes de identidade, carga de trabalho, dispositivo, dados, registro e política em todos os provedores de nuvem.
- Use controles nativos da nuvem, mas mantenha governança e evidências comuns.
- Remova a exposição pública, funções excessivas, chaves não gerenciadas e relações de confiança excessivamente amplas.
- Proteja planos de gerenciamento e pipelines CI/CD.
- Avaliar continuamente desvios de configuração e caminhos de ataque.

## 15. Desenho de políticas e decisões de acesso

- Definir assunto, recurso, ação, condições, risco, decisão, aplicação, duração da sessão e regras de reautenticação.
- Use a negação por padrão para recursos confidenciais, evitando regras que bloqueiem operações essenciais ou emergenciais.
- Avalie o acesso continuamente e reduza privilégios quando o contexto mudar.
- Registre os motivos das recusas e forneça mecanismos acessíveis de apoio e apelação.

## 16. Privacidade, ética e acessibilidade

- Colete apenas os sinais necessários para segurança e defina controles de retenção e acesso.
- Revise o monitoramento da força de trabalho com as partes interessadas jurídicas, de privacidade, trabalhistas e éticas.
- Testar políticas para verificar se há impacto desproporcional em trabalhadores remotos, prestadores de serviços, viajantes, pessoas com deficiência e usuários em locais de baixa conectividade.
- Fornecer avisos transparentes e métodos alternativos de autenticação ou recuperação.
- Não utilize pontuações de risco comportamental como prova automática de má conduta.

## 17. Estratégia de migração

- Comece com um serviço comercial ou grupo de usuários de alto valor, em vez de tentar uma substituição corporativa simultânea.
- Crie dependências, arquitetura alvo, marcos, proprietários, financiamento, critérios de teste, planos de reversão e etapas de descomissionamento.
- Execute controles antigos e novos em paralelo quando necessário.
- Remova caminhos de confiança obsoletos após a validação.
- Comunicar mudanças e treinar equipes de suporte antes da aplicação.

## 18. Teste e garantia

- Teste de autenticação, autorização, postura do dispositivo, segmentação, aplicação de políticas, registro, revogação, recuperação e acesso de emergência.
- Realizar exercícios de mesa e testes adversários autorizados.
- Teste tokens roubados, dispositivos comprometidos, contas inativas, privilégios excessivos, movimentação lateral e cenários de exfiltração de dados.
- Verifique se as falhas nas políticas falham com segurança, sem causar interrupções inaceitáveis ​​nos negócios.
- Teste novamente após grandes alterações.

## 19. Métricas e relatórios executivos

- Meça a cobertura de recursos, adoção de MFA resistente a phishing, cobertura de dispositivos gerenciados, duração de acesso privilegiado, cobertura de segmentação, contas obsoletas, exceções de política, tempo para revogar acesso, contenção de movimento lateral e exposição de dados confidenciais.
- Relatar a redução de riscos de negócios, não apenas a implantação de ferramentas.
- Mostrar tendências, dependências, ações atrasadas, riscos aceitos e decisões necessárias.
- Evite métricas de vaidade que recompensam o bloqueio de trabalhos legítimos.

## 20. Plano 30/60/90-day

- Dias 1 a 30: estabelecer governança, inventariar serviços críticos, identificar as principais suposições de confiança, proteger identidades privilegiadas e permitir o registro essencial.
- Dias 31 a 60: implementar acesso condicional, sinais de dispositivos, identidades de carga de trabalho, segmentação de prioridade, classificação de dados e restrições de terceiros.
- Dias 61-90: automatizar respostas selecionadas, testar cenários de alto risco, retirar caminhos de acesso obsoletos, estabelecer métricas e aprovar a próxima onda de implementação.

## 21. Avaliação de maturidade

## 22. Lista de verificação de prontidão de produção

☐ Patrocinador executivo e proprietários de pilares
☐ Serviços e recursos críticos inventariados
☐ Arquitetura alvo e roteiro aprovados
☐ MFA resistente a phishing priorizada
☐ Acesso privilegiado controlado
☐ Identidades não humanas governadas
☐ Postura do dispositivo utilizado no acesso
☐ Segmentação prioritária implementada
☐ Acesso a aplicativos e API aplicado
☐ Dados sensíveis classificados e protegidos
☐ Acesso de terceiros restrito
☐ Telemetria central e detecções habilitadas
☐ Automação testada com reversão
☐ Revisão de privacidade e acessibilidade concluída
☐ Exercícios de acesso a incidentes e emergências concluídos
☐ Métricas e revisões de exceções agendadas

## 23. Referências oficiais

- Arquitetura Zero Trust NIST SP 800-207: https://csrc.nist.gov/pubs/sp/800/207/final
- NIST SP 1800-35 Implementando uma arquitetura Zero Trust: https://csrc.nist.gov/pubs/sp/1800/35/final
- Controle de acesso nativo da nuvem NIST SP 800-207A: https://csrc.nist.gov/pubs/sp/800/207/a/final
- Modelo de maturidade CISA Zero Trust versão 2.0: https://www.cisa.gov/resources-tools/resources/zero-trust-maturity-model
- Estratégia Zero Trust do Departamento de Defesa dos EUA: https://dodcio.defense.gov/Portals/0/Documents/Library/DoD-ZTStrategy.pdf
- Centro de orientação Microsoft Zero Trust: https://learn.microsoft.com/security/zero-trust/

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
| Pilar | Tradicional | Inicial | Avançado | Ótimo |
| --- | --- | --- | --- | --- |
| Identidade | Senhas e funções amplas | AMF para usuárioes prioritários | Acesso baseado em risco e PAM | Resistente a phishing, contínuo e automatizado |
| Dispositivos | Estoque limitado | Gestão básica | Acesso baseado em conformidade | Postura contínua e resposta automatizada |
| Redes | Rede confiável plana | Segmentação prioritária | Segmentação com reconhecimento de aplicação | Acesso dinâmico com privilégios mínimos |
| Aplicações | Confiança herdada | SSO e inventário | Identidades de carga de trabalho e política de API | Autorização contínua e proteção em tempo de execução |
| Dados | Proteção baseada em localização | Pilotos de classificação | DLP e controles de direitos | Política segue dados e riscos |
| Visibilidade | Toras isoladas | Arrecadação central | Análise entre pilares | Feedback e resposta automatizados |
