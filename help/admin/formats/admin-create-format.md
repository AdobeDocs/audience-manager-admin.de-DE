---
description: Verwenden Sie die Seite „Formate“ im Audience Manager Admin-Tool, um ein neues Format zu erstellen oder ein vorhandenes Format zu bearbeiten.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Erstellen oder Bearbeiten eines Formats
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
TQID: https://experienceleague.adobe.com/VMEOfWNeQ5CSWvWqZYdjNO4qyvFD5Iw1onpAdVRKgQQ
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: a8b0238e-1d43-4679-a3b4-5ba1bad83baa
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 439
ht-degree: 1%

---

# Erstellen oder Bearbeiten eines Formats {#create-or-edit-a-format}

Verwenden Sie die Seite &quot;[!UICONTROL Formats]&quot; im Audience Manager Admin-Tool, um ein neues Format zu erstellen oder ein vorhandenes Format zu bearbeiten.

<!-- t_create_format.xml -->

>[!TIP]
>
>Bei der Auswahl eines Formats für Ihre ausgehenden Daten ist es am besten, wenn möglich, ein vorhandenes Format wiederzuverwenden. Die Verwendung eines bereits bewährten Formats stellt sicher, dass Ihre ausgehenden Daten erfolgreich generiert werden. Um genau zu sehen, wie ein vorhandenes Format formatiert ist, klicken Sie auf die Option [!UICONTROL Formats] in der Menüleiste und suchen Sie entweder nach Name oder nach ID-Nummer nach Ihrem Format. Falsch formatierte Formate oder Makros, die in -Formaten verwendet werden, liefern eine falsch formatierte Ausgabe oder verhindern die Ausgabe von Informationen vollständig.

1. Um ein neues Format zu erstellen, klicken Sie auf **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Um ein vorhandenes Format zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Name]** auf das gewünschte Format.

   ![](assets/create_format.png)

1. Füllen Sie die Felder aus:
   * **Name:** (erforderlich) Geben Sie einen beschreibenden Namen für das Format an.
   * **Typ:** (Erforderlich) Wählen Sie das gewünschte Format aus:
      * **[!UICONTROL File]**: Sendet Daten über [!DNL FTP].
      * **[!UICONTROL HTTP]**: Schließt Daten in einen [!DNL JSON] ein.

1. (Bedingt) Wenn Sie **[!UICONTROL File]** ausgewählt haben, füllen Sie die Felder aus:

   >[!NOTE]
   >
   >Eine Liste der verfügbaren Makros finden Sie unter [Dateiformatmakros](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) und [HTTP-Formatmakros](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Geben Sie den Dateinamen für die Datenübertragungsdatei an.
   * **Kopfzeile:** Geben Sie den Text an, der in der ersten Zeile der Datenübertragungsdatei angezeigt wird.
   * **[!UICONTROL Data Row]:** Geben Sie den Text an, der in jeder ausgehenden Zeile der Datei angezeigt wird.
   * **[!UICONTROL Maximum File Size (In MB)]:** Geben Sie die maximale Dateigröße für Datenübertragungsdateien an. Komprimierte Dateien müssen kleiner als 100 MB sein. Die unkomprimierte Dateigröße ist unbegrenzt.
   * **[!UICONTROL Compression]:** Wählen Sie den gewünschten Komprimierungstyp: gz oder zip für Ihre Datendateien. Für den Versand an [!UICONTROL AWS S3] müssen Sie .gz- oder unkomprimierte Dateien verwenden.
   * **[!UICONTROL .info Receipt]:** Gibt an, dass eine Datei für die Übertragungssteuerung ([!DNL .info]) generiert wird. Die [!DNL .info]-Datei enthält Metadateninformationen zu Dateiübertragungen, damit Partner überprüfen können, ob Audience Manager Dateiübertragungen korrekt verarbeitet hat. Weitere Informationen finden Sie unter [Transfersteuerungsdateien für Protokolldateiübertragungen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=de).
   * **[!UICONTROL MD5 Checksum Receipt]:** Gibt an, dass eine [!DNL MD5] generiert wird. Die [!DNL MD5] Prüfsummenquittung, mit der Partner überprüfen können, ob Audience Manager die vollständige Übertragung ordnungsgemäß verarbeitet hat.

1. (Bedingt) Wenn Sie **[!UICONTROL HTTP]** ausgewählt haben, füllen Sie die Felder aus:

   * **[!UICONTROL Method]:** Wählen Sie die [!DNL API], die Sie für Ihren Übertragungsprozess verwenden möchten:
      * **[!UICONTROL POST]:** Wenn Sie [!DNL POST] auswählen, wählen Sie den Inhaltstyp aus ([!DNL XML] oder [!DNL JSON]) und geben Sie dann den Anfragetext an.
      * **[!UICONTROL GET]:** Wenn Sie [!DNL GET] auswählen, geben Sie die Abfrageparameter an.

1. Klicken Sie auf **[!UICONTROL Create]** , wenn Sie ein neues Format erstellen, oder klicken Sie auf **[!UICONTROL Save Updates]** , wenn Sie ein vorhandenes Format bearbeiten.

## Löschen eines Formats {#delete-format}

1. Klicken Sie auf **[!UICONTROL Formats]**.
2. Klicken Sie in der **[!UICONTROL Actions]** Spalte des gewünschten Formats auf ![](assets/icon_delete.png) .
3. Klicken Sie auf **[!UICONTROL OK]** , um den Löschvorgang zu bestätigen.
