# Como realizar uma avaliação de risco de segurança cibernética

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

**Autor / Autor:** Alberto (Al) Leiva  
**Versão/Versão:** 1.0 - Julho/Julio 2026  
**Licença/Licença:** CC BY-NC-SA 4.0
COMO REALIZAR UMA AVALIAÇÃO DE RISCO DE SEGURANÇA CIBERNÉTICA
Um guia prático para definir o escopo, identificar, analisar, tratar, documentar e monitorar riscos cibernéticos
Alberto (Al) Leiva
Versão 1.0 - julho de 2026
CC BY-NC-SA 4.0


## Finalidade e aviso de uso responsável

Este manual ensina um método repetível e baseado em evidências para avaliar o risco de segurança cibernética. Ele foi projetado para analistas de GRC, profissionais de segurança, gerentes, auditores, estudantes e pessoas em mudança de carreira. Ele não substitui aconselhamento jurídico, regulatório, de auditoria, de seguros ou profissional. Adapte o método à organização, setor, jurisdição e apetite ao risco.
A segurança humana está em primeiro lugar. As decisões de risco devem proteger as pessoas, os serviços essenciais, a privacidade, a acessibilidade e a resiliência organizacional. Não esconda riscos materiais ou pressione os avaliadores para produzir uma classificação preferida.


## Como usar este manual

- Leia os capítulos 1 a 5 para compreender o método.
- Use os Capítulos 6 a 12 como procedimento de avaliação de trabalho.
- Use os Capítulos 13-16 para relatórios, tratamento, monitoramento e evidências de carreira.
- Copie os modelos de amostra em uma planilha, plataforma GRC, sistema de tickets ou repositório de documentos aprovado.

## Índice

- 1. Fundamentos da avaliação de risco
- 2. Funções, governança e independência
- 3. Definir escopo e contexto
- 4. Identifique ativos, serviços e dados
- 5. Identifique ameaças e eventos de ameaças
- 6. Identificar vulnerabilidades e controlar lacunas
- 7. Analise a probabilidade
- 8. Analisar impacto
- 9. Calcular e comunicar riscos
- 10. Avaliar controles e risco residual
- 11. Desenvolver planos de tratamento
- 12. Documentar o registro de riscos
- 13. Reportar aos líderes e stakeholders
- 14. Monitorar e reavaliar
- 15. Erros comuns e verificações de qualidade
- 16. Projeto de portfólio e plano 30/60/90-day
- 17. Modelos e exemplos
- 18. Glossário e referências oficiais

## 1. Fundamentos da avaliação de risco

Uma avaliação de riscos de cibersegurança é um processo estruturado para compreender o que pode correr mal, porque pode acontecer, quão graves podem ser as consequências e o que deve ser feito. NIST SP 800-30 descreve a avaliação de risco como parte de um processo mais amplo de gestão de risco. O NIST CSF 2.0 coloca a estratégia de risco, funções, políticas, supervisão e risco da cadeia de suprimentos dentro do GOVERN e a identificação de riscos dentro do IDENTIFY.


### Uma simples declaração de risco

Como [evento de ameaça] pode explorar [vulnerabilidade ou condição] que afeta [ativo ou processo], a organização pode sofrer [impacto nos negócios].
Exemplo: como um agente de ameaça pode usar credenciais de administrador roubadas contra um serviço de acesso remoto acessível pela Internet sem MFA resistente a phishing, a organização pode enfrentar acesso não autorizado à rede, implantação de ransomware, interrupção operacional e divulgação de dados.


## 2. Funções, governança e independência

- Documentar conflitos de interesse.
- Não permitir que o proprietário do controle seja o único revisor da eficácia do controle.
- Registrar divergências e a autoridade de decisão.
- Proteja notas de entrevistas, arquitetura, vulnerabilidades e registros de riscos de acordo com a classificação.

## 3. Defina escopo e contexto

Um escopo claro evita que uma avaliação se torne superficial ou interminável. Defina primeiro o objetivo do negócio e depois a tecnologia e as dependências que o suportam.


### Declaração de escopo mínimo

