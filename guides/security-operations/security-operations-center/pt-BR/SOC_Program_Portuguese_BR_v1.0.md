# Como construir um programa de centro de operações de segurança

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

COMO CONSTRUIR UM PROGRAMA DE CENTRO DE OPERAÇÕES DE SEGURANÇA
Um manual de implementação conciso e prático
Alberto (Al) Leiva
Versão 1.0 - julho de 2026

## Propósito

Use este manual para trabalhos defensivos legais, autorizados. Adapte os controles ao risco organizacional, às obrigações legais, às necessidades de acessibilidade e aos recursos disponíveis.

## Objetivo e modelo operacional

- Definir missão, escopo, clientes, autoridade, horário de atendimento, caminhos de escalonamento e relacionamento com resposta a incidentes do SOC.
- Escolha um modelo interno, terceirizado, cogerenciado ou virtual com base no risco, pessoal, cobertura e orçamento.
- Crie um catálogo de serviços que cubra monitoramento, triagem, investigação, caça a ameaças, engenharia de detecção, coordenação de vulnerabilidades e relatórios.

## Pessoas e funções

- Designar um gerente SOC, líderes de turno, analistas, engenheiros de detecção, caçadores de ameaças, respondedores de incidentes, engenheiros de plataforma e contatos de negócios.
- Use níveis claros sem prender os analistas em trabalhos repetitivos.
- Fornecer treinamento, orientação, procedimentos acessíveis, cargas de trabalho razoáveis ​​e controles de fadiga.

## Tecnologia e telemetria

- Priorize identidade, endpoint, rede, nuvem, email, aplicativos, vulnerabilidade e telemetria de negócios críticos.
- Normalize tempo, identidade de ativo, identidade de usuário e campos de evento.
- Proteja logs, defina retenção, monitore falhas de ingestão e evite coletar dados confidenciais sem propósito.

## Engenharia de detecção

- Mapeie detecções para ameaças, caminhos de ataque, ativos e impacto nos negócios.
- Documente a finalidade, a lógica, as fontes de dados, o proprietário, a gravidade, os falsos positivos esperados, as etapas de resposta e as evidências de teste.
- Ajuste continuamente e retire regras obsoletas.

## Triagem e investigação

- Use critérios de gravidade que combinem confiança, escopo, privilégio, dados, impacto nos negócios e exploração ativa.
- Preservar evidências e registrar decisões.
- Escale rapidamente quando segurança, dados confidenciais, acesso privilegiado ou comprometimento generalizado puderem estar envolvidos.

## Caça e inteligência de ameaças

- Utilizar a inteligência para formar hipóteses testáveis ​​em vez de recolher indicadores sem contexto.
- Cace apenas em ambientes autorizados.
- Converta descobertas validadas em detecções, controles e lições aprendidas.

## Qualidade, métricas e roteiro

- Medir a cobertura, a qualidade do alerta, o tempo de reconhecimento, o tempo de contenção, incidentes reabertos, lacunas de detecção e carga de trabalho do analista.
- Evite recompensar a velocidade de fechamento do alerta em detrimento da precisão.
- Dias 1 a 30: escopo, telemetria, funções e manuais críticos. Dias 31 a 60: ciclo de vida de detecção, gerenciamento de casos e exercícios. Dias 61-90: caça, métricas, automação e revisão executiva.

## Lista de verificação de implementação

☐ Proprietário atribuído
☐ Escopo aprovado
☐ Inventário concluído
☐ Riscos priorizados
☐ Políticas documentadas
☐ Controles implementados
☐ Evidências retidas
☐ As exceções expiram
☐ Teste concluído
☐ Revisão gerencial registrada

## Referências oficiais

- NIST SP 800-61 Rev. 3: https://csrc.nist.gov/pubs/sp/800/61/r3/final
- NIST CSF 2.0: https://www.nist.gov/cyberframework
- MITRE ATT&CK: https://attack.mitre.org/

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
