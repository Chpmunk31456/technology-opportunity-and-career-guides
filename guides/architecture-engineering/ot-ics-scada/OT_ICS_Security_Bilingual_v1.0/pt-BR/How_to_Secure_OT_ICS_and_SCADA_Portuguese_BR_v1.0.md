# Como proteger ambientes OT, ICS e SCADA

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

Um guia prático para segurança cibernética industrial, proteção, resiliência, arquitetura, monitoramento, resposta a incidentes e governança
Alberto (Al) Leiva
Versão 1.0 - julho de 2026
CC BY-NC-SA 4.0

## Finalidade e aviso de uso responsável

Este manual fornece orientação defensiva para organizações que possuem ou operam tecnologia operacional. As mudanças na TO podem afetar os processos físicos, a segurança do trabalhador, a segurança pública, a qualidade do produto e as condições ambientais. Todos os testes, varreduras, alterações de configuração e ações de incidentes devem ser autorizados e coordenados com os proprietários de operações, engenharia, segurança e equipementos.
Segurança antes da segurança. Se uma ação de segurança cibernética puder desestabilizar um processo físico, interrompa e obtenha aprovação operacional antes de prosseguir.

## Índice

- 1. Compreendendo TO, ICS e SCADA
- 2. Por que a segurança de TO difere da segurança de TI
- 3. Governação e responsabilização partilhada
- 4. Inventário de ativos e contexto do sistema
- 5. Avaliação de riscos e integração de segurança
- 6. Arquitetura, zonas e conduítes seguros
- 7. Gerenciamento de identidade e acesso
- 8. Acesso remoto e suporte de terceiros
- 9. Segurança de rede e protocolos industriais
- 10. Configuração segura e controle de alterações
- 11. Vulnerabilidade e gerenciamento de patches
- 12. Segurança de endpoint, servidor e estação de trabalho de engenharia
- 13. Backup, recuperação e resiliência
- 14. Monitoramento e detecção
- 15. Defesa informada sobre ameaças com MITRE ATT&CK para ICS
- 16. Resposta a incidentes em TO
- 17. Ransomware e preparação para eventos destrutivos
- 18. Risco da cadeia de suprimentos e do fornecedor
- 19. Segurança em nuvem, IIoT, borda e sem fio
- 20. Segurança física e controles ambientais
- 21. Conformidade, evidências e métricas
- 22. Roteiro de implementação 30/60/90-day
- 23. Listas de verificação e artefatos de amostra
- 24. Glossário e referências oficiais

## 1. Compreendendo TO, ICS e SCADA

- A tecnologia operacional inclui sistemas e dispositivos que monitoram ou controlam processos físicos.
- Os sistemas de controle industrial podem incluir sistemas de controle distribuído, controladores lógicos programáveis, sistemas instrumentados de segurança, unidades terminais remotas, interfaces homem-máquina, historiadores, estações de trabalho de engenharia e dispositivos de campo.
- O SCADA geralmente suporta monitoramento e controle distribuídos geograficamente, como sistemas elétricos, de água, de dutos, de transporte e ambientais.
- Documente as consequências físicas de cada função digital crítica.

## 2. Por que a segurança de TO é diferente da segurança de TI

- Segurança, estabilidade de processo, confiabilidade e disponibilidade geralmente têm prioridade sobre mudanças rápidas de segurança.
- Os dispositivos legados podem ter vida útil longa, recursos computacionais limitados, protocolos proprietários e sistemas operacionais não suportados.
- Varredura ativa, testes agressivos, correção automática ou reinicializações não planejadas podem interromper a produção ou criar condições inseguras.
- A recuperação pode exigir validação de engenharia, inspeção física, calibração e sequências de reinicialização controladas.
- As decisões de segurança devem envolver operações e engenharia, em vez de serem impostas apenas pela TI.

## 3. Governança e responsabilidade compartilhada

- Definir a propriedade executiva do risco cibernético de TO.
- Criar um grupo diretor de segurança de TO incluindo operações, engenharia, segurança, TI, segurança, jurídico, compras e continuidade de negócios.
- Designar proprietários de sistemas, proprietários de ativos, proprietários de redes, proprietários de segurança e autoridade para decisão de incidentes.
- Estabelecer padrões aprovados para arquitetura, acesso, suporte remoto, registro em log, backups, gerenciamento de mudanças e resposta a incidentes.
- Documentar a autoridade de aceitação de riscos e as datas de expiração das exceções.