Esta avaliação abrange [serviços e processos de negócios], incluindo [sistemas, dados, identidades, ambientes e fornecedores], para o período [intervalo de datas]. Avalia [tipos de risco] usando [método e escalas]. Exclui [itens], que serão abordados por [owner/date ou avaliação separada].


## 4. Identifique ativos, serviços e dados

- Comece com serviços comerciais essenciais, em vez de apenas uma lista de dispositivos.
- Mapeie sistemas, aplicativos, identidades, armazenamentos de dados, redes, instalações e fornecedores.
- Identifique os ativos da joia da coroa e os pontos únicos de falha.
- Registrar requisitos de classificação, residência, retenção e backup de dados.
- Documentar dependências upstream e downstream.
- Valide o inventário com evidências técnicas, como inventários de nuvem, registros CMDB, diretórios de identidade, diagramas de rede e contratos.

## 5. Identifique ameaças e eventos de ameaças

Use mais do que uma lista genérica de ameaças. Conectar atores e condições confiáveis ​​a eventos específicos que possam afetar o objetivo definido.
- Use incidentes internos, quase acidentes, descobertas de vulnerabilidades, relatórios de fraude, tendências de suporte técnico e observações de auditoria.
- Use inteligência externa confiável sobre ameaças e alertas do setor.
- Distinguir possibilidade de credibilidade. Um cenário deve ser plausível para a organização e o escopo.
- Evite presumir que uma ameaça é irrelevante apenas porque nunca aconteceu antes.

## 6. Identifique vulnerabilidades e controle lacunas

Uma vulnerabilidade pode ser técnica, processual, contratual, organizacional, física ou humana. A falta de um controle não é automaticamente uma vulnerabilidade; explicar como a condição permite ou piora um evento de ameaça.


### Qualidade das evidências

- Prefira evidências atuais, diretas e reprodutíveis.
- Registre a data da evidência, fonte, proprietário e limitações.
- Não trate um documento de política como prova de que um controle funciona.
- Não trate uma amostra bem-sucedida como prova de operação consistente.
- Quando faltarem provas, registe a incerteza em vez de assumir a eficácia.

## 7. Analise a probabilidade

A probabilidade é um julgamento informado sobre a probabilidade de um evento de ameaça ocorrer e produzir danos durante o horizonte de tempo determinado. Use critérios e evidências definidas, não apenas a intuição.
- Considere a capacidade, a intenção, o direcionamento, a frequência, a exposição, a facilidade de exploração e a confiabilidade do controle da ameaça.
- Separar a probabilidade do evento do impacto. Um evento provável pode ter baixo impacto e um evento raro pode ser catastrófico.
- Indique o horizonte temporal, como os próximos 12 meses.
- Documentar a incerteza e utilizar intervalos ou cenários quando a evidência for fraca.

## 8. Analise o impacto

O impacto deve descrever as consequências para os objetivos do negócio e para as pessoas, e não apenas a severidade técnica.


## 9. Calcule e comunique o risco

Uma matriz pode suportar consistência, mas a multiplicação não cria precisão científica. A narrativa, as evidências, a incerteza e o contexto empresarial são mais importantes que a aritmética.


### Exemplo de matriz 5 x 5

- Defina as classificações antes do início da avaliação.
- Permitir julgamento profissional documentado quando o resultado da matriz não reflete a real consequência do negócio.
- Não calcule a média dos riscos não relacionados em uma única pontuação.
- Utilize declarações de risco claras e explique as evidências por trás de cada classificação.

## 10. Avalie controles e risco residual

Avalie o design do controle e a eficácia operacional. Um controle bem escrito que não é executado não reduz o risco.
Reavaliar a probabilidade e o impacto depois de considerar os controles eficazes. Registre o risco residual e compare-o com o apetite ao risco, a tolerância e a autoridade de aceitação delegada.


## 11. Desenvolva planos de tratamento


### Ações de tratamento SMART

- Específico: identifique o controle ou alteração exata.
- Mensuráveis: definir evidências e critérios de sucesso.
- Atribuído: nomeie um proprietário responsável.
- Realista: confirme recursos, dependências e aprovações.
- Prazo: defina marcos e uma data de vencimento final.

## 12. Documente o registro de riscos


### Exemplo resolvido


## 13. Reporte aos líderes e stakeholders

