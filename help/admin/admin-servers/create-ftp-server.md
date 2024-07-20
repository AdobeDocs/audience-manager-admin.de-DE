---
description: Verwenden Sie die Seite "Server"im Audience Manager Admin-Tool, um einen neuen FTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Erstellen oder Bearbeiten eines FTP-Servers
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# Erstellen oder Bearbeiten eines FTP-Servers {#create-or-edit-an-ftp-server}

Verwenden Sie die Seite &quot;[!UICONTROL Servers]&quot;im Audience Manager Admin Tool, um einen neuen FTP-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.

>[!NOTE]
>
>Sie müssen über die Rolle &quot;[!UICONTROL DEXADMIN]&quot;verfügen, um neue Server zu erstellen oder vorhandene Server zu bearbeiten.

1. Um einen neuen Server zu erstellen, klicken Sie auf **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Um einen vorhandenen Server zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Label]** auf den gewünschten Server.
1. Geben Sie die gewünschte Bezeichnung für diesen Server an.
1. Wählen Sie aus der Dropdownliste **[!UICONTROL Protocol]** das gewünschte Protokoll aus: **FTP**.

   >[!NOTE]
   >
   >Als Best Practice wird empfohlen, [!DNL Amazon S3] als Methode zum Abrufen von Dateien von und zum Bereitstellen von Dateien an Partner zu verwenden. [!DNL Amazon S3] bietet eine einfache Web-Services-Oberfläche, die verwendet werden kann, um eine beliebige Menge von Daten jederzeit von überall im Internet zu speichern und abzurufen. Weitere Informationen finden Sie unter [Über Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) im *Benutzerhandbuch für Audience Manager*.

1. Füllen Sie die Felder aus:

   * **[!UICONTROL Type]:** Wählen Sie den gewünschten Verschlüsselungstyp aus: **[!UICONTROL SFTP]** oder **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Geben Sie die gewünschte Domäne (den Host) für diesen Server an.
   * **[!UICONTROL Port]:** Geben Sie den gewünschten Anschluss für diesen Server an. Für jeden Verschlüsselungstyp wird der Standardanschluss angezeigt. Sie können bei Bedarf den Standardanschluss ändern.
   * **[!UICONTROL Remote Path]:** Geben Sie den gewünschten Remote-Pfad für diesen Server an. Wenn Sie dieses Feld leer lassen, platziert Audience Manager die Dateien im Standardverzeichnis.
   * **[!UICONTROL .tmp File Rename on Completion]:** Aktivieren Sie diese Option, um die `.tmp`-Datei nach Abschluss umzubenennen.
   * **[!UICONTROL Filename Suffix]:** Geben Sie den Text an, der an Dateien angehängt werden soll.
   * **[!UICONTROL Moved to When Finished]:** Geben Sie den Pfad zu dem Speicherort an, an den die Übertragungsdatei nach Abschluss verschoben werden soll.
   * **[!UICONTROL Authentication]:** Geben Sie die gewünschte Server-Authentifizierungsmethode an: **[!UICONTROL Username/Password]** oder **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Denken Sie daran, unsere Ausgangs- [!DNL FTP] [!DNL IP] zu Ihrer Liste der zulässigen IPs hinzuzufügen: **52.44.29.204**.

1. Für die **[!UICONTROL SSH Key]**-Authentifizierung:
   >[!NOTE]
   >
   >Stellen Sie beim Konfigurieren der SSH-Schlüsselauthentifizierung sicher, dass Sie immer die öffentlichen und privaten Schlüssel nur im OpenSSH-Format generieren.
   1. Generieren Sie das Paar aus öffentlichem/privatem Schlüssel von einem beliebigen [!DNL Linux] - oder [!DNL Mac] -Computer.
   1. Geben Sie den öffentlichen Schlüssel **1} an den Client weiter, um ihn auf seinem [!DNL SFTP] -Server zu aktualisieren.** Sie müssen den gesamten Text aus dem öffentlichen Schlüssel auf ihrem Server einschließen, einschließlich `-----BEGIN RSA PRIVATE KEY-----` und `-----END RSA PRIVATE KEY-----` . Im Gegenzug müssen sie den Benutzernamen angeben, unter dem sie den Schlüssel installieren.
   1. Aktualisieren Sie das Feld &quot;Benutzername&quot;mit dem vom Client bereitgestellten Feld und das Schlüsselfeld mit dem Schlüssel **private Schlüssel**.
1. Klicken Sie auf &quot;**[!UICONTROL Create]**&quot;, wenn Sie einen neuen Server erstellen, oder auf &quot;**[!UICONTROL Update]**&quot;, wenn Sie einen vorhandenen Server bearbeiten.