## 4. Inventário de ativos e contexto do sistema

- Inventariar hardware, software, firmware, sistemas operacionais, controladores, dispositivos de rede, sistemas virtuais, rádios, sensores, atuadores e sistemas de segurança.
- Registre fabricante, modelo, número de série, firmware, localização física, função do processo, proprietário, endereço de rede, dependências, criticidade, status de suporte e método de backup.
- Use a descoberta passiva sempre que possível e valide os resultados com documentação de engenharia e inspeção física.
- Manter diagramas de rede, fluxos de dados, dependências de processos e uma linha de base aprovada.
- Identifique ativos desconhecidos, não gerenciados, sem suporte e temporários.

## 5. Avaliação de riscos e integração de segurança

- Definir o processo, a missão, a segurança, as consequências ambientais, de qualidade, financeiras e de serviço público da falha.
- Modelar eventos cibernéticos que podem causar perda de visão, perda de controle, manipulação de controle, negação de serviço, estado inseguro ou perda de proteção.
- Avaliar ameaças, vulnerabilidades, salvaguardas existentes, probabilidade, consequência e recuperabilidade.
- Integre o risco de segurança cibernética com análise de perigos de processo, análises de segurança, análise de impacto nos negócios e gerenciamento de riscos corporativos.
- Prefira tratamentos de risco que reduzam a exposição cibernética sem enfraquecer a segurança ou a confiabilidade operacional.

## 6. Arquitetura, zonas e conduítes seguros

- Agrupar ativos em zonas de acordo com função, criticidade, confiança e nível de segurança exigido.
- Utilizar condutas com regras de comunicação explícitas entre zonas.
- TI corporativa separada, DMZ industrial, operações de OT, controle, segurança e redes de campo.
- Minimize as conexões diretas e evite o acesso descontrolado à Internet a partir de zonas de controle.
- Use firewalls, diodos de dados, gateways seguros, hosts de salto e proxies de aplicativos quando apropriado.
- Documente cada fluxo entre zonas, proprietário, protocolo, direção, propósito e requisitos de monitoramento.

## 7. Gerenciamento de identidade e acesso

- Use contas nomeadas e elimine credenciais de administrador compartilhadas sempre que for tecnicamente possível.
- Funções separadas de operador, engenheiro, manutenção, fornecedor e segurança.
- Use autenticação multifator em limites de acesso remoto, jump-host, VPN e gerenciamento privilegiado.
- Aplique privilégios mínimos e acesso por tempo limitado.
- Proteger contas de serviço e identidades de máquinas; alterne as credenciais cuidadosamente por meio de procedimentos de alteração aprovados.
- Revise o acesso após mudanças de trabalho, conclusão de contrato, incidentes e descomissionamento de sistema.

## 8. Acesso remoto e suporte de terceiros

- Proibir o acesso remoto direto não gerenciado a controladores e sistemas de engenharia.
- Exigir VPN aprovada ou acesso de confiança zero, MFA, um host de salto controlado, registro de sessão e autorização por tempo limitado.
- Habilite o acesso somente durante janelas de manutenção aprovadas, quando for prático.
- Exija que o fornecedor identifique a pessoa, a finalidade, os sistemas, os comandos esperados e a duração.
- Monitore sessões e encerre o acesso inativo.
- Mantenha um método de emergência para desativar todo o acesso remoto sem interromper as operações seguras.

## 9. Segurança de rede e protocolos industriais

- Use regras de negação padrão entre zonas de segurança.
- Permita apenas a origem, o destino, o protocolo, a porta e a direção necessários.
- Entenda que muitos protocolos industriais não foram projetados com autenticação ou criptografia forte.
- Use monitoramento com reconhecimento de protocolo e firewalls industriais quando apropriado.
- Proteja sincronização de horário, resolução de nomes, roteamento e serviços de gerenciamento.
- Desative portas de switch, serviços, interfaces sem fio e backdoors de fornecedores não utilizados.
- Teste alterações de rede em um ambiente representativo antes da produção.

