# activemq

![Version: 2.1.0](https://img.shields.io/badge/Version-2.1.0-informational?style=flat-square) ![AppVersion: 5.16.4](https://img.shields.io/badge/AppVersion-5.16.4-informational?style=flat-square)

A Helm chart Providing Apache ActiveMQ.

Please refer to the [documentation](https://github.com/Alfresco/acs-deployment/blob/master/docs/helm/README.md) for information on the Helm charts and deployment instructions.

## Source Code

* <https://github.com/Alfresco/acs-deployment>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kubernetes-charts.alfresco.com/incubator | alfresco-common | 0.1.0-SNAPSHOT |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| adminUser.password | string | `"admin"` |  |
| adminUser.username | string | `"admin"` |  |
| enabled | bool | `true` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"alfresco/alfresco-activemq"` |  |
| image.tag | string | `"5.17.1-jre11-rockylinux8"` |  |
| initContainer.image.pullPolicy | string | `"IfNotPresent"` |  |
| initContainer.image.repository | string | `"busybox"` |  |
| initContainer.image.tag | string | `"1.35.0"` |  |
| initContainer.resources.limits.memory | string | `"10Mi"` |  |
| initContainer.resources.requests.memory | string | `"5Mi"` |  |
| livenessProbe.failureThreshold | int | `1` |  |
| livenessProbe.initialDelaySeconds | int | `130` |  |
| livenessProbe.periodSeconds | int | `20` |  |
| livenessProbe.timeoutSeconds | int | `10` |  |
| nodeSelector | object | `{}` |  |
| persistence.chownWithDynamicProvisioning | bool | `false` |  |
| persistence.existingClaim | string | `"alfresco-volume-claim"` |  |
| persistence.mountPath | string | `"/opt/activemq/data"` |  |
| persistence.subPath | string | `"alfresco-infrastructure/activemq-data"` |  |
| readinessProbe | object | `{"failureThreshold":6,"initialDelaySeconds":60,"periodSeconds":20,"timeoutSeconds":10}` | The ActiveMQ readiness probe is used to check startup only as a failure of the liveness probe later will result in the pod being restarted. |
| replicaCount | int | `1` |  |
| resources.limits.memory | string | `"2048Mi"` |  |
| resources.requests.memory | string | `"512Mi"` |  |
| services.broker.ports.external.amqp | int | `5672` |  |
| services.broker.ports.external.openwire | int | `61616` |  |
| services.broker.ports.external.stomp | int | `61613` |  |
| services.broker.ports.internal.amqp | int | `5672` |  |
| services.broker.ports.internal.openwire | int | `61616` |  |
| services.broker.ports.internal.stomp | int | `61613` |  |
| services.broker.type | string | `"ClusterIP"` |  |
| services.webConsole.ports.external.webConsole | int | `8161` |  |
| services.webConsole.ports.internal.webConsole | int | `8161` |  |
| services.webConsole.type | string | `"NodePort"` |  |