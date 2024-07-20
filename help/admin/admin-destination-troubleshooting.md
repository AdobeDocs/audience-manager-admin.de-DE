---
description: Informationen, die Sie bei der Einrichtung von Zielen in Audience Manager unterstützen und allgemeine Probleme vermeiden.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Fehlerbehebung bei der Zieleinrichtung
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 3%

---

# Fehlerbehebung bei der Zieleinrichtung {#destination-setup-troubleshooting}

Informationen, die Sie bei der Einrichtung von Zielen in Audience Manager unterstützen und allgemeine Probleme vermeiden.

## Ich habe ein Ziel eingerichtet, aber ich sehe keine Dateien. Wo sind sie? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

Häufige Probleme bei der Zielkonfiguration sind unter anderem folgende:

### Nicht konfiguriertes Ziel

* **Falscher [!UICONTROL UserID] Schlüssel:** Der [!UICONTROL UserID] Schlüssel ist der [!UICONTROL MasterDPID] dieses Ziels und bildet die Grundlage für die ausgehenden ID-Werte. Selbst wenn ein [!UICONTROL UserID] -Schlüssel über die Dropdownliste auswählbar ist, bedeutet dies nicht unbedingt, dass diesem Wert IDs/Eigenschaften/Segmente zugeordnet sind. Wenn der [!UICONTROL Outbound]-Prozess (der nach der Erstellung von Zielen ausgeführt wird) keine Benutzer findet, die diesem [!UICONTROL UserID] -Schlüssel zugeordnet sind, werden keine Daten ausgegeben.
* **Nein In &quot;Ausgewählte Dateidatenquellen&quot;:** Bei der Auswahl eines anderen Zieltyps als [!UICONTROL S2S] wird unten auf dem Bildschirm ein Abschnitt mit der Bezeichnung [!UICONTROL Configure Data Sources] angezeigt. Wenn dieser Abschnitt zum ersten Mal angezeigt wird, werden keine Werte ausgewählt. Wenn Sie vergessen haben, auf das Kontrollkästchen [!UICONTROL All First Party] zu klicken oder Datenquellen aus dem Fenster [!UICONTROL Available Data Sources] einzeln auszuwählen, werden keine Daten ausgegeben.

### Falsch konfiguriertes Format

Wenn Sie ein Format für Ihre ausgehenden Daten auswählen, sollten Sie möglichst ein vorhandenes Format wiederverwenden. Die Verwendung eines bereits bewährten Formats stellt sicher, dass Ihre ausgehenden Daten erfolgreich generiert werden. Um genau zu sehen, wie ein vorhandenes Format formatiert ist, klicken Sie in der Menüleiste auf die Option [!UICONTROL Formats] und suchen Sie nach Ihrem Format entweder nach Namen oder nach ID-Nummer. Fehlerhafte Formate oder Makros, die in Formaten verwendet werden, liefern eine falsch formatierte Ausgabe oder verhindern die vollständige Ausgabe von Informationen.

