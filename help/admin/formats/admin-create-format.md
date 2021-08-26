---
description: Verwenden Sie die Seite "Formate"im Audience Manager-Admin-Tool, um ein neues Format zu erstellen oder ein vorhandenes Format zu bearbeiten.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Erstellen oder Bearbeiten von Formaten
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 4%

---

# Erstellen oder Bearbeiten von Formaten {#create-or-edit-a-format}

Verwenden Sie die Seite [!UICONTROL Formats] im Audience Manager Admin-Tool, um ein neues Format zu erstellen oder ein vorhandenes Format zu bearbeiten.

<!-- t_create_format.xml -->

>[!TIP]
>
>Wenn Sie ein Format für Ihre ausgehenden Daten auswählen, sollten Sie möglichst ein vorhandenes Format wiederverwenden. Die Verwendung eines bereits bewährten Formats stellt sicher, dass Ihre ausgehenden Daten erfolgreich generiert werden. Um genau zu sehen, wie ein vorhandenes Format formatiert ist, klicken Sie in der Menüleiste auf die Option [!UICONTROL Formats] und suchen Sie nach Ihrem Format entweder nach Namen oder nach ID-Nummer. Fehlerhafte Formate oder Makros, die in Formaten verwendet werden, liefern eine falsch formatierte Ausgabe oder verhindern die vollständige Ausgabe von Informationen.

1. Um ein neues Format zu erstellen, klicken Sie auf **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Um ein vorhandenes Format zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Name]** auf das gewünschte Format.

   ![](assets/create_format.png)

1. Füllen Sie die Felder aus:
   * **Name:**  (Erforderlich) Geben Sie einen beschreibenden Namen für das Format ein.
   * **Typ:** (Erforderlich) Wählen Sie das gewünschte Format aus:
      * **[!UICONTROL File]**: Sendet Daten über  [!DNL FTP] Dateien.
      * **[!UICONTROL HTTP]**: Umfasst Daten in einem  [!DNL JSON] Wrapper.

1. (Bedingt) Wenn Sie **[!UICONTROL File]** auswählen, füllen Sie die Felder aus:

   >[!NOTE]
   >
   >Eine Liste der verfügbaren Makros finden Sie unter [Dateiformatmakros](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) und [HTTP-Formatmakros](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Geben Sie den Dateinamen für die Datenübertragungsdatei an.
   * **Kopfzeile:**  Geben Sie den Text an, der in der ersten Zeile der Datenübertragungsdatei angezeigt wird.
   * **[!UICONTROL Data Row]:** Geben Sie den Text an, der in jeder ausgehenden Zeile der Datei angezeigt wird.
   * **[!UICONTROL Maximum File Size (In MB)]:** Geben Sie die maximale Dateigröße für Datenübertragungsdateien an. Komprimierte Dateien müssen kleiner als 100 MB sein. Die unkomprimierte Dateigröße ist nicht beschränkt.
   * **[!UICONTROL Compression]:**  Wählen Sie den gewünschten Komprimierungstyp aus: gz oder zip für Ihre Datendateien. Für die Bereitstellung an [!UICONTROL AWS S3] müssen Sie .gz- oder unkomprimierte Dateien verwenden.
   * **[!UICONTROL .info Receipt]:** Gibt an, dass eine Übertragungssteuerungsdatei ([!DNL .info]) generiert wird. Die Datei [!DNL .info] enthält Metadateninformationen zu Dateiübertragungen, damit Partner überprüfen können, ob der Audience Manager die Dateiübertragungen ordnungsgemäß verarbeitet hat. Weitere Informationen finden Sie unter [Dateiübertragungen für Protokolldateiübertragungen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]:** Gibt an, dass ein  [!DNL MD5] Prüfsummenbeleg generiert wird. Der [!DNL MD5]-Prüfsummenbeleg, damit Partner überprüfen können, ob der Audience Manager den vollständigen Transfer ordnungsgemäß durchgeführt hat.

1. (Bedingt) Wenn Sie **[!UICONTROL HTTP]** auswählen, füllen Sie die Felder aus:

   * **[!UICONTROL Method]:** Wählen Sie die  [!DNL API] Methode aus, die Sie für Ihren Übertragungsprozess verwenden möchten:
      * **[!UICONTROL POST]:** Wenn Sie auswählen, wählen Sie  [!DNL POST]den Inhaltstyp ([!DNL XML] oder  [!DNL JSON]) und geben Sie dann den Anfrageinhalt an.
      * **[!UICONTROL GET]:** Wenn Sie auswählen, geben Sie  [!DNL GET]die Abfrageparameter an.

1. Klicken Sie auf **[!UICONTROL Create]**, wenn Sie ein neues Format erstellen, oder auf **[!UICONTROL Save Updates]** , wenn Sie ein vorhandenes Format bearbeiten.

## Löschen eines Formats {#delete-format}

1. Klicken **[!UICONTROL Formats]**.
2. Klicken Sie in der Spalte **[!UICONTROL Actions]** des gewünschten Formats auf ![](assets/icon_delete.png) .
3. Klicken Sie auf **[!UICONTROL OK]**, um den Löschvorgang zu bestätigen.
