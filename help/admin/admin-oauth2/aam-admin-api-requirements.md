---
description: Was Sie Ihre Kunden wissen lassen sollten, wenn sie mit den Audience Manager-APIs arbeiten.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API-Anforderungen und -Empfehlungen
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# API-Anforderungen und -Empfehlungen {#api-requirements-and-recommendations}

Dinge, die Sie Ihre Kunden darauf hinweisen sollten, wenn sie mit den [!DNL API] von Audience Manager arbeiten.

## Anforderungen {#requirements}

Beachten Sie beim Arbeiten mit [!DNL Audience Manager] [!DNL API]-Code Folgendes:

* **Anfrageparameter:** Alle Anfrageparameter sind erforderlich, sofern nicht anders angegeben.
* **[!DNL JSON]Content-Typ:** Geben Sie `content-type: application/json` *und* in Ihrem Code `accept: application/json`.

* **Anfragen und Antworten:** Senden von Anfragen als ordnungsgemäß formatiertes [!DNL JSON]. [!DNL Audience Manager] antwortet mit [!DNL JSON] formatierten Daten. Serverantworten können angeforderte Daten, einen Status-Code oder beides enthalten.

* **Zugriff** Ihr [!DNL Audience Manager] stellt Ihnen eine Client-ID und einen Schlüssel zur Verfügung, mit denen Sie [!DNL API] Anfragen stellen können.

* **Dokumentations- und Codebeispiele:** Text in *kursiv* stellt eine Variable dar, die Sie angeben oder übergeben, wenn Sie [!DNL API] Daten erstellen oder empfangen. Ersetzen *kursiv* Text durch eigenen Code, eigene Parameter oder andere erforderliche Informationen.

## Empfehlungen: Erstellen eines generischen API-Benutzers {#recommendations}

Es wird empfohlen, ein separates technisches Benutzerkonto für die Arbeit mit den Audience Manager [!DNL API]s zu erstellen. Dies ist ein allgemeines Konto, das nicht mit einem bestimmten Benutzer in der Organisation Ihres Kunden verknüpft ist. Mit dieser Art [!DNL API] Benutzerkontos können zwei Dinge erreicht werden:

* Identifizieren Sie, welcher Service die [!DNL API] aufruft (z. B. Aufrufe von einer Client-Anwendung, die unsere [!DNL API] verwenden, oder von Massenänderungen).
* Ununterbrochener Zugriff auf die [!DNL API]s. Ein Konto, das an einen bestimmten Mitarbeiter gebunden ist, kann gelöscht werden, wenn er das Unternehmen verlässt. Dies verhindert, dass Ihre Kunden mit dem verfügbaren [!DNL API]-Code arbeiten. Ein generisches Konto, das nicht an einen bestimmten Mitarbeiter gebunden ist, hilft, dieses Problem zu vermeiden.

Nehmen wir an, Ihre Kunden möchten als Beispiel oder Anwendungsfall für diese Art von Konto viele Segmente gleichzeitig mit den [Tools für die Massenverwaltung“ ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=de). Dazu benötigen sie [!DNL API] Zugriff. Anstatt einem bestimmten Benutzer Berechtigungen hinzuzufügen, erstellen Sie ein unspezifisches, [!DNL API] Benutzerkonto, das über die entsprechenden Anmeldeinformationen, den Schlüssel und das Geheimnis verfügt, um [!DNL API] Aufrufe durchzuführen. Dies ist auch nützlich, wenn die Kunden ihre eigenen Anwendungen entwickeln, die die [!DNL Audience Manager] [!DNL API] verwenden.