- Liderar os objetivos de negócios e as decisões necessárias.
- Mostre os principais riscos, tendências, ações atrasadas, riscos aceitos e risco de concentração.
- Fatos separados, suposições e julgamento profissional.
- Explicar a incerteza e as limitações das evidências.
- Evite sobrecarregar os executivos com contagens brutas de vulnerabilidades.
- Adaptar detalhes técnicos aos proprietários do sistema e equipes de implementação.
- Preservar um registro de decisões e aprovações.

### Resumo executivo de uma página

- Escopo e data de avaliação
- Conclusão geral
- Três a cinco principais cenários
- Impacto nos negócios
- Pontos fortes existentes
- Ações prioritárias e investimento necessário
- Riscos que exigem aceitação ou escalonamento
- Principais suposições e limitações
- Próxima data de revisão

## 14. Monitore e reavalie

O risco não é estático. Reavaliar após mudanças significativas e com uma frequência apropriada à criticidade.
- Novo sistema, nuvem, IA, fornecedor, fusão ou aquisição
- Arquitetura de materiais ou mudança no fluxo de dados
- Grande campanha de vulnerabilidade ou ameaça
- Incidente de segurança ou quase acidente
- Falha de controle ou tratamento tardio
- Alteração regulatória ou contratual
- Mudança na criticidade do negócio
- Data da revisão periódica

## 15. Erros comuns e verificações de qualidade


### Lista de verificação de revisão de qualidade

☐ O escopo é explícito e aprovado
☐ As declarações de risco conectam ameaça, condição, ativo e consequência
☐ As classificações usam critérios definidos
☐ As evidências são atuais e rastreáveis
☐ Risco inerente e residual não se confundem
☐ A eficácia do controle é apoiada
☐ As ações de tratamento são específicas e atribuídas
☐ A aceitação usa a autoridade correta
☐ Limitações e incertezas são visíveis
☐ Os gatilhos e as datas da revisão são registrados


## 16. Projeto de portfólio e plano 30/60/90-day


### Projeto de portfólio seguro

- Escolha uma pequena empresa fictícia ou um laboratório autorizado.
- Crie uma declaração de escopo e um diagrama de arquitetura simples.
- Inventariar cinco a dez ativos e tipos de dados.
- Escreva cinco cenários de risco confiáveis.
- Definir escalas de probabilidade e impacto.
- Avaliar os controles existentes e o risco residual.
- Crie um registro de riscos e um resumo executivo de uma página.
- Publicar apenas informações fictícias e higienizadas; nunca exponha vulnerabilidades reais, credenciais, dados de clientes ou arquitetura confidencial.

### Primeiros 30 dias

- Estude vocabulário de risco, NIST CSF 2.0 e NIST SP 800-30.
- Pratique escrever declarações de risco.
- Construir critérios de probabilidade e impacto.
- Crie um exemplo de inventário de ativos e registro de riscos.

### Dias 31-60

- Realizar uma avaliação de um serviço fictício ou autorizado.
- Praticar entrevistas de controle e avaliação de evidências.
- Escreva planos de tratamento e um resumo executivo.
- Peça a um mentor para desafiar suposições e classificações.

### Dias 61-90

- Mapear riscos para controles relevantes e objetivos de negócios.
- Criar métricas e gatilhos de reavaliação.
- Publique um projeto de portfólio GitHub higienizado com README e modelos.
- Pratique explicar um risco a um proprietário técnico e a um executivo.

## 17. Modelos e exemplos


### Perguntas da entrevista sobre riscos

- Que resultado comercial este serviço suporta?
- O que aconteceria se ficasse indisponível por uma hora, um dia ou uma semana?
- Que dados sensíveis trata?
- Quem tem acesso privilegiado e como é revisto?
- Quais fornecedores e integrações são essenciais?
- Que eventos de segurança ou quase acidentes ocorreram?
- Quais controles são manuais, inconsistentes ou difíceis de evidenciar?
- Que mudanças futuras poderão alterar o risco?
- Quais decisões de risco precisam de aprovação executiva?

### Modelo de acompanhamento de tratamento


## 18. Glossário e referências oficiais

