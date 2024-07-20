---
description: Dinge, die Sie Ihren Kunden empfehlen sollten, sich dessen bewusst zu sein, wenn sie mit den Audience Manager-APIs arbeiten.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API-Anforderungen und Recommendations
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# API-Anforderungen und Recommendations {#api-requirements-and-recommendations}

Dinge, die Sie Ihren Kunden empfehlen sollten, sich dessen bewusst zu sein, wenn sie mit dem Audience Manager [!DNL API]s arbeiten.

## Anforderungen {#requirements}

Beachten Sie Folgendes beim Arbeiten mit dem Code [!DNL Audience Manager] [!DNL API] :

* **Anforderungsparameter:** Alle Anforderungsparameter sind erforderlich, sofern nicht anders angegeben.
* **[!DNL JSON]Content-Typ:** Geben Sie `content-type: application/json` *und* `accept: application/json` in Ihren Code ein.

* **Anforderungen und Antworten:** Anforderungen als ordnungsgemäß formatiertes [!DNL JSON] -Objekt senden. [!DNL Audience Manager] antwortet mit [!DNL JSON] formatierten Daten. Serverantworten können angeforderte Daten, einen Statuscode oder beides enthalten.

* **Zugriff:** Ihr [!DNL Audience Manager] -Berater stellt Ihnen eine Client-ID und einen Schlüssel zur Verfügung, mit denen Sie [!DNL API] -Anfragen stellen können.

* **Dokumentation und Codebeispiele:** Text in *kursiv* stellt eine Variable dar, die Sie beim Erstellen oder Empfangen von [!DNL API] -Daten bereitstellen oder übergeben. Ersetzen Sie den Text *kursiv gedruckt* durch Ihren eigenen Code, Ihre eigenen Parameter oder andere erforderliche Informationen.

## Recommendations: Erstellen eines generischen API-Benutzers {#recommendations}

Es wird empfohlen, ein eigenes technisches Benutzerkonto für die Arbeit mit dem Audience Manager [!DNL API]s zu erstellen. Dies ist ein generisches Konto, das nicht an einen bestimmten Benutzer in der Organisation Ihres Kunden gebunden ist oder mit diesem verknüpft ist. Mit diesem Benutzerkonto vom Typ [!DNL API] können Sie zwei Dinge erreichen:

* Identifizieren Sie, welcher Dienst die [!DNL API] aufruft (z. B. Aufrufe von einer Client-App, die unsere [!DNL API] verwenden, oder von Massenänderungen).
* Gewähren Sie unterbrechungsfreien Zugriff auf die [!DNL API]s. Ein an einen bestimmten Mitarbeiter gebundenes Konto kann gelöscht werden, wenn er das Unternehmen verlässt. Dadurch wird verhindert, dass Ihre Kunden mit dem verfügbaren [!DNL API] -Code arbeiten. Ein generisches Konto, das nicht an einen bestimmten Mitarbeiter gebunden ist, hilft, dieses Problem zu vermeiden.

Nehmen wir als Beispiel oder Anwendungsfall für diesen Kontotyp an, Ihre Kunden möchten mit den [Tools für die Massenverwaltung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en) viele Segmente gleichzeitig ändern. Dazu benötigen sie [!DNL API] Zugriff. Anstatt einem bestimmten Benutzer Berechtigungen hinzuzufügen, erstellen Sie ein unspezifisches Benutzerkonto mit dem Namen [!DNL API] , das über die entsprechenden Anmeldeinformationen, den Schlüssel und das Geheimnis verfügt, um [!DNL API] -Aufrufe durchzuführen. Dies ist auch dann nützlich, wenn Clients eigene Anwendungen entwickeln, die die [!DNL Audience Manager] [!DNL API]s verwenden.
