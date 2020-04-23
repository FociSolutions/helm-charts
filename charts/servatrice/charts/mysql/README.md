mysql
=====
Fast, reliable, scalable, and easy to use open-source relational database system.

Current chart version is `1.6.2`

Source code can be found [here](https://www.mysql.com/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| args | list | `[]` |  |
| busybox.image | string | `"busybox"` |  |
| busybox.tag | string | `"1.29.3"` |  |
| configurationFiles | object | `{}` |  |
| configurationFilesPath | string | `"/etc/mysql/conf.d/"` |  |
| deploymentAnnotations | object | `{}` |  |
| extraInitContainers | string | `"# - name: do-something\n#   image: busybox\n#   command: ['do', 'something']\n"` |  |
| extraVolumeMounts | string | `"# - name: extras\n#   mountPath: /usr/share/extras\n#   readOnly: true\n"` |  |
| extraVolumes | string | `"# - name: extras\n#   emptyDir: {}\n"` |  |
| image | string | `"mysql"` |  |
| imagePullPolicy | string | `"IfNotPresent"` |  |
| imageTag | string | `"5.7.28"` |  |
| initContainer.resources.requests.cpu | string | `"10m"` |  |
| initContainer.resources.requests.memory | string | `"10Mi"` |  |
| initializationFiles | object | `{}` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.annotations | object | `{}` |  |
| metrics.enabled | bool | `false` |  |
| metrics.flags | list | `[]` |  |
| metrics.image | string | `"prom/mysqld-exporter"` |  |
| metrics.imagePullPolicy | string | `"IfNotPresent"` |  |
| metrics.imageTag | string | `"v0.10.0"` |  |
| metrics.livenessProbe.initialDelaySeconds | int | `15` |  |
| metrics.livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.readinessProbe.initialDelaySeconds | int | `5` |  |
| metrics.readinessProbe.timeoutSeconds | int | `1` |  |
| metrics.resources | object | `{}` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `true` |  |
| persistence.size | string | `"8Gi"` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `5` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| securityContext.enabled | bool | `false` |  |
| securityContext.fsGroup | int | `999` |  |
| securityContext.runAsUser | int | `999` |  |
| service.annotations | object | `{}` |  |
| service.port | int | `3306` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.create | bool | `false` |  |
| ssl.certificates | string | `nil` |  |
| ssl.enabled | bool | `false` |  |
| ssl.secret | string | `"mysql-ssl-certs"` |  |
| strategy.type | string | `"Recreate"` |  |
| testFramework.enabled | bool | `true` |  |
| testFramework.image | string | `"dduportal/bats"` |  |
| testFramework.tag | string | `"0.4.0"` |  |
| tolerations | list | `[]` |  |
