# Zaiz Facturación — Instrucciones del proyecto

## 1. Objetivo

Zaiz Facturación es un producto SaaS orientado a facilitar la facturación electrónica en República Dominicana.

El objetivo inicial es definir un MVP con las funcionalidades mínimas necesarias para que una empresa pueda operar el proceso de facturación electrónica mediante la integración con un proveedor de servicios autorizado.

El alcance funcional, las integraciones y las decisiones técnicas todavía deben ser descubiertos, documentados y aprobados.

**No asumir que existen requisitos aprobados por el simple hecho de estar descritos en este documento.**

## 2. Idioma

- Toda la comunicación con el usuario debe realizarse en español.
- Los documentos de producto, requisitos, decisiones y especificaciones deben redactarse en español.
- Los identificadores de código, nombres de clases, métodos y propiedades pueden utilizar inglés siguiendo las convenciones del stack tecnológico.
- Conservar la terminología oficial de la DGII cuando corresponda.

## 3. Herramientas y responsabilidades

### BMAD — Descubrimiento y definición

Utilizar las skills de BMAD para:

- Analizar el problema y los objetivos del producto.
- Entrevistar al usuario y descubrir requisitos.
- Identificar actores, procesos y reglas de negocio.
- Elaborar y revisar el Product Brief y el PRD.
- Registrar preguntas abiertas, riesgos, supuestos y decisiones.

Los documentos generados por BMAD son borradores hasta recibir aprobación explícita.

Ubicaciones:
- Skills canónicas: `.agents/skills/`
- Skills disponibles en Claude Code: `.claude/skills/bmad*/`
- Configuración y scripts: `_bmad/`
- Salidas: `_bmad-output/`

### OpenSpec — Especificaciones aprobadas

Utilizar OpenSpec para convertir requisitos aprobados en propuestas y especificaciones verificables.

- Mantener `openspec/specs/` como referencia canónica de los comportamientos aprobados.
- Utilizar `openspec/changes/` para proponer y revisar cambios.
- No interpretar un borrador BMAD como autorización para modificar especificaciones.
- No aplicar cambios sin autorización explícita.

### Claude Code — Ejecución controlada

Claude Code puede investigar, analizar, documentar, diseñar, implementar y probar según la fase autorizada.

No debe comenzar tareas de implementación cuando el usuario solamente haya solicitado análisis o definición.

## 4. Flujo obligatorio

1. **Descubrimiento:** BMAD recopila necesidades, restricciones y preguntas.
2. **Aprobación de requisitos:** el usuario revisa y aprueba el alcance.
3. **Especificación:** OpenSpec documenta los comportamientos aprobados.
4. **Aprobación de implementación:** el usuario autoriza expresamente desarrollar el cambio.
5. **Implementación:** Claude Code desarrolla únicamente lo autorizado.
6. **Verificación:** ejecutar las pruebas pertinentes y reportar resultados.
7. **Cierre:** solicitar autorización antes de realizar commits, pushes o merges.

Una aprobación para analizar no equivale a una aprobación para implementar.

## 5. Reglas sobre facturación electrónica dominicana

- No inventar obligaciones legales, plazos, formatos fiscales, validaciones ni reglas de la DGII.
- Consultar documentación oficial vigente cuando sea necesario establecer requisitos regulatorios.
- Distinguir entre requisitos legales, capacidades del proveedor autorizado y decisiones internas del producto.
- No asumir que el proveedor autorizado admite una API, operación o modalidad de integración sin confirmación.
- Registrar la fuente y fecha de consulta de los requisitos externos.
- Cuando exista incertidumbre, formular una pregunta o registrar el punto como pendiente.
- No incorporar reglas fiscales no verificadas a las especificaciones aprobadas.

## 6. Gestión de decisiones y cambios

- No convertir suposiciones en decisiones.
- Identificar claramente lo aprobado, propuesto y pendiente.
- Evitar duplicar las especificaciones funcionales entre BMAD y OpenSpec.
- Ante contradicciones, señalar el conflicto y solicitar una decisión.
- Mantener trazabilidad entre requisitos, especificaciones y pruebas.

## 7. Restricciones de ejecución

Sin autorización explícita:

- No crear proyectos Angular o .NET.
- No implementar funcionalidades ni generar migraciones de base de datos.
- No instalar ni actualizar dependencias.
- No modificar configuraciones de despliegue, credenciales o infraestructura.
- No ejecutar operaciones destructivas.
- No hacer commits, pushes, merges ni despliegues.
- No modificar archivos fuera del repositorio.

Antes de una modificación importante, explicar qué archivos cambiarán y por qué.

## 8. Seguridad

- Nunca incluir secretos, tokens, claves privadas o credenciales en el repositorio.
- Respetar `.gitignore`.
- No registrar datos fiscales o personales sensibles en logs de depuración.
- Aplicar controles de acceso, validación y auditoría según los requisitos aprobados.
- No asumir que una implementación cumple una obligación fiscal sin validación.

## 9. Estado inicial

El proyecto se encuentra en fase de configuración de herramientas y preparación del descubrimiento.

BMAD y OpenSpec están instalados.

Todavía no existe autorización para implementar el MVP.

El siguiente trabajo funcional debe comenzar por el descubrimiento de requisitos, no por escribir código.
