---
description: Verwenden Sie die Seite Server im Audience Manager Admin-Tool, um einen neuen S3-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new S3 server or to edit an existing server.
seo-title: Create or Edit an S3 Server
title: Erstellen oder Bearbeiten eines S3-Servers
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
exl-id: 89310de0-e24e-4d4b-8171-56faf0b441f6
TQID: https://experienceleague.adobe.com/rtXpkVovwbjCwLk3caZ7Ii-LLcr2n3eL73OADaLoul0
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 1%

---

# Erstellen oder Bearbeiten eines S3-Servers {#create-or-edit-an-s-server}

Verwenden Sie die Seite [!UICONTROL Servers] im Audience Manager Admin-Tool, um einen neuen [!DNL S3]-Server zu erstellen oder einen vorhandenen Server zu bearbeiten.

>[!NOTE]
>
>Sie müssen über die Rolle [!UICONTROL DEXADMIN] verfügen, um neue Server zu erstellen oder vorhandene Server zu bearbeiten.

1. Um einen neuen Server zu erstellen, klicken Sie auf **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Um einen vorhandenen Server zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Label]** auf den gewünschten Server.
1. Geben Sie den gewünschten Titel für diesen Server an.
1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Protocol]** das gewünschte Protokoll aus: **[!UICONTROL S3]**.

   >[!NOTE]
   >
   >Es wird empfohlen, [!DNL Amazon S3] als Methode zum Abrufen von Dateien von und zum Bereitstellen von Dateien für Partner zu verwenden. [!DNL Amazon S3] bietet eine einfache Web-Services-Schnittstelle, mit der Daten jeder beliebigen Menge jederzeit und von jedem beliebigen Ort im Web gespeichert und abgerufen werden können. Weitere Informationen finden Sie unter [Über Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) im *Audience Manager-Benutzerhandbuch*.

1. Füllen Sie die Felder aus:

   * **[!UICONTROL Account]:** Geben Sie das gewünschte [!DNL S3] an.
   * **[!UICONTROL Bucket]:** Geben Sie den gewünschten [!DNL S3] an.
   * **[!UICONTROL Directory]:** Geben Sie das gewünschte [!DNL S3] an.
   * **[!UICONTROL Access Key]:** Geben Sie den gewünschten [!DNL S3] Zugriffsschlüssel an.
   * **[!UICONTROL Secret Key]:** Geben Sie den gewünschten geheimen [!DNL S3] an.

1. Klicken Sie auf **[!UICONTROL Create]**, wenn Sie einen neuen Server erstellen, oder klicken Sie auf **[!UICONTROL Update]**, wenn Sie einen vorhandenen Server bearbeiten.