NIST SP 800-30 Rev. 1 - Guia para realização de avaliações de risco
Estrutura de segurança cibernética do NIST 2.0
Estrutura de gerenciamento de risco do NIST
Avaliações de risco CISA
Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.


### Tabela / Tabela 1

| Prazo | Significado prático |
| --- | --- |
| Ativo | Um sistema, serviço, processo, pessoa, instalação, conjunto de dados, fornecedor ou capacidade que possui valor. |
| Ameaça | Uma circunstância ou ator com potencial para causar danos. |
| Evento de ameaça | Um evento específico, como roubo de credenciais, execução de ransomware, configuração incorreta da nuvem ou interrupção do fornecedor. |
| Vulnerabilidade | Uma fraqueza que pode ser explorada ou contribuir para danos. |
| Controle | Uma salvaguarda que altera a probabilidade, o impacto ou ambos. |
| Risco inerente | Risco antes de considerar os controles atuais. |
| Risco residual | Risco remanescente após considerar os controles atuais. |
| Apetite pelo risco | A ampla quantidade e tipo de risco que uma organização está disposta a assumir ou reter. |
| Tolerância ao risco | Variação específica aceitável em torno de objetivos ou limites. |

### Tabela / Tabela 2

| Função | Responsabilidades |
| --- | --- |
| Patrocinador executivo | Aprova o escopo, resolve barreiras e aceita ou escala riscos significativos. |
| Proprietário do risco | Possui o objetivo de negócios e decide o tratamento dentro da autoridade delegada. |
| Líder de avaliação | Planeja a avaliação, aplica o método de forma consistente e mantém evidências. |
| Proprietário do sistema ou serviço | Explica arquitetura, dependências, usuários, mudanças e controles atuais. |
| Proprietário do controle | Opera uma salvaguarda e fornece evidências de design e desempenho. |
| Especialistas em segurança e privacidade | Fornecer análises técnicas, jurídicas, de privacidade, segurança e conformidade. |
| Auditoria interna ou revisor independente | Desafia suposições e avalia a qualidade ou garantia. |
| Terceiros | Fornece informações precisas sobre serviços, controles, incidentes e dependências. |

### Tabela / Tabela 3

| Elemento de escopo | Perguntas |
| --- | --- |
| Finalidade comercial | Qual missão, cliente, objetivo jurídico, de segurança ou de receita o serviço suporta? |
| Limite | Quais aplicativos, identidades, redes, locais, assinaturas de nuvem, APIs e endpoints estão incluídos? |
| Dados | Quais dados são coletados, processados, transmitidos, armazenados, registrados ou excluídos? |
| Pessoas | Quem administra, usa, apoia, aprova ou é afetado pelo serviço? |
| Fornecedores | Quais fornecedores, processadores, componentes de código aberto e utilitários são dependências? |
| Horizonte temporal | Estamos avaliando o estado atual, uma mudança proposta, uma aquisição ou uma estratégia plurianual? |
| Critérios | Quais escalas de probabilidade, impacto, risco e aceitação serão utilizadas? |
| Restrições | Quais são as limitações de evidência, tempo, acesso, orçamento ou conhecimento especializado? |

### Tabela / Tabela 4

| Campo de registro de ativo | Exemplo |
| --- | --- |
| Serviço empresarial | Serviço de pagamento on-line ao cliente |
| Proprietário | Diretor de Comércio Digital |
| Criticidade | Alto |
| Dados | Dados de pagamento e contato do cliente |
| RTO/RPO | 4 horas/30 minutos |
| Dependências | Provedor de identidade, plataforma em nuvem, processador de pagamentos, DNS |
| Exposição | Voltado para a Internet |
| Evidência | Diagrama de arquitetura, exportação de CMDB, fluxo de dados, contrato |

### Tabela / Tabela 5

