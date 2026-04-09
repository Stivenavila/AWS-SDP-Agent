# AWS SDP Power for Kiro

> Kiro Power para documentar y validar casos de éxito del **AWS Service Delivery Program (SDP)** — diseñado para equipos de AWS Partners que necesitan crear customer references para obtener y mantener designaciones APN.

---

## ¿Qué hace este Power?

Cuando mencionas palabras clave como **SDP**, **caso de éxito**, **customer reference** o **APN** en Kiro, este power se activa automáticamente y convierte al agente en un experto en documentación del AWS Service Delivery Program.

El agente puede:

- Leer documentos del proyecto (propuestas, actas de cierre, memorias técnicas) y extraer la información relevante
- Redactar cada campo del formulario SDP con el nivel de detalle que AWS espera
- Construir la tabla de servicios AWS con el rol específico de cada servicio en la solución
- Validar el caso antes de enviarlo a AWS usando un checklist completo
- Generar el documento Word final listo para entregar

---

## Instalación

### Opción A — Desde Kiro IDE (recomendado)

1. Abre el panel de **Powers** en Kiro
2. Haz clic en **"Add power from GitHub"**
3. Pega la URL de este repositorio
4. Kiro instala y registra el power automáticamente

### Opción B — Desde ruta local

```bash
git clone https://github.com/Stivenavila/AWS-SDP-Agent.git
```

1. Abre el panel de **Powers** en Kiro
2. Haz clic en **"Add power from Local Path"**
3. Selecciona la carpeta `power-aws-sdp/`

---

## Activación

El power se activa automáticamente cuando mencionas cualquiera de estas palabras clave en tu conversación con Kiro:

`SDP` · `Service Delivery Program` · `caso de éxito` · `customer reference` · `APN` · `AWS partner` · `designación AWS` · `referencia de cliente` · `formulario SDP` · `APN validation`

---

## Estructura

```
power-aws-sdp/
├── POWER.md                        # Entrada principal y keywords de activación
└── steering/
    ├── workflow-redaccion.md       # Proceso paso a paso para redactar desde documentos
    ├── campos-detalle.md           # Guía campo por campo con ejemplos y errores comunes
    ├── resultados-banco.md         # Banco de métricas y outcomes por tipo de SDP
    └── checklist-validacion.md     # Validación completa antes de enviar a AWS
```

---

## SDPs soportados

| SDP | Servicios AWS cubiertos |
|---|---|
| **Networking** | VPC, Transit Gateway, Direct Connect, VPN Site-to-Site, Route 53, WAF, Network Firewall, CloudFront |
| **Containers EKS** | EKS, ECR, ELB, VPC, IAM, CloudWatch |
| **Containers ECS** | ECS, ECR, Fargate, ELB, VPC |
| **Serverless** | Lambda, API Gateway, DynamoDB, S3, CloudWatch |
| **Database** | RDS, Aurora, VPC, Security Groups, CloudWatch |
| **Security** | IAM, CloudTrail, Config, GuardDuty, Security Hub, WAF |
| **Migration** | MGN, DMS, S3, EC2, VPC |

---

## Ejemplo de uso

```
Usuario: Tengo los documentos de un cliente y necesito llenar el formulario SDP de Networking

Kiro: [power aws-sdp activado]
      Entendido. Para redactar el caso de éxito necesito revisar los documentos
      del proyecto. ¿Puedes compartir la memoria técnica, el acta de cierre
      y la propuesta económica? Con eso extraigo fechas, servicios AWS,
      el desafío del cliente y los resultados para completar todos los campos
      del formulario SDP...
```

---

## Campos del formulario SDP cubiertos

- ✅ Name of the Publicly Available Case Study
- ✅ Desafío del cliente
- ✅ Solución propuesta
- ✅ Aplicaciones o soluciones de terceros utilizadas
- ✅ Cómo se utiliza AWS como parte de la solución
- ✅ Fecha de inicio del compromiso
- ✅ Fecha de finalización del compromiso
- ✅ Fecha en que el proyecto entró en producción
- ✅ Resultado(s) / Outcomes
- ✅ Diagramas de arquitectura (guía de qué adjuntar)

---

## Reglas críticas que el agente siempre respeta

- **Nunca inventa datos** — AWS verifica manualmente cada caso con el cliente
- **Siempre incluye Account IDs** cuando están disponibles
- **Exige diagrama de arquitectura** — sin él el caso puede ser rechazado
- **Redacta desde la perspectiva del cliente** — lenguaje que el cliente reconocería como suyo
- **Prioriza métricas medibles** sobre beneficios genéricos

---

## Autor

Desarrollado por el equipo de Cloud Architecture de **ITERA** — AWS Partner con múltiples designaciones SDP activas.

---

## Licencia

MIT
