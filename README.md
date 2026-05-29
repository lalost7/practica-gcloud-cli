# Práctica: Introducción a la Infraestructura en la Nube

## Alumno

Jose Eduardo Santos Toribio

# Objetivo

Realizar consultas básicas de auditoría utilizando Google Cloud CLI para conocer zonas disponibles, tipos de máquinas virtuales y reglas de firewall en Google Cloud.

# Paso 1: Filtrado geográfico

Se utilizó el siguiente comando:

```bash
gcloud compute zones list --filter="status:UP" --limit=5
```

Este comando permitió visualizar zonas activas disponibles en Google Cloud.

# Paso 2: Auditoría de hardware

Se ejecutó el comando:

```bash
gcloud compute machine-types list --filter="zone:us-central1-a AND name:e2-*" --limit=5
```

Con este comando se listaron máquinas virtuales de la familia e2 disponibles en la zona us-central1-a.

Las máquinas e2 son utilizadas frecuentemente en servicios cloud debido a su bajo costo y eficiencia.

# Paso 3: Auditoría de reglas de firewall

Se ejecutó el siguiente comando:

```bash
gcloud compute firewall-rules list
```

Las reglas mostradas permiten tráfico SSH por el puerto 22, RDP por el puerto 3389 y tráfico ICMP para conectividad de red.

# Evidencia

Se adjunta captura de pantalla del resultado obtenido en la terminal de Ubuntu.

# Conclusión

La práctica permitió conocer comandos básicos de Google Cloud CLI para consultar infraestructura cloud utilizando filtros y límites desde terminal.

También se comprendió la importancia de las reglas de firewall y de la identificación de recursos disponibles antes de desplegar infraestructura.

# Fuentes

Google Cloud Documentation:
https://cloud.google.com/docs

Google Cloud CLI:
https://cloud.google.com/sdk/gcloud

Compute Engine:
https://cloud.google.com/compute/docs
