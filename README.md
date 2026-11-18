# N8n-Wazuh-SecurityAgent

Laboratorio de ciberseguridad en desarrollo sobre una única máquina Ubuntu, con Wazuh y n8n desplegados en Docker.

## Objetivo

Construir un agente de ciberseguridad autónomo. El proyecto documentará progresivamente el despliegue del laboratorio, las integraciones, las pruebas y los resultados.

Las capacidades de análisis, decisión y respuesta del agente, así como su grado de autonomía, están pendientes de definir e implementar.

## Estado actual

Estado actualizado el **18 de noviembre de 2026** a partir de los avances comunicados por el autor.

| Componente | Ubicación prevista | Estado confirmado |
|---|---|---|
| Ubuntu | Máquina anfitriona del laboratorio | Entorno del proyecto |
| Docker | Ubuntu | Instalado |
| Wazuh | Docker | Instalado |
| n8n | Docker | Instalado |
| Red Docker `soc-net` | Docker | Incluida en el diseño; configuración pendiente de documentar |
| auditd | Ubuntu, fuera de Docker | Instalado |
| Atomic Red Team | Ubuntu, fuera de Docker | Instalado |
| Wazuh en el anfitrión | Ubuntu, fuera de Docker | Incluido en el diseño; función como agente e instalación pendientes de confirmar |
| Postman | Ubuntu, fuera de Docker | Incluido en el diseño; instalación pendiente de confirmar |

El autor ha confirmado la instalación de Wazuh, n8n, auditd y Atomic Red Team. Las configuraciones, la conectividad y el funcionamiento conjunto se documentarán con evidencias conforme avance el proyecto.


### Función prevista de los componentes

| Componente | Función en el diseño |
|---|---|
| Wazuh Manager | Procesamiento de eventos y generación de alertas |
| Wazuh Indexer | Indexación y almacenamiento de los datos de Wazuh |
| Wazuh Dashboard | Consulta y visualización de la información de seguridad |
| n8n | Orquestación de flujos de automatización e integraciones |
| auditd | Generación de registros de auditoría del sistema Ubuntu |
| Atomic Red Team | Ejecución de pruebas controladas para evaluar la detección |
| Agente Wazuh, pendiente de confirmar | Recogida y envío de eventos del anfitrión |
| Postman | Pruebas de peticiones e integraciones mediante API |

Estas funciones describen el diseño previsto. Las integraciones entre componentes todavía no están documentadas como operativas.


## Registro de avances

| Fecha | Avance |
|---|---|
| 2026-11-17 | Documentación inicial del objetivo, la arquitectura prevista y el estado comunicado: Docker, Wazuh y n8n instalados; auditd y Atomic Red Team pendientes. |
| 2026-11-18 | Instalación de auditd y Atomic Red Team en el anfitrión Ubuntu, fuera de Docker. |

## Origen de la idea

La idea de este proyecto está inspirada en el repositorio [Atlantium-AI/wazuh-n8n-lab-setup](https://github.com/Atlantium-AI/wazuh-n8n-lab-setup), que se reconoce como referencia de partida para este laboratorio.
