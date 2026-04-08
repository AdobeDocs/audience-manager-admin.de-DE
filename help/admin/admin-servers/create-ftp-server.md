---
description: Verwenden Sie die Seite Server im Audience Manager Admin-Tool, um einen neuen FTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Erstellen oder Bearbeiten eines FTP-Servers
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
TQID: https://experienceleague.adobe.com/vXm5k1APT6BVn0Ub7ntfDCnAdSfOWTLRo6ci-yK5cWk
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 397
ht-degree: 1%

---

# Erstellen oder Bearbeiten eines FTP-Servers {#create-or-edit-an-ftp-server}

Verwenden Sie die Seite &quot;[!UICONTROL Servers]&quot; im Audience Manager Admin-Tool, um einen neuen FTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.

>[!NOTE]
>
>Sie müssen über die Rolle [!UICONTROL DEXADMIN] verfügen, um neue Server zu erstellen oder vorhandene Server zu bearbeiten.

1. Um einen neuen Server zu erstellen, klicken Sie auf **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Um einen vorhandenen Server zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Label]** auf den gewünschten Server.
1. Geben Sie den gewünschten Titel für diesen Server an.
1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Protocol]** das gewünschte Protokoll aus: **FTP**.

   >[!NOTE]
   >
   >Als Best Practice empfehlen wir die Verwendung von [!DNL Amazon S3] als Methode zum Abrufen von Dateien von und zum Bereitstellen von Dateien für Partner. [!DNL Amazon S3] bietet eine einfache Web-Services-Schnittstelle, mit der Daten jeder beliebigen Menge jederzeit und von jedem beliebigen Ort im Web gespeichert und abgerufen werden können. Weitere Informationen finden Sie unter [Über Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) im *Audience Manager-Benutzerhandbuch*.

1. Füllen Sie die Felder aus:

   * **[!UICONTROL Type]:** Wählen Sie den gewünschten Verschlüsselungstyp aus: **[!UICONTROL SFTP]** oder **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Geben Sie die gewünschte Domain (den Host) für diesen Server an.
   * **[!UICONTROL Port]:** Geben Sie den gewünschten Port für diesen Server an. Der Standard-Port wird für jeden Verschlüsselungstyp angezeigt. Sie können bei Bedarf den Standard-Port ändern.
   * **[!UICONTROL Remote Path]:** Geben Sie den gewünschten Remote-Pfad für diesen Server an. Wenn Sie dieses Feld leer lassen, platziert Audience Manager die Dateien im Standardverzeichnis.
   * **[!UICONTROL .tmp File Rename on Completion]:** Aktivieren Sie diese Option, um die `.tmp` nach Abschluss umzubenennen.
   * **[!UICONTROL Filename Suffix]:** Geben Sie den Text an, der zur Übertragung von Dateien angehängt werden soll.
   * **[!UICONTROL Moved to When Finished]:** Geben Sie den Pfad zu dem Speicherort an, an den die Übertragungsdatei nach Abschluss verschoben werden soll.
   * **[!UICONTROL Authentication]:** Geben Sie die gewünschte Serverauthentifizierungsmethode an: **[!UICONTROL Username/Password]** oder **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Denken Sie daran, unsere Egress-[!DNL FTP]-[!DNL IP] zu Ihrer Liste der zulässigen IPs hinzuzufügen: **54.204.116.43**.

1. Für **[!UICONTROL SSH Key]** Authentifizierung:

   >[!NOTE]
   >
   >Stellen Sie bei der Konfiguration der SSH-Schlüsselauthentifizierung sicher, dass Sie die öffentlichen und privaten Schlüssel nur im OpenSSH-Format generieren.

   1. Generieren Sie das Schlüsselpaar aus öffentlichem/privatem Schlüssel aus einem beliebigen [!DNL Linux] oder [!DNL Mac].
   1. Geben Sie **Client den „öffentlichen Schlüssel**, damit er auf seinem [!DNL SFTP] aktualisiert wird. Sie müssen den gesamten Text aus dem öffentlichen Schlüssel auf ihrem Server einschließen, einschließlich `-----BEGIN RSA PRIVATE KEY-----` und `-----END RSA PRIVATE KEY-----` . Im Gegenzug müssen sie den Benutzernamen angeben, unter dem sie den Schlüssel installieren.
   1. Aktualisieren Sie das Feld Benutzername mit dem vom Client bereitgestellten Feld und das Feld Schlüssel mit dem **privaten Schlüssel**.

1. Klicken Sie auf **[!UICONTROL Create]**, wenn Sie einen neuen Server erstellen, oder klicken Sie auf **[!UICONTROL Update]**, wenn Sie einen vorhandenen Server bearbeiten.