## 10. Configuração segura e controle de alterações

- Crie linhas de base seguras aprovadas para controladores, IHMs, servidores, estações de trabalho, dispositivos de rede e sistemas de segurança.
- Desative serviços desnecessários e contas padrão.
- Use a lista de permissões de aplicativos onde houver suporte e segurança operacional.
- Exigir revisão por pares, aprovação operacional, backups, planos de reversão e validação pós-alteração.
- Registre alterações de lógica, alterações de firmware, alterações de ponto de ajuste, alterações de conta e alterações de regras de rede.
- Use verificação de integridade criptográfica ou controle de versão para configurações críticas e lógica de controle.

## 11. Vulnerabilidade e gerenciamento de patches

- Acompanhe avisos de fornecedores, alertas CISA, status de suporte, vulnerabilidades exploradas conhecidas e controles de compensação.
- Não aplique patches apenas porque a pontuação de vulnerabilidade é alta; considere exposição, explorabilidade, segurança, impacto no processo e opções de recuperação.
- Teste patches e firmware em um ambiente representativo.
- Agende manutenção com operações e crie backups e planos de reversão.
- Use segmentação, lista de permissões, aplicação de patches virtuais, monitoramento e restrições de acesso quando a aplicação imediata de patches não for segura.
- Documentar o risco aceito e revisá-lo periodicamente.

## 12. Segurança de endpoint, servidor e estação de trabalho de engenharia

- Use estações de trabalho de engenharia dedicadas para sistemas críticos.
- Restrinja e-mail, navegação na web, software pessoal e uso geral do escritório em endpoints OT.
- Use controles de mídia removível, quiosques de verificação de malware e procedimentos de transferência aprovados.
- Proteja o acesso do administrador local e desative contas desnecessárias.
- Implante a proteção de endpoint somente após validação de compatibilidade e desempenho.
- Manter instaladores, licenças, drivers, configurações e mídia de recuperação offline.

## 13. Backup, recuperação e resiliência

- Fazer backup da lógica do controlador, projetos de IHM, configurações de histórico, imagens de servidores, configurações de rede, certificados, licenças, receitas e dados críticos.
- Mantenha cópias off-line protegidas ou imutáveis.
- Teste de restauração com engenharia e operações.
- Documente a ordem de dependência e os procedimentos de reinicialização segura.
- Manter dispositivos sobressalentes, firmware aprovado, mídia de configuração e contatos de fornecedores.
- Exercite a operação manual ou procedimentos em modo degradado sempre que possível.

## 14. Monitoramento e detecção

- Colete eventos de rede, firewall, acesso remoto, identidade, endpoint, servidor, historiador e controlador de acordo com a capacidade do sistema.
- Use monitoramento de rede OT passivo e análises com reconhecimento de protocolo.
- Comunicações normais de base, atividades de engenharia, downloads de lógica, atualizações de firmware, novos dispositivos e sessões remotas.
- Alerta sobre novos ativos, protocolos inesperados, alterações na lógica do controlador, proteções desabilitadas, comandos incomuns e tráfego entre zonas.
- Garantir que as detecções sejam revisadas por pessoal que entenda tanto a segurança cibernética quanto o processo físico.

## 15. Defesa informada sobre ameaças com MITRE ATT&CK para ICS

- Use ATT&CK for ICS para entender os objetivos do adversário e as técnicas observadas em ambientes industriais.
- Mapear técnicas prováveis ​​para telemetria disponível, controles preventivos, detecções, ações de resposta e procedimentos de recuperação.
- Priorize cenários relevantes para o setor, arquitetura e exposição a ameaças da organização.
- Não trate a ATT&CK como uma lista de verificação de conformidade.
- Usar exercícios práticos e validação de detecção em vez de técnicas inseguras ao vivo em sistemas de controle de produção.

## 16. Resposta a incidentes no AT