| Fonte de ameaça | Exemplos de eventos de ameaça |
| --- | --- |
| Criminoso externo | Phishing, ransomware, preenchimento de credenciais, extorsão, fraude de pagamento. |
| Estado-nação ou ator avançado | Espionagem, comprometimento da cadeia de abastecimento, operações destrutivas. |
| Insider | Roubo intencional, sabotagem, divulgação não autorizada, desvio de políticas. |
| Ação humana acidental | Configuração incorreta, exclusão incorreta, destinatário errado, compartilhamento inseguro. |
| Fornecedor ou parceiro | Interrupção de serviço, atualização comprometida, acesso fraco, atraso na notificação de violação. |
| Falha tecnológica | Corrupção de armazenamento, expiração de certificado, defeito de software, falha de capacidade. |
| Ambiental ou físico | Perda de energia, incêndio, inundação, roubo, falha de refrigeração. |
| Falha na governança | Propriedade pouco clara, uso de IA não aprovado, retenção ausente, exceções não gerenciadas. |

### Tabela / Tabela 6

| Fonte de evidências | O que isso pode revelar |
| --- | --- |
| Revisão de configuração | Exposição pública, autenticação fraca, permissões excessivas, padrões inseguros. |
| Verificação de vulnerabilidade | Falhas de software conhecidas e patches ausentes. |
| Teste de penetração | Caminhos exploráveis ​​e fraquezas encadeadas dentro do escopo autorizado. |
| Entrevista de controle | Propriedade pouco clara, soluções alternativas manuais, operação inconsistente. |
| Testes de amostra | Aprovações falhadas, revisões incompletas, registros ausentes. |
| Histórico de incidentes | Controles que falharam em condições reais. |
| Contratos e relatórios | Limitações, exclusões, notificação fraca ou compromissos de recuperação de fornecedores. |
| Revisão de arquitetura | Problemas de limite de confiança, segmentação, concentração e ponto único de falha. |

### Tabela / Tabela 7

| Avaliação | Critério de exemplo |
| --- | --- |
| 1 - Raro | Não esperado no período; barreiras fortes; nenhum histórico confiável ou segmentação ativa. |
| 2 - Improvável | Possível, mas requer condições incomuns ou falhas múltiplas. |
| 3 - Possível | Credível e pode ocorrer; existem eventos semelhantes na organização ou setor. |
| 4 - Provável | Esperado em muitas circunstâncias; exposição ativa, tentativas recorrentes ou barreiras fracas. |
| 5 - Quase certo | Esperado repetidamente ou já ocorrendo; altamente exposto e facilmente explorado. |

### Tabela / Tabela 8

| Área de impacto | Perguntas |
| --- | --- |
| Segurança e impacto humano | As pessoas poderiam ser fisicamente prejudicadas, ser-lhes negados serviços essenciais, discriminadas ou expostas a situações de sofrimento grave? |
| Operações | Por quanto tempo o serviço pode ficar indisponível ou degradado? Que alternativas manuais existem? |
| Confidencialidade e privacidade | Que dados poderiam ser expostos, a quem e em que escala? |
| Integridade | Os registros, decisões, modelos, configurações ou dados financeiros poderiam ser alterados? |
| Financeiro | Que resposta, recuperação, fraude, perda de receita, penalidades ou custos contratuais podem ocorrer? |
| Legal e regulatório | Quais consequências de notificação, investigação, litígio ou licenciamento se aplicam? |
| Reputação e confiança | Os clientes, funcionários, parceiros ou o público perderiam a confiança? |
| Estratégico | O evento poderia impedir objetivos, aquisições, entrada no mercado ou transformações críticas? |

### Tabela / Tabela 9

| Avaliação | Critério de exemplo |
| --- | --- |
| 1 - Insignificante | Interrupção mínima; nenhum dado material, consequência legal, de segurança ou financeira. |
| 2 - Menor | Impacto local limitado; recuperação de rotina; pequeno custo ou interrupção curta. |
| 3 – Moderado | Interrupção material nos negócios, problema relatável ou impacto significativo no cliente. |
| 4 - Maior | Interrupção grave, exposição significativa de dados, ação regulatória ou grandes perdas financeiras. |
| 5 - Catastrófico | Ameaça à vida ou a serviços essenciais, falha em toda a empresa ou dano existencial legal/financial. |

### Tabela / Tabela 10

| Probabilidade x Impacto | Nível sugerido |
| --- | --- |
| 1-4 | Baixo |
| 5-9 | Moderado |
| 10-16 | Alto |
| 17-25 | Crítico |

### Tabela / Tabela 11

