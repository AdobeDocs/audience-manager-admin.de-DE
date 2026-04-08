---
description: Verwenden Sie die Seite „Server“ im Audience Manager Admin-Tool, um einen neuen HTTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: Erstellen oder Bearbeiten eines HTTP-Servers
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
TQID: https://experienceleague.adobe.com/vcybBl222PvpcEeMFtPZyqbP-YWHCNKF9luqmTZ1C7Y
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: a8b0238e-1d43-4679-a3b4-5ba1bad83baa
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 2%

---

# Erstellen oder Bearbeiten eines HTTP-Servers {#create-or-edit-an-http-server}

Verwenden Sie die Seite &quot;[!UICONTROL Servers]&quot; im Audience Manager Admin-Tool, um einen neuen HTTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.

>[!NOTE]
>
>Sie müssen über die Rolle [!UICONTROL DEXADMIN] verfügen, um neue Server zu erstellen oder vorhandene Server zu bearbeiten.

1. Um einen neuen Server zu erstellen, gehen Sie zu **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Um einen vorhandenen Server zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Label]** auf den gewünschten Server.
1. Geben Sie den gewünschten Titel für diesen Server an.
1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Protocol]** das gewünschte Protokoll aus: [!DNL HTTP].
1. Füllen Sie die Felder aus:

   * **[!UICONTROL Domain]:** Geben Sie die gewünschte Domain (den Host) für diesen Server an.
   * **[!UICONTROL Port]:** Geben Sie den gewünschten Port für diesen Server an. Der Standard-Port wird für jeden Verschlüsselungstyp angezeigt. Sie können bei Bedarf den Standard-Port ändern
   * **[!UICONTROL Maximum Users Per Request]:** Geben Sie die maximale Anzahl von Benutzern pro Anfrage an, die für diesen Server zulässig ist.
   * **[!UICONTROL URL Prefix]:** Geben Sie das [!DNL URL] Präfix an, das für diesen Server verwendet werden soll.
   * **[!UICONTROL Authentication URL]:** Geben Sie die [!UICONTROL Authentication URL] für diesen `HTTP` an.
   * **[!UICONTROL Authentication]:** Geben Sie die gewünschte Authentifizierungsmethode an: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** oder **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** Der Name der vom Kunden bereitgestellten [!DNL HTTP]-Kopfzeile, die den [!DNL HTTP] Signaturschlüssel enthält. Der Standardwert ist [!UICONTROL X-Signature], wie im folgenden Beispiel gezeigt:

     ```
     * Connected to partner.website.com (127.0.0.1) port 80 (#0)
     > POST /webpage HTTP/1.1
     > Host: partner.host.com
     > Accept: */*
     > Content-Type: application/json
     > Content-Length: 20
     > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
     POST message content
     ```

   * **[!UICONTROL HTTP Signature Key]:** Der Schlüssel, mit dem die vom Kunden bereitgestellte [!DNL HTTP] signiert wird.
   * **[!UICONTROL Show Signature Key]:** Schalten Sie ein, ob die Signatur im Browser angezeigt werden soll.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Geben Sie die Methode an, die zum Verschlüsseln der Signatur verwendet werden soll. Verwenden Sie [!UICONTROL SHA1], sofern der Kunde nichts anderes vorzieht.

   >[!NOTE]
   >
   >Wenn Sie die [OAuth 2.0-Authentifizierung für Echtzeit-Datenübertragungen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=de) für einen Partner aktivieren möchten, füllen Sie die Felder wie in der folgenden Tabelle aus. Die Felder *kursiv* müssen genau wie in der Tabelle ausgefüllt werden.

   | Name | Wert |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Genehmigung*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Klicken Sie auf **[!UICONTROL Create]**, wenn Sie einen neuen Server erstellen, oder klicken Sie auf **[!UICONTROL Update]**, wenn Sie einen vorhandenen Server bearbeiten.
