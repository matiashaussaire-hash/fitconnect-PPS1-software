
# 4. Roles en el Equipo de Desarrollo

La propuesta de roles fue elaborada a partir del análisis del proyecto y de la información obtenida durante las entrevistas con los distintos stakeholders.

| Rol | Cantidad | Responsabilidades principales | ¿Por qué es necesario para FitConnect? |
|------|----------|-------------------------------|----------------------------------------|
| **Analista Funcional** | **1** | Relevar y documentar los requisitos del sistema, mantener la comunicación con los stakeholders y asegurar que las funcionalidades desarrolladas respondan a las necesidades del proyecto. | Permite transformar las necesidades del cliente y de los distintos stakeholders en requisitos claros para el equipo de desarrollo. Gabriel indicó que un analista funcional es suficiente para este proyecto, ya que la visión del producto y las prioridades del MVP se encuentran definidas. |
| **Diseñador UX/UI** | **1** | Diseñar la experiencia de usuario, definir los flujos de navegación y desarrollar interfaces intuitivas. | Es fundamental para cumplir uno de los principales objetivos del proyecto: reducir la fricción durante el onboarding y permitir que un usuario pueda comenzar a entrenar con la menor cantidad de pasos posible. |
| **Desarrollador Front-end Mobile** | **2** | Implementar la interfaz de la aplicación móvil, integrar las funcionalidades del sistema y optimizar la experiencia del usuario. | FitConnect es una aplicación móvil que debe iniciar en menos de tres segundos, funcionar en dispositivos de gama media-baja y ofrecer una experiencia fluida. Gabriel remarcó la importancia de que estos desarrolladores tengan experiencia en desarrollo móvil nativo o cross-platform (React Native o Flutter). |
| **Desarrollador Back-end** | **2** | Desarrollar la lógica de negocio, la gestión de usuarios y entrenadores, el almacenamiento de información, las videollamadas y la integración entre los distintos módulos del sistema. | Además de implementar la lógica del sistema, deben garantizar el manejo seguro de datos sensibles, el cifrado de la información y el cumplimiento de los requisitos legales relevados junto a Mara y Diego (HIPAA, GDPR y seguridad de la información). |
| **QA (Tester)** | **1** | Diseñar y ejecutar pruebas funcionales y no funcionales, detectar errores y verificar que el sistema cumpla los requisitos definidos. | Permite asegurar la calidad del producto antes de cada entrega, verificando tanto las funcionalidades como los requisitos de rendimiento, estabilidad y usabilidad. |
| **DevOps** | **1** | Administrar la infraestructura, automatizar despliegues, monitorear el sistema y garantizar la disponibilidad de la plataforma. | Es necesario para mantener la estabilidad del sistema, asegurar un alto nivel de disponibilidad y colaborar con la implementación de mecanismos de seguridad, monitoreo y recuperación ante fallos, aspectos destacados por Diego durante el relevamiento. |

## ¿Los roles irán rotando durante el proceso de desarrollo?

Consideramos que **los roles no deberían rotar** durante el desarrollo del proyecto.

Cada rol requiere conocimientos técnicos y responsabilidades específicas. Mantener funciones bien definidas favorece la especialización, mejora la calidad del trabajo y permite que cada integrante adquiera experiencia en su área. Si bien el equipo puede colaborar de forma conjunta y compartir conocimientos, cada miembro debería conservar su rol principal para garantizar la continuidad y eficiencia del desarrollo.

## ¿Quién representa al cliente (stakeholder)?

El principal representante del cliente es **Gabriel (Product Manager)**.

Durante el relevamiento fue quien presentó la visión del producto, definió las prioridades del MVP, validó los problemas identificados por el equipo y realizó observaciones sobre la organización del equipo de desarrollo. Por este motivo, actúa como el principal stakeholder del proyecto.

## ¿Quién representa a la alta gerencia de la empresa que desarrolla FitConnect?

Consideramos que **Diego (CTO)** representa a la alta gerencia técnica de la organización.

Durante el relevamiento fue quien definió los lineamientos tecnológicos del proyecto, estableció objetivos de disponibilidad, rendimiento, seguridad, arquitectura y escalabilidad, además de determinar los criterios técnicos que deberán cumplirse durante el desarrollo del MVP.

---

**Fuentes de las decisiones tomadas:**

- [2026_07_02_Gabriel_Equipo_desarrollo.md](./2026_07_02_Gabriel_Equipo_desarrollo.md)
- [2026_06_23_Diego_Arquitectura_mvp.md](./2026_06_23_Diego_Arquitectura_mvp.md)
- [2026_06_19_Mara_verificacion_entrenadores.md](./2026_06_19_Mara_verificacion_entrenadores.md)