| Impacto → / Probabilidade ↓ | 1 | 2 | 3 | 4 | 5 |
| --- | --- | --- | --- | --- | --- |
| 5 - Quase certo | 5 milhões | 10h | 15h | 20ºC | 25 C |
| 4 - Provável | 4L | 8 milhões | 12H | 16h | 20ºC |
| 3 - Possível | 3L | 6 milhões | 9 milhões | 12H | 15h |
| 2 - Improvável | 2L | 4L | 6 milhões | 8 milhões | 10h |
| 1 - Raro | 1L | 2L | 3L | 4L | 5 milhões |

### Tabela / Tabela 12

| Dimensão | Perguntas |
| --- | --- |
| Projeto | O controle, se executado conforme projetado, reduziria o cenário declarado? |
| Implementação | Ele é implantado em todo o escopo pretendido? |
| Operação | É realizado de forma consistente e na frequência exigida? |
| Cobertura | Protege todas as identidades, sistemas, locais e fornecedores relevantes? |
| Confiabilidade | É automatizado, monitorado, testado e resistente a bypass? |
| Evidência | A operação pode ser demonstrada com registros confiáveis? |
| Dependências | O controle depende de outro controle que pode falhar? |

### Tabela / Tabela 13

| Eficácia | Descrição |
| --- | --- |
| Eficaz | Adequadamente concebido, implementado, operacional e evidenciado. |
| Parcialmente eficaz | Reduz o risco, mas apresenta lacunas de cobertura, consistência ou evidências. |
| Ineficaz | Não reduz de forma confiável o cenário. |
| Não implementado | Planejado ou obrigatório, mas ausente. |
| Não avaliado | Evidências insuficientes; a incerteza deve ser registrada. |

### Tabela / Tabela 14

| Opção | Usar |
| --- | --- |
| Mitigar | Adicione ou melhore controles para reduzir a probabilidade ou o impacto. |
| Evite | Interrompa a atividade, remova a exposição ou escolha um design diferente. |
| Transferir ou compartilhar | Use seguros, termos contratuais, terceirização ou responsabilidade compartilhada, embora reconheça que a responsabilidade pode permanecer. |
| Aceitar | Reter formalmente o risco dentro da autoridade e tolerância, com justificativa e data de revisão. |

### Tabela / Tabela 15

| Ação fraca | Ação melhorada |
| --- | --- |
| Melhorar o controle de acesso | Até 30 de setembro, migre todo o acesso remoto privilegiado para MFA resistente a phishing, remova contas de administrador compartilhadas e forneça evidências de login e revisão de acesso ao Entra. |
| Servidores de patches | Dentro de 30 dias, corrija vulnerabilidades críticas voltadas para a Internet; reportar exceções semanais com controles compensatórios e prazos aprovados. |
| Treinar usuários | Ofereça treinamento sobre phishing e relatórios com base em funções para 95% dos usuários, teste o comportamento de relatórios e repita o treinamento para grupos de alto risco. |

### Tabela / Tabela 16

| Campo | Finalidade |
| --- | --- |
| ID e título do risco | Referência única e nome conciso. |
| Objectivo e activo empresarial | O que está em risco e por que isso é importante. |
| Declaração de risco | Ameaça, condição, ativo e consequência. |
| Escopo e premissas | Limite, horizonte temporal, exclusões e incerteza. |
| Controles existentes | Salvaguardas relevantes para o cenário. |
| Evidência | Documentos, registros, testes, entrevistas e datas. |
| Probabilidade e impacto inerentes | Avaliações de pré-controle. |
| Eficácia do controlo | Conclusão do projeto e operação. |
| Probabilidade e impacto residual | Classificações pós-controle. |
| Proprietário do risco | Pessoa responsável pela decisão empresarial. |
| Tratamento e proprietário | Ações, marcos, evidências e data de vencimento. |
| Autoridade de aceitação | Pessoa autorizada a aceitar o risco residual. |
| Situação e data de revisão | Gatilho de rastreamento e reavaliação do ciclo de vida. |

### Tabela / Tabela 17

