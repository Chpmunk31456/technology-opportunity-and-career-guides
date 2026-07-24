# Como realizar avaliações de risco de fornecedores terceirizados

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

Um guia prático para due diligence, contratos, evidências, monitoramento, incidentes e segurança da cadeia de suprimentos
Alberto (Al) Leiva
Versão 1.0 - julho de 2026
A segurança humana e a justiça estão em primeiro lugar. Este manual é para uso legal, autorizado e defensivo. As avaliações dos fornecedores devem ser justas, baseadas em evidências, proporcionais ao risco e respeitando a confidencialidade.

## 1. Objetivo e resultados

- Identifique como um fornecedor, provedor de serviços, subcontratado, produto de software, plataforma de nuvem ou provedor de IA pode afetar a organização.
- Decida se o relacionamento é aceitável, requer remediação, precisa de termos contratuais mais fortes ou não deve prosseguir.
- Crie um registro repetível de escopo, evidências, descobertas, decisões, proprietários e datas de revisão.
- Aplicar diligência mais profunda em relacionamentos de alto risco sem criar barreiras desnecessárias para fornecedores de baixo risco.

## 2. Governança do programa

- Atribua patrocínio executivo e propriedade clara das equipes de segurança, privacidade, jurídico, compras, conformidade, negócios e tecnologia.
- Definir uma metodologia aprovada, níveis de risco, requisitos de evidência, rotas de escalonamento, autoridade de exceção e cadência de revisão.
- Manter a independência entre o patrocinador do negócio e a pessoa que aprova o risco residual material.
- Meça a pontualidade, avaliações atrasadas, descobertas críticas não resolvidas, risco de concentração e desempenho de incidentes.

## 3. Construa o estoque do fornecedor

- Registre a razão social do fornecedor, empresa-mãe, serviço, proprietário da empresa, proprietário do contrato, países, dados tratados, integrações, subcontratados, data de renovação e requisitos de rescisão.
- Inclui software gratuito, componentes de código aberto, aplicativos de mercado, consultores, corretores de dados, serviços de IA e TI paralela.
- Vincular fornecedores a serviços empresariais, sistemas, conjuntos de dados, regulamentações e planos de continuidade.
- Marcar com precisão fornecedores inativos, duplicados, adquiridos, desinvestidos e rescindidos.

## 4. Triagem e níveis de risco

- Tier fornecedores antes de enviar um longo questionário.
- Considere a sensibilidade dos dados, o acesso privilegiado, a conectividade de rede, a autoridade de transação, a criticidade do negócio, a população de usuários, a exposição geográfica, o uso de IA, os subcontratados e a facilidade de substituição.
- Utilize uma pontuação simples de risco inerente, mas permita julgamento profissional e substituições documentadas.
- Não trate um pequeno fornecedor como de baixo risco apenas porque tem poucos funcionários.

## 5. Escopo da avaliação

- Defina o produto, serviço, ambiente, fluxo de dados, interfaces, locais e contrato exatos em revisão.
- Indique se a revisão abrange a empresa, um produto, um serviço hospedado, uma região de implantação ou uma atividade de processamento específica.
- Identificar o que está excluído e porquê.
- Defina datas de evidências e rejeite evidências obsoletas quando elas não representarem mais o serviço.

## 6. Evidência de devida diligência

- Prefira evidências a respostas de sim ou não sem suporte.
- As possíveis evidências incluem relatórios SOC, certificados ISO, resumos de testes de penetração, políticas, diagramas de arquitetura, diagramas de fluxo de dados, relatórios de vulnerabilidade, testes de continuidade de negócios, exercícios de resposta a incidentes, avaliações de privacidade e registros de desenvolvimento seguro.
- Verificar o escopo, período, organização emissora, qualificações, exceções, respostas da gestão e controles complementares do cliente.
- Proteja evidências confidenciais do fornecedor e limite o acesso interno.

## 7. Domínios de segurança a serem avaliados

- Governança e gestão de riscos.
- Identidade, acesso privilegiado e autenticação.
- Proteção de dados, criptografia, retenção e exclusão.
- Segurança de rede e nuvem.
- Desenvolvimento seguro, gerenciamento de vulnerabilidades e cadeia de fornecimento de software.
- Registro, monitoramento, detecção e resposta a incidentes.
- Continuidade dos negócios, recuperação de desastres e resiliência.
- Obrigações de privacidade, regulatórias e contratuais.
- Subcontratados e quartos terceiros.
- Sistemas de IA, modelos, agentes, dados de treinamento, RAG e decisões automatizadas quando aplicável.

## 8. Desenho do questionário

- Faça perguntas que possam alterar uma decisão ou requisito de controle.
- Use perguntas condicionais para que fornecedores de baixo risco não recebam seções irrelevantes.
- Solicite um item claro de evidência para cada afirmação material.
- Evite copiar centenas de controles sem explicar a aplicabilidade.
- Permitir que o fornecedor explique os controles de compensação e a correção planejada.
- Rastreie a origem da pergunta, o mapeamento da estrutura, as evidências, a conclusão do revisor e a data de validade.

