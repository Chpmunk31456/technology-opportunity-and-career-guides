# Seguridad práctica de IA en Azure

## Cómo proteger Microsoft Foundry, Copilot, Purview, Entra ID, RAG, agentes y MCP

**Autor:** Alberto (Al) Leiva  
**Versión:** 1.0 - Julio de 2026  
**Licencia:** CC BY-NC-SA 4.0

> La seguridad humana es lo primero. Ninguna prueba, fecha de entrega, objetivo empresarial o experimento técnico es más importante que la seguridad, la dignidad, la privacidad y los derechos de las personas afectadas por un sistema de IA.

## Contenido

1. Fundamentos de seguridad de IA en Azure
2. Responsabilidad compartida y modelado de amenazas
3. Arquitectura segura de referencia
4. Identidad y acceso con Microsoft Entra ID
5. Aislamiento de red y conectividad privada
6. Protección de datos con Microsoft Purview
7. Seguridad de proyectos en Microsoft Foundry
8. Protección de modelos, instrucciones y contenido
9. Sistemas RAG seguros
10. Agentes de IA e identidades no humanas
11. Seguridad de servidores y herramientas MCP
12. Seguridad y gobierno de Copilot
13. Defender for Cloud y postura continua
14. Pruebas, evaluación y red teaming
15. Registros, monitoreo y respuesta a incidentes
16. Gobierno, cumplimiento y evidencia
17. Hoja de ruta de 30, 60 y 90 días
18. Lista de preparación para producción
19. Glosario
20. Referencias oficiales

## 1. Fundamentos

Una solución de IA en Azure incluye identidades, aplicaciones, redes, instrucciones, datos, índices, almacenamiento, API, agentes, herramientas, monitoreo y decisiones humanas. Proteja todo el sistema, no solamente el modelo.

Principios:

- Inventariar cada activo y propietario.
- Usar Entra ID e identidades administradas.
- Aplicar privilegio mínimo.
- Usar conectividad privada y egreso controlado.
- Clasificar y proteger los datos.
- Tratar instrucciones, contenido recuperado, herramientas y resultados como no confiables.
- Probar antes de publicar y después de cambios.
- Monitorear y conservar evidencia.

## 2. Responsabilidad compartida y amenazas

El cliente es responsable de configuración, identidades, aplicaciones, datos, instrucciones, herramientas, monitoreo, gobierno y decisiones. Pregunte quién puede cambiar, cargar, desplegar o ejecutar; qué datos sensibles están presentes; qué podría hacer un agente comprometido; y cuál es el radio máximo de impacto.

## 3. Arquitectura segura

Use Entra ID, Azure RBAC, identidades administradas, puntos de conexión privados, DNS privado, egreso controlado, datos protegidos, Purview, Defender for Cloud y monitoreo centralizado.

## 4. Identidad y acceso

- MFA y Acceso condicional.
- Privileged Identity Management.
- Cuentas administrativas separadas.
- Identidades administradas para cargas de Azure.
- Federación de identidad para CI/CD compatible.
- Permisos en el alcance más reducido.
- Revisión de plano de administración y de datos.

## 5. Red

- Deshabilitar acceso público cuando sea posible.
- Usar puntos privados para Foundry, Storage, Search, Key Vault y bases de datos.
- Validar DNS privado.
- Controlar egreso.
- Permitir solo destinos necesarios.
- Revisar toda la cadena de dependencias.

## 6. Microsoft Purview

Inventarie, clasifique y proteja datos de instrucciones, fundamentación, evaluación y registros. Use etiquetas, DLP y capacidades actuales de DSPM. Registre excepciones y controles compensatorios.

## 7. Microsoft Foundry

Separe entornos, use infraestructura como código, restrinja despliegues y conexiones, habilite diagnóstico, aplique políticas, presupuestos y límites, y guarde secretos inevitables en Key Vault.

## 8. Modelos, instrucciones y contenido

- Separe instrucciones del sistema, entrada del usuario, contenido recuperado y resultados de herramientas.
- Trate documentos como datos, no como instrucciones.
- Aplique autorización fuera del modelo.
- Valide parámetros estructurados.
- Use controles de contenido y ataques de instrucciones.
- Exija aprobación para acciones de alto impacto.
- Pruebe jailbreaks, inyección indirecta y exfiltración.

## 9. RAG seguro

Aplique autorización en tiempo de consulta, conserve permisos de origen, use filtrado de seguridad, separe datos sensibles, analice archivos, registre procedencia, limite contexto, devuelva citas y monitoree enumeración.

## 10. Agentes

