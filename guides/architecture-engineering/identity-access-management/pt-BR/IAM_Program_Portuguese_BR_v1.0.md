# Como construir um programa de gerenciamento de identidade e acesso

> **Status da tradução:** esta edição em português brasileiro foi preparada com assistência de tradução automática e revisão estrutural. Antes de usar o conteúdo para decisões importantes, recomenda-se revisão por uma pessoa fluente em português e familiarizada com o tema técnico.

COMO CONSTRUIR UM PROGRAMA DE GESTÃO DE IDENTIDADE E ACESSO
Um manual de implementação conciso e prático
Alberto (Al) Leiva
Versão 1.0 - julho de 2026

## Propósito

Use este manual para trabalhos defensivos legais, autorizados. Adapte os controles ao risco organizacional, às obrigações legais, às necessidades de acessibilidade e aos recursos disponíveis.

## Fundações do programa

- Trate a identidade como um controle de segurança e uma capacidade de negócios.
- Definir fontes autorizadas, tipos de identidade, propriedade, políticas, necessidades de garantia e eventos de ciclo de vida.
- Inclui funcionários, prestadores de serviços, clientes, parceiros, cargas de trabalho, dispositivos, contas de serviço, APIs e agentes de IA.

## Ciclo de vida do marceneiro, do movimentador e do abandono

- Crie acesso a partir de funções comerciais aprovadas e dados de identidade verificados.
- Atualize o acesso imediatamente quando as funções mudarem.
- Desative acessos, sessões, tokens, certificados e credenciais físicas na partida.

## Autenticação

- Use MFA resistente a phishing para acesso privilegiado e de alto risco.
- Aplicar autenticação baseada em risco e procedimentos de recuperação segura.
- Proteja o registro, a substituição do autenticador e as redefinições do suporte técnico contra a engenharia social.

## Autorização e privilégio mínimo

- Use controles baseados em funções e atributos quando apropriado.
- Separar funções incompatíveis e exigir aprovação para direitos sensíveis.
- Use acesso privilegiado just-in-time e por tempo limitado.

## Identidades privilegiadas e de máquina

- Armazene credenciais privilegiadas e monitore sessões administrativas.
- Contas de serviço de inventário, segredos, certificados, chaves, cargas de trabalho e identidades não humanas.
- Atribua proprietários, alterne credenciais, restrinja o uso e remova identidades abandonadas.

## Acesse avaliações e governança

- Revise o acesso de alto risco com mais frequência.
- Dê aos revisores um contexto claro e exija decisões baseadas em evidências.
- Rastreie contas órfãs, acesso excessivo, combinações tóxicas, remoções malsucedidas e exceções.

## Federação, privacidade e roteiro

- Valide confiança, reivindicações, chaves de assinatura, alvos de redirecionamento, controles de sessão e responsabilidades do parceiro.
- Minimize os dados de identidade e forneça opções de autenticação acessíveis.
- Dias 1 a 30: controles de estoque e saídas. Dias 31 a 60: MFA, acesso privilegiado e análises. Dias 61-90: automação, identidade da máquina, métricas e testes.

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

- NIST SP 800-63-4: https://www.nist.gov/publications/nist-sp-800-63-4-digital-identity-guidelines
- Centro de recursos NIST IAM: https://www.nist.gov/identity-and-access-management
-NIST SP 800-207: https://csrc.nist.gov/pubs/sp/800/207/final

## Licença

Copyright © 2026 Alberto (Al) Leiva. Licenciado sob CC BY-NC-SA 4.0.