## 9. Revise relatórios e certificações SOC

- Confirme se o relatório ou certificado cobre o serviço que está sendo adquirido.
- Revise o período de auditoria, opinião, limitações de escopo, exclusões, exceções, organizações de subserviços e controles complementares de entidades usuárias.
- Não trate um relatório limpo como prova de que todos os riscos foram abordados.
- Confirme se o certificado é válido e emitido por um organismo credenciado apropriado, quando aplicável.
- Solicitar cartas-ponte ou provas mais recentes quando o período de cobertura terminar.

## 10. Risco de nuvem, software e código aberto

- Identifique modelo de hospedagem, regiões, locação, acesso administrativo, backup, criptografia, registro em log e responsabilidades de segurança do cliente.
- Revise listas de materiais de software quando apropriado, gerenciamento de dependências, assinatura de código, integridade de lançamento e práticas de divulgação de vulnerabilidades.
- Avalie a rapidez com que as vulnerabilidades críticas são triadas e corrigidas.
- Determine se componentes não suportados, produtos em fim de vida ou bibliotecas não mantidas estão presentes.
- Documente as tarefas de configuração do cliente para que o risco não seja atribuído incorretamente apenas ao fornecedor.

## 11. Risco do provedor de IA e do serviço de IA

- Identificar modelos, provedores, usos de dados, retenção imediata, uso de treinamento, subprocessadores, processamento geográfico, controles de conteúdo, supervisão humana e processos de incidentes.
- Determinar se informações confidenciais ou pessoais podem ser usadas para melhorar modelos compartilhados.
- Avalie injeção imediata, vazamento de dados, agentes inseguros, acesso a ferramentas, autorização RAG, atualizações de modelo e confiabilidade de saída.
- Exigir transparência sobre alterações de modelo de material ou serviço.
- Definir usos proibidos e requisitos de aprovação para decisões de alto impacto.

## 12. Controles de contratos e aquisições

- Traduzir decisões de risco importantes em linguagem contratual executável.
- Abordar requisitos de segurança, privacidade, confidencialidade, localização de dados, subcontratados, direitos de auditoria, notificação de incidentes, cooperação, remediação de vulnerabilidades, continuidade, seguro, registros, exclusão e assistência para rescisão.
- Definir níveis de serviço mensuráveis ​​e soluções quando apropriado.
- Garantir que as obrigações contratuais fluam para os subcontratados relevantes.
- Não confie num questionário quando o contrato não exige os controlos prometidos.

## 13. Descobertas e classificações de risco

- Escreva as descobertas como condição, risco, evidência, impacto e ação necessária.
- Separar risco inerente, eficácia de controle, risco residual e aceitação do negócio.
- Use critérios de severidade de forma consistente, mas considere a explorabilidade, a sensibilidade dos dados, o impacto nos negócios, os deveres legais e a concentração.
- Não aumente todas as lacunas para alto risco.
- Registre a incerteza quando as evidências estiverem incompletas.

## 14. Correção e exceções

- Atribua um proprietário, ação, data prevista, exigência de evidência e data de revisão.
- Utilize salvaguardas provisórias quando a remediação permanente levar tempo.
- Escalar ações de alto risco vencidas.
- Exigir aceitação formal para risco residual material.
- Defina datas de vencimento para exceções e reavalie antes da renovação.
- Encerrar as descobertas somente após analisar as evidências.

## 15. Monitoramento contínuo

- Monitorar as classificações de segurança com cautela; use-os como sinais e não como conclusões finais.
- Rastreie violações, mudanças de propriedade, aquisições, ações legais, status de certificados, vulnerabilidades, interrupções de serviço, mudanças geográficas, subcontratados e alterações materiais de produtos.
- Reavaliar após incidentes, grandes mudanças arquitetônicas, expansão do uso de dados, novas integrações ou renovação de contrato.
- Mantenha a frequência de revisão proporcional ao risco.

## 16. Resposta a incidentes do fornecedor

- Manter contatos atuais e caminhos de escalonamento.
- Definir cronogramas de notificação e informações necessárias sobre incidentes nos contratos.
- Coordenar contenção, preservação de evidências, análise regulatória, comunicação com o cliente, recuperação e lições aprendidas.
- Determine se o acesso, tokens, integrações ou transferências de dados devem ser suspensos.
- Acompanhar as ações corretivas do fornecedor e validar o fechamento.

## 17. Offboarding e rescisão

- Desative contas, tokens, integrações, acesso VPN, chaves API, certificados e acesso administrativo.
- Recupere ativos organizacionais e confirme a devolução de dados ou exclusão segura.
- Preservar os registros necessários para fins legais, regulatórios ou de auditoria.
- Transferir conhecimentos, configurações e dependências operacionais.
- Remover o fornecedor dos inventários e ferramentas de monitoramento somente após a verificação do fechamento.

