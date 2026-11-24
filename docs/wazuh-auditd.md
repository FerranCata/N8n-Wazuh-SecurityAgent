# Recogida de registros de auditd con el agente Wazuh

## Cambio realizado

Se editó la configuración del agente Wazuh que corre en el anfitrión Ubuntu, fuera de Docker, para que recoja los registros locales de auditd.

## Configuración de referencia

En una instalación estándar, el archivo de configuración del agente es `/var/ossec/etc/ossec.conf`. Wazuh documenta este bloque para indicar la ruta del registro y su formato:

```xml
<localfile>
  <log_format>audit</log_format>
  <location>/var/log/audit/audit.log</location>
</localfile>
```

Para aplicar un cambio en ese archivo, se reinicia el servicio del agente con `sudo systemctl restart wazuh-agent`.

## Verificación en el laboratorio

La configuración del agente está hecha según lo comunicado por el autor. Queda pendiente incorporar la captura del archivo editado y documentar la comprobación de que llegan eventos de auditd a Wazuh.

[Configuración oficial de Wazuh para auditd](https://documentation.wazuh.com/current/user-manual/capabilities/system-calls-monitoring/audit-configuration.html)
