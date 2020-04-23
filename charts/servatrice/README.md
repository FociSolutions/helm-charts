servatrice
==========
deploys the cockatrice server called servatrice along with the MySql database

Current chart version is `0.1.0`

## Chart Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kubernetes-charts.storage.googleapis.com | mysql | 1.6.2 |

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| audit.enableAudit | bool | `true` |  |
| audit.enableForgotPasswordAudit | bool | `true` |  |
| audit.enableRegistrationAudit | bool | `true` |  |
| authentication.method | string | `"sql"` |  |
| authentication.password | string | `nil` |  |
| authentication.regOnly | bool | `false` |  |
| database.type | string | `"mysql"` |  |
| forgotPassword.body | string | `"Hi %username, sorry to hear you forgot your password on our Cockatrice server\r\nHere's the token to use to reset your account password:\r\n\r\n%token\r\n\r\nHappy gaming!"` |  |
| forgotPassword.enable | bool | `false` |  |
| forgotPassword.enableChallenge | bool | `false` |  |
| forgotPassword.subject | string | `"Cockatrice forgot password token"` |  |
| forgotPassword.tokenLife | int | `60` |  |
| fullnameOverride | string | `""` |  |
| game.allowCreateAsJudge | bool | `false` |  |
| game.maxGameInactivityTime | int | `120` |  |
| game.storeReplays | bool | `true` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"blastdan/servatrice"` |  |
| imagePullSecrets | list | `[]` |  |
| logging.enableLogQuery | bool | `false` |  |
| logging.logUserMsgChat | bool | `false` |  |
| logging.logUserMsgGame | bool | `false` |  |
| logging.logUserMsgIsl | bool | `false` |  |
| logging.logUserMsgRoom | bool | `false` |  |
| mysql.mysqlDatabase | string | `"servatrice"` |  |
| mysql.mysqlUser | string | `"servatrice"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| registration.emailProviderBlacklist | string | `nil` |  |
| registration.enabled | bool | `false` |  |
| registration.maxAccountsPerEmail | int | `1` |  |
| registration.requireEmail | bool | `true` |  |
| registration.requireEmailActivation | bool | `false` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| rooms.method | string | `"sql"` |  |
| security.commandCountingInterval | int | `10` |  |
| security.enableMaxUserLimit | bool | `false` |  |
| security.maxCommandCountPerInterval | int | `20` |  |
| security.maxGamesPerUser | int | `5` |  |
| security.maxMessageCountPerInterval | int | `10` |  |
| security.maxMessageSizePerInterval | int | `1000` |  |
| security.maxUsersPerAddress | int | `4` |  |
| security.maxUsersTcpL | int | `500` |  |
| security.maxUsersTotal | int | `500` |  |
| security.maxUsersWebSocket | int | `500` |  |
| security.messageCountingInterval | int | `10` |  |
| security.trustedSources | string | `"127.0.0.1,::1"` |  |
| securityContext | object | `{}` |  |
| server.clientKeepAlive | int | `1` |  |
| server.host | string | `"any"` |  |
| server.id | int | `1` |  |
| server.idleClientTimeout | int | `3600` |  |
| server.logFile | string | `"server.log"` |  |
| server.logFilters | string | `nil` |  |
| server.maxPlayerInactivityTime | int | `15` |  |
| server.name | string | `"My Cockatrice server"` |  |
| server.numberPools | int | `1` |  |
| server.officialWarnings | string | `"Flamming,Spamming,Causing Drama,Abusive Language"` |  |
| server.port | int | `4747` |  |
| server.requireClientId | bool | `false` |  |
| server.requiredFeatures | string | `""` |  |
| server.statusUpdate | int | `15000` |  |
| server.websocketHost | string | `"any"` |  |
| server.websocketNumberPools | int | `1` |  |
| server.websocketPort | int | `4748` |  |
| server.writeLog | int | `1` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| smtp.acceptAllCerts | bool | `false` |  |
| smtp.body | string | `"Hi %username, thank our for registering on our Cockatrice server\r\nHere's the activation token you need to supply for activating your account:\r\n\r\n%token\r\n\r\nHappy gaming!"` |  |
| smtp.connection | string | `"tcp"` |  |
| smtp.email | string | `"email=root@localhost"` |  |
| smtp.enableInternalSmtpClient | bool | `true` |  |
| smtp.host | string | `"localhost"` |  |
| smtp.name | string | `"Cockatrice server"` |  |
| smtp.password | string | `"foobar"` |  |
| smtp.port | int | `25` |  |
| smtp.subject | string | `"Cockatrice server account activation token"` |  |
| smtp.username | string | `"root@localhost"` |  |
| tolerations | list | `[]` |  |
| users.allowLowerCase | bool | `true` |  |
| users.allowNumerics | bool | `true` |  |
| users.allowPunctuationPrefix | bool | `false` |  |
| users.allowUpperCase | bool | `true` |  |
| users.allowedPunctuation | string | `"_.-"` |  |
| users.disallowedRegExp | string | `""` |  |
| users.disallowedWords | string | `"admin"` |  |
| users.maxNameLength | int | `12` |  |
| users.minNameLength | int | `6` |  |
| users.minPasswordLength | int | `6` |  |