- Criar um plano de resposta a incidentes específico de TO integrado com segurança, operações, engenharia, segurança física, jurídico, comunicações e resposta empresarial.
- Definir quem pode isolar uma rede, interromper um processo, desabilitar o acesso remoto, alterar a lógica do controlador ou iniciar o desligamento.
- Preservar logs, configurações, estado do controlador, capturas de rede e evidências físicas.
- Conter com cuidado; desconectar um dispositivo pode remover a visibilidade ou colocar o processo em um estado inseguro.
- Use uma sequência de recuperação controlada e verifique a integridade do processo antes de retornar à operação normal.
- Conduzir lições aprendidas e atualizar diagramas, controles, manuais e treinamentos.

## 17. Ransomware e preparação para eventos destrutivos

- Segmentar TO de redes corporativas e restringir caminhos de confiança administrativos.
- Proteja backups e contas de recuperação do mesmo caminho de comprometimento.
- Prepare-se para perda de serviços de identidade, virtualização, compartilhamentos de arquivos, acesso remoto, historiadores e estações de trabalho de engenharia.
- Identificar operações mínimas viáveis ​​e alternativas manuais.
- Exercer a comunicação quando o e-mail corporativo e as ferramentas de colaboração não estiverem disponíveis.
- Não conecte sistemas restaurados não verificados de volta ao OT.

## 18. Risco da cadeia de suprimentos e do fornecedor

- Avaliar fabricantes de equipementos, integradores, provedores de manutenção, fornecedores de software, serviços gerenciados, serviços em nuvem e provedores de suporte remoto.
- Exigir desenvolvimento seguro, divulgação de vulnerabilidades, integridade de atualização, compromissos de suporte, notificação de incidentes e acesso remoto controlado.
- Verifique firmware, software e fontes de configuração.
- Rastreie produtos não suportados e planos de substituição.
- Avaliar subcontratados e terceiros que possam acessar ou influenciar o meio ambiente.

## 19. Segurança em nuvem, IIoT, borda e sem fio

- Inventariar sensores, gateways, análises, gêmeos digitais, telemetria remota, modems celulares e redes sem fio conectados à nuvem.
- Separe o gerenciamento da nuvem do controle direto do processo sempre que possível.
- Use identidade forte de dispositivos, gerenciamento do ciclo de vida de certificados, comunicações criptografadas e conexões de saída controladas.
- Valide o comportamento à prova de falhas se os serviços de nuvem ou de comunicação não estiverem disponíveis.
- Proteger mecanismos de atualização e plataformas de gerenciamento de borda.
- Avalie a residência dos dados, a privacidade, o acesso do fornecedor e a dependência de serviços externos.

## 20. Segurança física e controles ambientais

- Controlar o acesso a salas de controle, gabinetes, armários de rede, gabinetes de campo e equipementos portáteis de engenharia.
- Monitore adulterações, conexões não autorizadas, portas abertas de gabinetes e substituição de dispositivos.
- Proteja energia, resfriamento, supressão de incêndio, água, monitoramento ambiental e geração de backup.
- Coordenar investigações cibernéticas e físicas.
- Trate locais de campo autônomos e subestações remotas como ambientes de maior exposição.

## 21. Conformidade, evidências e métricas

- Maintain evidence of inventories, diagrams, risk assessments, approvals, access reviews, backups, restoration tests, changes, vulnerabilities, training, exercises, incidents, and remediation.
- Mapear controles para NIST CSF 2.0, NIST SP 800-82 Rev. 3, ISA/IEC 62443, requisitos do setor e política organizacional.
- Acompanhe a redução de riscos, não apenas a atividade.
- Useful metrics include unmanaged assets, unsupported assets, remote-access exceptions, overdue critical findings, restoration success, detection coverage, and exercise results.
- Identificar claramente o NIST SP 800-82 Rev. 4 como um trabalho preliminar, em vez de uma orientação final atual.

## 22. Roteiro de implementação 30/60/90-day

- Dias 1 a 30: estabelecer a propriedade, identificar processos críticos, inventariar ativos prioritários, documentar o acesso remoto, validar backups e revisar os principais caminhos de TI para TO.
- Dias 31 a 60: criar zonas e conduítes, reduzir o acesso excessivo, definir a linha de base do tráfego de rede, estabelecer triagem de vulnerabilidades e escrever manuais de incidentes de TO.
- Dias 61-90: testar restauração, testar cenários de ransomware e perda de visão, validar detecções, formalizar requisitos de fornecedores e criar métricas executivas.

