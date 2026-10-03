# 06 - Drivers arquitectónicos

| ID | Driver arquitectónico | Origen | ¿Por qué influye en la arquitectura? |
|---|---|---|---|
| DA01 | Soportar un incremento importante de usuarios durante campañas comerciales. | AC03 - Escalabilidad | Influye en la estrategia de escalamiento y despliegue. |
| DA02 | Mantener tiempos de respuesta adecuados con alta concurrencia. | AC01 - Rendimiento | Influye en la comunicación entre componentes, procesamiento y almacenamiento. |
| DA03 | Proteger los datos de usuarios y operaciones de compra. | AC04 - Seguridad | Influye en autenticación, autorización y protección de datos. |
| DA04 | Integrarse con una pasarela de pago externa mediante una API. | RC04 - Pasarela de pago | Condiciona la comunicación e integración con servicios externos. |
| DA05 | Utilizar una API REST entre frontend y backend. | RC03 - API REST | Limita las alternativas de comunicación entre las partes del sistema. |
| DA06 | Integrarse con el ERP, envío y facturación. | RC05, RC06, RC07 | Exige una capa clara de integración con sistemas externos. |
| DA07 | Facilitar cambios sin afectar otros módulos. | AC05 - Mantenibilidad | Justifica la separación por capas y módulos. |
| DA08 | El sistema debe permitir modificar funcionalidades sin afectar innecesariamente otros módulos. | AC05 - Mantenibilidad | Influye en la separación de responsabilidades, modularidad y dependencias internas. |

## Evaluación de candidatos
| Fuente | Elemento | ¿Driver? |
|---|---|---|
| Requisito funcional | RF09 Procesar pago | Sí |
| Requisito funcional | RF01 Buscar productos | No |
| Atributo de calidad | AC04 Seguridad | Sí |
| Atributo de calidad | AC05 Mantenibilidad | Sí |
| Restricción | RC04 Pasarela de pago | Sí |
| Restricción | RC02 Control de versiones | No |