| Campo | Exemplo |
| --- | --- |
| Título | Comprometimento de acesso remoto privilegiado |
| Declaração de risco | Um agente de ameaça pode usar credenciais roubadas contra acesso remoto pela Internet sem MFA resistente a phishing, causando acesso não autorizado, ransomware, interrupção e exposição de dados. |
| Risco inerente | Probabilidade 4; Impacto 5; Crítico 20 |
| Controles existentes | MFA de senha para a maioria dos usuários, registro de VPN, proteção de endpoint. |
| Avaliação de controle | Parcialmente eficaz; contas legadas e administração compartilhada permanecem. |
| Risco residual | Probabilidade 3; Impacto 5; Alto 15 |
| Tratamento | Implante MFA resistente a phishing, remova contas compartilhadas, restrinja locais de origem, crie estações de trabalho com acesso privilegiado e teste a recuperação. |
| Proprietário e data de vencimento | Diretor de Infraestrutura; 30 de setembro de 2026 |
| Gatilho de revisão | Alteração na arquitetura do material, incidente relacionado ou data de vencimento. |

### Tabela / Tabela 18

| Indicador | Exemplo |
| --- | --- |
| Indicador-chave de risco | Porcentagem de contas privilegiadas sem MFA resistente a phishing. |
| Indicador de controle | Porcentagem de sistemas críticos que enviam logs para o SIEM. |
| Indicador de tratamento | Altos riscos vencidos pelo proprietário e pela unidade de negócios. |
| Indicador de exposição | Vulnerabilidades críticas voltadas para a Internet com mais de 15 dias. |
| Indicador de resiliência | Porcentagem de serviços críticos com objetivos de recuperação testados. |

### Tabela / Tabela 19

| Erro | Melhores práticas |
| --- | --- |
| Começando com uma lista de verificação genérica | Comece com o serviço de negócios, o objetivo e o fluxo de dados. |
| Chamando cada descoberta de alto risco | Use critérios definidos e impacto específico do cenário. |
| Igualando conformidade com segurança | Avalie ameaças, controles e consequências comerciais reais. |
| Contando políticas como controles operacionais | Implementação de testes e evidências. |
| Ignorando fornecedores e concentração | Mapeie dependências e pontos de falha comuns. |
| Escondendo a incerteza | Registre evidências, suposições e confiança ausentes. |
| Aceitar riscos sem autoridade | Use limites de aceitação delegados documentados. |
| Deixando o tratamento vago | Defina proprietário, ação, evidência, marco e data de vencimento. |
| Nunca fechando o ciclo | Testar novamente o tratamento e atualizar o risco residual. |

### Tabela / Tabela 20

| ID do risco | Ação | Proprietário | Marco | Data de vencimento | Evidência | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| R-001 | Implantar MFA resistente a phishing | Gerente IAM | Piloto concluído | 30/09/2026 | Configuração + logs de login | Abrir |
| R-002 | Testar recuperação offline | Gerente de Infraestrutura | Exercício de restauração | 15/10/2026 | Relatório de exercício | Planejado |

### Tabela / Tabela 21

| Prazo | Definição |
| --- | --- |
| Risco | Efeito da incerteza nos objetivos; na segurança cibernética, comumente expressa através de probabilidade e impacto. |
| Cenário de risco | Uma descrição estruturada de como um evento de ameaça pode criar consequências. |
| Risco inerente | Risco antes dos controles atuais. |
| Risco residual | Risco após considerar os controles atuais. |
| Projeto de controle | Se um controle é capaz de reduzir o risco declarado. |
| Eficácia operacional | Se o controle funciona consistentemente na prática. |
| Proprietário do risco | Pessoa responsável por gerenciar e decidir sobre um risco. |
| Aceitação de riscos | Decisão autorizada de reter risco residual. |
| KRI | Indicador-chave de risco usado para monitorar mudanças na exposição. |
| Gatilho de reavaliação | Evento ou data que exige que o risco seja revisto novamente. |

## Referências oficiais / Referências oficiais

- [NIST SP 800-30 Rev. 1 - Guia para realização de avaliações de risco](https://csrc.nist.gov/pubs/sp/800/30/r1/final)
- [Estrutura de segurança cibernética do NIST 2.0](https://www.nist.gov/cyberframework)
- [Estrutura de gerenciamento de riscos do NIST](https://csrc.nist.gov/projects/risk-management)
- [Avaliações de risco CISA](https://www.cisa.gov/risk-assessments)
