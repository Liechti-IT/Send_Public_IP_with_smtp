# IP Notification Script

Das Skript wurde von Pascal Liechti in der Schweiz erstellt und dient dazu, die öffentliche IP-Adresse des Hosts zu ermitteln und diese Informationen per E-Mail zu senden.

## Voraussetzungen

- PowerShell muss installiert und konfiguriert sein.
- Zugriff auf einen SMTP-Server für den E-Mail-Versand.

## Verwendung

Das Skript führt die folgenden Schritte aus:

1. **Hostname und aktuelles Datum abrufen:** Die Variablen `$Hostname` und `$TimeDate` werden mit diesen Informationen gefüllt.
2. **Öffentliche IP abrufen:** Die öffentliche IP-Adresse wird mit `Invoke-WebRequest` von http://wtfismyip.com abgerufen und in der Variable `$MyIP` gespeichert.
3. **E-Mail senden:** Eine E-Mail mit der öffentlichen IP, dem Hostnamen und der aktuellen Zeit wird an die angegebene E-Mail-Adresse gesendet.

## Anpassung

Sie müssen die folgenden Variablen im Skript ändern, um es an Ihre Bedürfnisse anzupassen:

- `$to`: E-Mail-Adresse, an die die Benachrichtigung gesendet werden soll.
- `$from`: E-Mail-Adresse, von der die Benachrichtigung gesendet wird.
- `$Username`: Benutzername für den SMTP-Server.
- `$Password`: Passwort für den SMTP-Server.
- `$server`: SMTP-Serveradresse (z. B. "smtp.gmail.com").
- `$port`: SMTP-Port (standardmäßig 587).

## Hinweis

- Verwenden Sie dieses Skript mit Vorsicht, besonders wenn Sie sensible Informationen wie E-Mail-Anmeldedaten im Skript selbst speichern.
- Es wird empfohlen, dieses Skript in einer sicheren und kontrollierten Umgebung zu verwenden.
- Die E-Mail-Anmeldedaten sollten sicher gespeichert werden. Es ist nicht ratsam, sie direkt im Skript zu speichern.

## Lizenz

Dieses Skript wurde von Pascal Liechti erstellt und steht zur freien Verwendung zur Verfügung. Bitte achten Sie auf korrekte Nutzung und Sicherheit.