## 23. Listas de verificação e artefatos de amostra

### Lista de verificação de prontidão para produção

☐ Processo crítico e consequências de segurança documentadas
☐ Inventário de ativos e diagramas de rede validados
☐ Proprietários e autoridade de incidente atribuída
☐ Zonas e condutas aprovadas
☐ Acesso remoto controlado e monitorado
☐ Contas nomeadas, limites de MFA e acesso privilegiado revisados
☐ Backups protegidos e restauração testada
☐ Processo de triagem de vulnerabilidade operacional
☐ Linhas de base seguras e controle de mudanças em vigor
☐ Monitoramento passivo e detecções de alto valor habilitadas
☐ Plano de incidente de TO e decisões de contenção segura documentadas
☐ Exercício de ransomware e perda de visão concluído
☐ Riscos de fornecedores e produtos não suportados rastreados
☐ Procedimentos de operação manuais ou degradados revisados
☐ Aceitação de risco executivo registrada

### Exemplos de campos de inventário de ativos de TO

### Exemplo de declaração de risco de TO

Risco: uma conta de fornecedor compartilhada com acesso remoto persistente pode ser comprometida e usada para modificar a lógica do controlador. Impacto: Perda de controle, condições inseguras do processo, interrupção da produção e danos ao equipemento. Tratamento: Substitua a conta compartilhada por identidades nomeadas, MFA, aprovação por tempo limitado, sessões monitoradas de jump-host, alertas de mudança de controlador e revisão de acesso trimestral.

## 24. Glossário e referências oficiais

### Referências oficiais

- NIST SP 800-82 Rev. 3 - Guia para segurança de tecnologia operacional: https://csrc.nist.gov/pubs/sp/800/82/r3/final
- NIST SP 800-82 Rev. 4 - Pré-rascunho da chamada para comentários: https://csrc.nist.gov/pubs/sp/800/82/r4/iprd
- Estrutura de segurança cibernética NIST 2.0: https://www.nist.gov/cyberframework
- ISA/IEC Série 62443 de padrões: https://www.isa.org/standards-and-publications/isa-standards/isa-iec-62443-series-of-standards
- MITRE ATT&CK para ICS: https://attack.mitre.org/matrices/ics/
- Metas de desempenho de segurança cibernética intersetorial da CISA: https://www.cisa.gov/cross-sector-cybersecurity-performance-goals
- Recursos de sistemas de controle industrial CISA: https://www.cisa.gov/topics/industrial-control-systems

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
| Campo | Exemplo |
| --- | --- |
| ID do ativo | OT-PLC-001 |
| Função | Controle de água de alimentação de caldeiras |
| Proprietário | Operações da Planta |
| Fabricante/modelo | Modelo de controlador aprovado |
| Firmware/SO | Versão validada |
| Localização | Planta 2 - Gabinete de Controle B |
| Zona | Controle Básico de Processo |
| Criticidade | Crítico |
| Impacto na segurança | Potencial interrupção do processo e danos ao equipemento |
| Dependências de rede | HMI, historiador, estação de trabalho de engenharia |
| Acesso remoto | Fornecedor somente por meio de host de salto aprovado |
| Backup | Backup lógico verificado trimestralmente |
| Status de suporte | Apoiado até 2028 |
| Última revisão | 18/07/2026 |
| Prazo | Definição |
| --- | --- |
| AT | Tecnologia que monitora ou controla processos físicos, dispositivos e infraestrutura. |
| ICS | Sistemas de controle industrial usados ​​para controlar processos industriais. |
| SCADA | Controle supervisório e aquisição de dados para monitoramento e controle distribuído. |
| CLP | Controlador lógico programável. |
| IHM | Interface homem-máquina utilizada pelos operadores. |
| SIS | Sistema instrumentado de segurança projetado para mover um processo para um estado seguro. |
| Zona | Grupo de ativos com requisitos de segurança comuns. |
| Conduíte | Caminho de comunicação controlado entre zonas. |
| Historiador | Sistema que armazena dados de processos de série temporal. |
| Estação de trabalho de engenharia | Sistema utilizado para configurar e programar ativos industriais. |