Weitere Informationen zum Einrichten von Formaten und Verwenden von Makros finden Sie unter [Dateiformatmakros](formats/file-formats.md#) und [HTTP-Formatmakros](formats/web-formats.md).

### Nicht konfigurierter Server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Geben Sie keine Präfixe für Hostnamen ein. Wenn Sie ein Konto [!DNL ftp://hello.com] erhalten, geben Sie einfach [!DNL hello.com] in dieses Feld ein.
   * **[!UICONTROL Port/Type Combination]**
      * Bei einer [!DNL FTP] -Übertragung ist der bevorzugte Transfertyp [!DNL SFTP].
      * Bei Auswahl des Typs [!DNL SFTP] beträgt der Anschluss fast immer 22.
      * Bei Auswahl des Typs [!DNL FTPs/TLS] beträgt der Anschluss fast immer 21.
      * Der Typ [!DNL FTPs/TLS] ist nicht derselbe wie eine normale [!DNL FTP] Übertragung. Wir unterstützen keine regulären (ungesicherten) [!DNL FTP] Transfers.
   * **[!UICONTROL Remote Path]**
      * Bei der Auswahl eines Remote-Unterpfads sollte dieser ohne Schrägstrich eingegeben werden.
      * Wenn Ihre übertragene Datei im Unterordner [!DNL (root)/inbound] platziert werden soll, fügen Sie einfach [!DNL inbound] für den Remote-Pfad hinzu, nicht [!DNL /inbound].
      * Wenn Sie Ihre Dateien in mehreren Verzeichnissen unter dem Pfad senden, geben Sie Schrägstriche zwischen den einzelnen Verzeichnissen ein. Wenn Sie den Speicherort von [!DNL /inbound/subdirectory1/subdirectory2] erhalten, sollten Sie in dieses Feld [!DNL inbound/subdirectory1/subdirectory2] eingeben.
      * Wenn Ihre Datei im Ordner abgelegt werden soll, der automatisch vom externen Server an den Server weitergeleitet wird, können Sie diesen Bereich leer lassen. Geben Sie keinen Punkt ein ( . ), Schrägstrich ( / ) oder alles andere.

* **[!DNL S3]**
   * [!DNL S3] ist das bevorzugte Transferprotokoll (über [!DNL FTP] oder [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * Der Bucket-Name sollte ohne Schrägstriche, Präfixe, Suffixe usw. aufgeführt werden. Wenn Sie die Adresse [!DNL s3://your-bucket] erhalten, sollten Sie einfach [!DNL your-bucket] in dieses Feld einfügen.
      * **[!UICONTROL Directory]**
         * Lassen Sie dieses Feld leer, es sei denn, Sie erhalten speziell ein Unterverzeichnis, in das die Daten eingefügt werden sollen. Wenn Sie die Adresse [!DNL s3://your-bucket/your-subdirectory] erhalten, geben Sie [!DNL your-bucket] in das Feld [!UICONTROL Bucket] ein und [!DNL your-subdirectory] sollte in das Feld [!UICONTROL Directory] eingefügt werden. Fügen Sie keine vorangegangenen Schrägstriche hinzu.
         * Wenn Sie mehrere Verzeichnisse entlang des Pfads bewegen müssen, sollten Sie nur Schrägstriche als Trennzeichen verwenden. Für eine Position von [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] würde also [!DNL your-bucket] im Feld [!UICONTROL Bucket] und [!DNL your-subdirectory1/your-subdirectory2] im Feld [!UICONTROL Directory] eingegeben.
      * **[!UICONTROL Access / Secret Keys]**
         * Wenn [!DNL TechOps] einen Behälter erstellt und einem Berater Zugriffs-/geheime Schlüssel zur Verfügung stellt, sind diese Anmeldeinformationen normalerweise `READ-ONLY` Anmeldeinformationen, die an den Client übergeben werden sollen. Diese Anmeldeinformationen sollten nicht in die Felder [!UICONTROL Access / Secret Key] eingegeben werden, da dies dazu führt, dass die Übertragung fehlschlägt (da diese Anmeldeinformationen schreibgeschützt, nicht schreibbar sind). Wenn [!DNL TechOps] einen Bucket erstellt und Anmeldeinformationen bereitstellt, sollte der Berater auch ein Adobe-Schlüsselpaar anfordern - NICHT AN DEN CLIENT ZU ÜBERGEBEN -, das das Schreiben von Dateien in diesen Bucket ermöglicht. Dieser Schlüssel sollte in diese Felder eingefügt werden.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Geben Sie Präfixinformationen für [!DNL HTTP] -Einträge ein. Wenn Sie ein Konto [!DNL https://superduper.com] erhalten, geben Sie [!DNL https://superduper.com] in dieses Feld ein.
      * **[!UICONTROL URL Prefix]**
         * Lassen Sie beim Hinzufügen eines &quot;[!DNL URL]&quot;-Präfixes den vorangehenden Schrägstrich deaktiviert. Bei einer Adresse von [!DNL https://hello.com/r/x/y/z] sollte [!DNL https://hello.com] in das Feld [!UICONTROL Domain] eingegeben und [!DNL r/x/y/z] in das Feld [!UICONTROL URL Prefix] eingegeben werden.
         * Wenn kein [!UICONTROL URL Prefix] erforderlich ist, lassen Sie diesen Wert leer.
      * **[!UICONTROL Authentication - SSH Key]**
         * Geben Sie den vollständigen Schlüssel `SSH PRIVATE` in dieses Feld ein, einschließlich Kopf- und Fußzeilen sowie Zeilenumbrüchen, um eine genaue Verschlüsselung/Schlüsselspeicherung sicherzustellen.

### Nicht genügend Zeit für ausgehende Generationen

Der ausgehende Prozess wird zweimal täglich ausgeführt, und es werden mehrere Prozesse ausgeführt (Outbound, Publishing, Push an externe Standorte usw.) muss ausgeführt werden, bevor eine Datei an ihr endgültiges Ziel gesendet wird. Eine gute Faustregel besteht darin, dass ein Ziel mindestens 24 Stunden vollständig konfiguriert werden sollte, bevor Sie erwarten können, dass Daten an einen externen Speicherort gesendet werden.

### Dateiaufspaltungsgrößen zu groß

Wenn Sie Dateien an Ziele aussenden, können Sie größere ausgehende Dateien in Dateiblöcke aufteilen. Stellen Sie sicher, dass die einzelnen Dateiblöcke nicht größer als 10 GB sind. Siehe auch [Name der ausgehenden Datendatei: Syntax und Beispiele](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Einrichten Ihrer Ziele zum Exportieren von Experience Cloud-IDs, Kunden-IDs oder Audience Manager-IDs in ausgehende Datendateien {#set-up-destinations-export}

Auf dieser Seite erfahren Sie, wie Sie Ziele einrichten, um Daten zu exportieren, die vom gewünschten ID-Typ in [!UICONTROL Outbound Data Files] stammen.

<!-- set-up-destinations-mcid-aamid.xml -->

Ziele ermöglichen es unseren Kunden, ihre Daten über eine beliebige Anzahl digitaler Kanäle zu aktivieren. Sie können beispielsweise Zielgruppendaten in andere [!DNL Adobe Experience Cloud] -Lösungen ([!DNL Target], [!DNL Campaign] usw. exportieren. Oder sie können Daten an [!UICONTROL DSP]s, [!UICONTROL SSP]s oder eine beliebige Plattform senden, die mit Audience Manager integriert ist. Eine Liste der Partner, mit denen wir arbeiten, finden Sie auf unserer [Integrations Wiki-Seite](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Eine ausführliche Anleitung zum Erstellen von Zielen in der Admin-Benutzeroberfläche finden Sie im Artikel [Erstellen oder Bearbeiten von Unternehmenszielen](companies/admin-manage-company-destinations.md#create-edit-company-destinations) .

Ihre Kunden möchten je nach Ziel unterschiedliche ID-Typen exportieren. Das folgende Konfigurationdiagramm zeigt die Optionen, die Sie auswählen sollten, um Profilinformationen zu unterschiedlichen ID-Typen zu exportieren. Es wird empfohlen, auch auf den [Index of IDs in Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en) zu verweisen. Es sind drei wichtige Einstellungen zu beachten: die [!UICONTROL User ID Key], die [!UICONTROL Data Source Type] und die [!UICONTROL Format]. Wir führen sie alle im Folgenden detailliert auf.

* [!UICONTROL User ID Key]. Wechseln Sie in der [!UICONTROL Admin UI] zu **[!UICONTROL Companies]**. Suchen Sie nach dem Unternehmen Ihres Kunden und klicken Sie darauf. Suchen Sie nach der Registerkarte **[!UICONTROL Destinations]** und drücken Sie **[!UICONTROL Add Destination]**. Wählen Sie im Workflow **[!UICONTROL Add Destination]** den Wert [!UICONTROL User ID Key] aus. Die [!UICONTROL User ID Key] filtert die eingehenden IDs aus der Zieldatenquelle und lässt nur die Weiterleitung der IDs zu.

  ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Wählen Sie diese Option beim Erstellen eines Ziels in der Audience Manager-Benutzeroberfläche aus. Wählen Sie zunächst [!UICONTROL Inbound] und dann den gewünschten ID-Typ aus. Die Optionen sind:

  ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Diese Option bestimmt das Dateiformat, das exportiert werden soll. Wählen Sie im Workflow **[!UICONTROL Add Destination]** unter **[!UICONTROL Batch Data]** das Format aus.

Um ein Format zu überprüfen, gehen Sie zu **[!UICONTROL Admin UI > Formats]** und suchen Sie nach dem Element [!UICONTROL Data Row] . Dieses Element enthält ein Makro des Dateiformats, im folgenden Beispiel &lt;MCID>.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Konfigurationsnummer </th> 
   <th colname="col1" class="entry"> <p>Benutzerschlüssel </p> </th> 
   <th colname="col2" class="entry"> <p>Source-Datentyp </p> </th> 
   <th colname="col3" class="entry"> <p>Format </p> </th> 
   <th colname="col4" class="entry"> <p>Exportierter ID-Typ </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Kunden-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Kunden-ID (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Kunden-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Kunden-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (Jede Datenquelle, auf die das Unternehmen Zugriff hat) </p> </td> 
   <td colname="col2"> <p>Audience Manager-ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager-UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## Nutzungsszenarios

Nehmen wir an, Sie verwenden Audience Manager und [!DNL Campaign]. Damit die Kundendaten in [!DNL Campaign] verarbeitet werden können, müssen Sie [!UICONTROL Experience Cloud IDs] exportieren. In diesem Fall sollten Sie die Konfigurationsnummer 3 verwenden.