Cada agente debe tener identidad y permisos mínimos. Separe lectura de escritura. El modelo propone; la lógica confiable autoriza.

## 11. MCP

Inventarie servidores, autentique y cifre, autorice por herramienta, valide esquemas, permita solo destinos aprobados, ejecute con permisos mínimos, registre llamadas y exija aprobación para acciones de alto impacto.

## 12. Copilot

Corrija permisos excesivos y datos compartidos en exceso antes de ampliar su uso. Aplique etiquetas, DLP, control de complementos y agentes, capacitación y monitoreo.

## 13. Defender for Cloud

Use Defender para descubrimiento, postura, rutas de ataque y protección frente a amenazas en servicios compatibles. Asigne hallazgos, integre alertas y valide cobertura después de cambios.

## 14. Pruebas

Pruebe acceso, inyección, datos, RAG, herramientas, aplicación, abuso, disponibilidad y factores humanos. Registre comportamiento esperado, resultado, versión, severidad, propietario y nueva prueba.

## 15. Monitoreo e incidentes

Registre autenticación, cambios, invocaciones, herramientas, bloqueos, recuperación, cuotas y alertas. Evite conservar contenido sensible completo sin justificación.

Pasos: identificar, contener, conservar evidencia, evaluar impacto, revocar credenciales, corregir permisos, limpiar contenido, reparar controles, notificar, volver a probar y documentar.

## 16. Gobierno y evidencia

Mantenga inventario, propietarios, propósito, usos prohibidos, diagramas, clasificación, privacidad, amenazas, controles, evaluaciones, supervisión humana, monitoreo, cambios y retiro.

## 17. Hoja de ruta

### Primeros 30 días
Inventariar, identificar exposición, habilitar registros, eliminar recursos abandonados y crear un estándar mínimo.

### Días 31 a 60
Migrar a identidades administradas, reducir RBAC, implementar conectividad privada, clasificar datos, configurar DLP y probar RAG, agentes y MCP.

### Días 61 a 90
Automatizar políticas y evidencia, integrar alertas, establecer revisiones, crear métricas y capacitar.

## 18. Lista de preparación

- [ ] Propietarios identificados
- [ ] Propósito y usos prohibidos
- [ ] Clasificación de datos
- [ ] Modelo de amenazas
- [ ] Entra e identidades administradas
- [ ] RBAC mínimo
- [ ] Red privada probada
- [ ] Key Vault
- [ ] Purview y retención
- [ ] RAG con filtrado
- [ ] Agentes y MCP aprobados
- [ ] Aprobación de alto impacto
- [ ] Controles de contenido probados
- [ ] Defender y monitoreo
- [ ] Guía de incidentes
- [ ] Reversión y apagado
- [ ] Accesibilidad y supervisión humana
- [ ] Aprobación final

## 19. Glosario

- **Agente:** componente que recupera información, llama herramientas y ejecuta acciones.
- **DSPM:** administración de la postura de seguridad de datos.
- **Foundry:** plataforma de Microsoft Azure para aplicaciones y agentes de IA.
- **Identidad administrada:** identidad de carga de trabajo administrada por Azure.
- **MCP:** Model Context Protocol.
- **Inyección de instrucciones:** entrada que intenta anular reglas, revelar datos o abusar de herramientas.
- **RAG:** generación aumentada por recuperación.
- **Filtrado de seguridad:** recuperación según la autorización del usuario.

## 20. Referencias oficiales

- [Mejores prácticas de seguridad de IA en Azure](https://learn.microsoft.com/azure/security/fundamentals/ai-security-best-practices)
- [Línea base de seguridad de Microsoft Foundry](https://learn.microsoft.com/security/benchmark/azure/baselines/azure-ai-foundry-security-baseline)
- [Aislamiento de red de Microsoft Foundry](https://learn.microsoft.com/azure/foundry/how-to/configure-private-link)
- [RBAC de Microsoft Foundry](https://learn.microsoft.com/azure/foundry/concepts/rbac-foundry)
- [Identidades administradas](https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/overview)
- [Microsoft Purview para IA](https://learn.microsoft.com/purview/ai-microsoft-purview)
- [DSPM para IA](https://learn.microsoft.com/purview/dspm-for-ai)
- [Defender for Cloud y postura de IA](https://learn.microsoft.com/azure/defender-for-cloud/ai-security-posture)
- [Protección contra amenazas de IA](https://learn.microsoft.com/azure/defender-for-cloud/ai-threat-protection)
- [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/overview)
- [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)

Copyright © 2026 Alberto (Al) Leiva.