## 18. Relatórios e métricas

- Relate a população de fornecedores por nível de risco, status de avaliação, revisões atrasadas, descobertas abertas, riscos aceitos, incidentes, concentração e dependências críticas.
- Mostre tendências em vez de contagens isoladas.
- Distinguir o risco pertencente ao fornecedor das responsabilidades do cliente.
- Fornecer aos executivos decisões e exposição, não apenas taxas de conclusão de questionários.

## 19. Plano de implementação 30/60/90-day

- Dias 1 a 30: definir governança, inventariar fornecedores críticos, criar critérios de hierarquização, identificar relacionamentos vencidos de alto risco e estabelecer cláusulas contratuais mínimas.
- Dias 31 a 60: lançar avaliações baseadas em riscos, centralizar evidências, criar fluxos de trabalho de descoberta e exceção e identificar riscos de concentração e de terceiros.
- Dias 61-90: implementar monitoramento contínuo, exercícios de incidentes, portas de renovação, métricas e revisões periódicas de qualidade.

## 20. Fluxo de trabalho de avaliação prática

1. Receba a solicitação e identifique o proprietário da empresa.
1. Triagem completa de riscos inerentes.
1. Defina o escopo e os requisitos de evidência.
1. Colete e revise evidências.
1. Entreviste o fornecedor quando persistirem dúvidas relevantes.
1. Documente as descobertas e o risco residual.
1. Acordar remediação e controles de contrato.
1. Obtenha aprovação ou aceitação de risco.
1. Registre as datas de monitoramento e reavaliação.
1. Reavaliar na renovação ou após mudança material.

## 21. Exemplo de critérios de nível de risco

## 22. Amostra de descoberta

## 23. Lista de verificação de produção

☐ Entrada de inventário do fornecedor concluída
☐ Proprietário da empresa e proprietário do contrato identificados
☐ Nível de risco inerente aprovado
☐ Escopo e fluxo de dados documentados
☐ Evidências atuais e aplicáveis
☐ Escopo e exceções SOC/ISO revisados
☐ Avaliação de riscos de segurança, privacidade, continuidade e incidentes
☐ Subcontratados e concentração revisados
☐ Risco de IA revisado quando aplicável
☐ Cláusulas contratuais aprovadas
☐ Descobertas atribuídas e rastreadas
☐ Risco residual aceito pelo proprietário autorizado
☐ Acompanhamento e reavaliação agendados
☐ Requisitos de desligamento documentados

## 24. Referências oficiais

- NIST SP 800-161 Rev. 1, Práticas de gerenciamento de risco da cadeia de suprimentos de segurança cibernética: https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final
- NIST SP 1326, Guia de início rápido da avaliação de due diligence C-SCRM: https://csrc.nist.gov/pubs/sp/1326/final
- Estrutura de segurança cibernética NIST 2.0: https://www.nist.gov/cyberframework
- Recursos da cadeia de suprimentos CISA: https://www.cisa.gov/topics/cyber-threats-and-advisories/information-and-communications-technology-supply-chain-security
- ISO/IEC 27036-1:2021 Relacionamentos com fornecedores: https://www.iso.org/standard/82905.html
- ISO/IEC 27036-2:2022 Requisitos de relacionamento com fornecedores: https://www.iso.org/standard/82060.html
- ISO/IEC 27036-3:2023 Segurança da cadeia de suprimentos de hardware, software e serviços: https://www.iso.org/standard/82890.html

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
| Nível | Características típicas | Revisão |
| --- | --- | --- |
| Crítico | Acesso privilegiado, dados altamente sensíveis, operações essenciais, autoridade de transação, grande concentração | Avaliação completa, revisão de contrato, aprovação executiva, reavaliação anual ou orientada por evento |
| Alto | Dados sensíveis, integração de produção, serviços importantes, subcontratados significativos | Revisão detalhada das evidências e reavaliação anual |
| Moderado | Dados confidenciais limitados ou dependência comercial | Questionário focado e reavaliação periódica |
| Baixo | Sem dados confidenciais, sem conectividade, facilmente substituíveis | Verificação básica e revisão leve |
| Elemento | Exemplo |
| --- | --- |
| Condição | O fornecedor não exige MFA para administração de produção privilegiada. |
| Evidência | Política de acesso administrativo e entrevista com fornecedor datada de julho de 2026. |
| Risco | Uma senha roubada pode permitir acesso não autorizado à produção e exposição de dados. |
| Ação necessária | Implemente MFA resistente a phishing para contas privilegiadas e forneça evidências. |
| Controlo provisório | Restrinja o acesso por rede, monitore logins e alterne credenciais. |
| Proprietário/data de vencimento | Líder de segurança do fornecedor / 60 dias |
