---
description: Erstellen, Bearbeiten und Löschen von Audience Manager-Zielen.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Verwalten von Unternehmenszielen
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
TQID: https://experienceleague.adobe.com/-MWpMACN0bFPIRAWejD0-VV5nG8BGAukmV1QXxXal-E
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 0%

---

# Verwalten von Unternehmenszielen {#manage-company-destinations}

Erstellen, Bearbeiten und Löschen von Audience Manager-Zielen.

<!-- t_company_destinations.xml -->

Detaillierte Informationen finden Sie unter [Ziele](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) im *Audience Manager-Benutzerhandbuch*.

## Erstellen oder Bearbeiten von Unternehmenszielen {#create-edit-company-destinations}

Scrollen Sie durch die Abschnitte, um schrittweise Anweisungen zum Erstellen neuer [!DNL Audience Manager] oder Bearbeiten vorhandener Ziele zu erhalten.

<!-- create-edit-company-destinations.xml -->

Besuchen Sie die Seite [Experience Cloud-Partnerintegration](https://wiki.corp.adobe.com/x/mPIMPw) bevor Sie Ziele einrichten. Die Seite enthält die spezifischen Informationen, die Sie für jede [!DNL Audience Manager]-Partnerintegration angeben müssen.

Wenn Ihr Client [!DNL Adobe Media Optimizer] als Ziel in [!DNL Audience Manager] verwenden möchte, müssen Sie dies in [!DNL Adobe Media Optimizer] einrichten.

## Navigieren Sie zur Registerkarte Ziele {#navigate-destinations}

1. Klicken Sie auf **[!UICONTROL Companies]**, suchen Sie dann das gewünschte Unternehmen und klicken Sie darauf, um dessen [!UICONTROL Profile] anzuzeigen. Sie können das [!UICONTROL Search] oder die Steuerelemente für die Paginierung unten in der Liste verwenden, um das gewünschte Unternehmen zu finden. Sie können jede Spalte in auf- oder absteigender Reihenfolge sortieren, indem Sie auf die Kopfzeile der gewünschten Spalte klicken.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Destinations]** .
1. Um ein neues Ziel zu erstellen, klicken Sie auf **[!UICONTROL Add Destination]**. Um ein vorhandenes Ziel zu bearbeiten, klicken Sie auf den Namen des Ziels in der Spalte **[!UICONTROL Name]** .

## Allgemeine Einstellungen {#basic-settings}

Füllen Sie die Felder im **[!UICONTROL Basic Settings]** aus.

* **[!UICONTROL Name]:** (Erforderlich) Geben Sie den Namen dieses Ziels an.
* **[!UICONTROL Description]:** Geben Sie beschreibende Informationen zu diesem Ziel an.
* **[!UICONTROL Type]:** (Erforderlich) Wählen Sie den gewünschten Zieltyp aus:
   * **[!UICONTROL Bulk ID]**: Synchronisieren von IDs zwischen verschiedenen Plattformen
   * **[!UICONTROL Bulk Trait]**: Senden Sie Eigenschafteninformationen stapelweise an verschiedene Plattformen.
   * **[!UICONTROL Bulk Segment]**: Senden Sie Segmentinformationen stapelweise an verschiedene Plattformen.
   * **[!UICONTROL S2S]**: Verwenden Sie Server-zu-Server-Ziele, um Echtzeit- und Batch-Daten an verschiedene Plattformen zu senden.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (nur [!UICONTROL S2S]) Option auswählen:
   * **[!UICONTROL Segment ID]:** Wenn Sie diese Einstellung auswählen, wird die Zielwert-Zuordnung mit der [!DNL Audience Manager] Segment-ID ausgefüllt.
   * **[!UICONTROL Integration Code Value]:** Wenn Sie diese Einstellung auswählen, wird die Zielwert-Zuordnung mit dem [!DNL Audience Manager] Segment-Integrations-Code gefüllt.
* **[!UICONTROL User ID Key]:** (Erforderlich) Wählen Sie den gewünschten Benutzer-ID-Schlüssel für dieses Ziel aus der Dropdown-Liste aus.

Diese ID wird als Master-Datenquellen-ID verwendet. Dadurch werden die Benutzer-IDs bestimmt, die in der Datei ausgehen sollen.

>[!NOTE]
>
>Für den [!UICONTROL Bulk ID] Zieltyp können Sie weder den [!DNL Audience Manager]-[!UICONTROL User ID] noch die [!DNL Adobe Experience Cloud]-ID verwenden.

Wenn Ihre Datenquellen-ID ([!UICONTROL DPID]) nicht in der Dropdown-Liste angezeigt wird, müssen Sie auf der Seite „Einstellungen für Data Source[ das Kontrollkästchen **[!UICONTROL Outbound]** auf der Ebene der Datenquelle ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Erforderlich) Wählen Sie die gewünschte Datenquelle für dieses Ziel aus der Dropdown-Liste aus. Diese Einstellung ermöglicht die Kennzeichnung ausgehender Daten, was die Aufnahme in separate Client-seitige Systeme ermöglicht.
* **[!UICONTROL Foreign Account ID]:** Geben Sie die ID des ausländischen Kontos für dieses Ziel an. Dies ist der Identifikationswert im System des Empfängers für diese ausgehenden Daten.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Wenn die Gesamtmenge der zurückgegebenen Daten unbekannt ist, verwenden Sie diese Einstellung, um nur eine Stichprobenmenge der Daten und nicht die vollständige Menge zurückzugeben. Passen Sie die Zahl hier an, um einen Bruchteil der Daten darzustellen (z. B. gibt ein Wert von „100“ 1/100 der regulären Datenmenge zurück, ein Wert von „10“ gibt 1/10 der regulären Datenmenge zurück). Der Standardwert lautet „1“ und gibt alle Daten zurück.

## Echtzeitdaten (für S2S-Ziele) {#realtime-s2s}

Wenn Sie ein [!UICONTROL S2S] Ziel erstellen, füllen Sie die folgenden Felder aus:

**[!UICONTROL Servers]**: Wählen Sie den gewünschten `HTTP` für dieses Ziel aus.
**[!UICONTROL Format]**: Wählen Sie das gewünschte Format für dieses Ziel aus der Dropdown-Liste aus: [!UICONTROL HTTP only].

>[!NOTE]
>
>Nur zur [!DNL S2S] können Sie [!UICONTROL Realtime] oder [!UICONTROL Batch] Ziele mithilfe der Ein-/Aus-Schieberegler auf dem Bildschirm aktivieren oder deaktivieren. Sie können nicht beide Optionen deaktivieren.

## Batch-Daten {#batch-data}

Für [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] oder [!UICONTROL Bulk Segment] Ziele füllen Sie die folgenden Felder aus:

* **[!UICONTROL Protocol]**: (Erforderlich) Wählen Sie das gewünschte Protokoll für dieses Ziel aus der Dropdown-Liste aus:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Erforderlich) Wählen Sie den gewünschten Server für dieses Ziel aus der Dropdown-Liste aus.
* **[!UICONTROL Format]**: (Erforderlich) Wählen Sie das gewünschte Format für dieses Ziel aus der Dropdown-Liste aus: [!DNL HTTP] oder Dateityp, je nach dem oben ausgewählten Protokoll.
* **[!UICONTROL Sync Type]**: (Erforderlich) Wählen Sie den gewünschten Synchronisierungstyp für dieses Ziel aus. Dies gibt die Anzahl der Benutzeraktivitäten an, die Kunden in die ausgehenden Bestellungen einbeziehen möchten. Wählen Sie **[!UICONTROL Customer]** aus, wenn Kunden nur an der Analyse von Segmentqualifikationen anhand ihrer Eigenschaften interessiert sind. Wählen Sie **[!UICONTROL Platform]** aus, wenn Segmentqualifikationen aus Offsite-Aktivitäten für alle [!DNL Audience Manager] Kunden einbezogen werden sollen.
* **[!UICONTROL Customer]**: Die Datei enthält aktive Benutzende, bei denen für den ausgewählten Zeitraum mindestens eine Eigenschaft nur in den Eigenschaften des Clients (verknüpft mit dem [!UICONTROL PID] des Clients) realisiert wurde. Ihre Kunden sollten diese Option verwenden, um ihre *-Segmentqualifikationen* Echtzeit an Ziele auszugeben.
* **[!UICONTROL Platform]**: Die Datei enthält aktive Benutzende, die über mindestens 1 Echtzeit-Interaktion verfügen, sei es ID-Synchronisierung oder Eigenschaftsrealisierung, überall in den Eigenschaften [!DNL Audience Manager] Clients (allen Client-PIDs zugeordnet) für den ausgewählten Zeitraum. Ihre Kunden sollten diese Option verwenden, um ihre *insgesamt* Segmentqualifikationen an Ziele auszugeben.
* **[!UICONTROL Lifetime]**: Die Datei enthält aktive Benutzer, die seit der Erstellung des Ziels überall in [!DNL Audience Manager] Eigenschaften der Clients angezeigt wurden.
* **[!UICONTROL Sync Type Lookback Period]**: Wenn Sie [!UICONTROL Customer] oder [!UICONTROL Platform] auswählen, wählen Sie einen Zeitraum aus. Dateien enthalten aktive Benutzer für den ausgewählten Zeitraum.
Wählen Sie als Nächstes den Bestelltyp aus. Gibt die Häufigkeit und den Umfang jeder ausgehenden Integration mit Partnern an. Wählen Sie zwischen inkrementeller und vollständiger Bestellung.
* **[!UICONTROL Incremental Scheduled Run]**: Bei jedem Durchlauf geben [!DNL Audience Manager] nur die neuen Benutzer aus, die seit dem vorherigen ausgehenden Auftrag qualifiziert sind. Wählen Sie den gewünschten Zeitraum aus, für den Sie inkrementelle Synchronisierungsprozesse durchführen [!DNL Audience Manager]. Sie können beispielsweise alle 24 Stunden, alle sieben Tage, alle 30 Tage oder nie auswählen.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Die erste inkrementelle Reihenfolge entspricht einer vollständigen Reihenfolge, da noch nie zuvor Benutzende an das Ziel gesendet wurden.

* **[!UICONTROL Full Sync Scheduled Run]**: Bei jeder Ausführung gehen [!DNL Audience Manager] alle aktiven Benutzer seit der Ersteinrichtung des Ziels aus. Wählen Sie den gewünschten Zeitplan aus, den Sie zur Durchführung vollständiger Synchronisierungsprozesse verwenden [!DNL Audience Manager]. Sie können beispielsweise alle 24 Stunden, alle sieben Tage, alle 30 Tage oder nie auswählen.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>Es wird empfohlen, inkrementelle Synchronisationen häufiger als vollständige Synchronisationen zu verwenden. Inkrementelle Synchronisationen senden nur Dateien, die neue Eigenschaftenerkennungen oder ID-Synchronisationen enthalten. Vollständige Synchronisationen senden alle Dateien, unabhängig davon, ob sie neue Realisierungen oder ID-Synchronisationen enthalten. Verwenden Sie die [!UICONTROL Full Sync Scheduled Run]-Konfiguration nur, wenn Clients eine vollständige Kopie aller Benutzer benötigen, um das Volumen der ausgehenden Daten zu reduzieren.

## Konfigurieren von Datenquellen {#configure-data-sources}

Für [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] oder [!UICONTROL Bulk Segment] Ziele füllen Sie die folgenden Felder aus. Mit diesen Einstellungen können Sie alle Daten (Eigenschaften, Segmente oder IDs, basierend auf dem ausgewählten Typ) senden, die mit den Datenquellen verknüpft sind.

* **[!UICONTROL All Unrestricted First Party Data]**: Wählen Sie diese Option aus, um alle Erstanbieter-Datenquellen zu verwenden. Wenn Sie diese Option auswählen, werden die [!UICONTROL Available Data Sources] deaktiviert.
* **[!UICONTROL Available Data Sources]**: Verwenden Sie die Pfeile, um Datenquellen zwischen den Feldern **[!UICONTROL Available Data Sources]** und **[!UICONTROL In File Data Sources]** zu verschieben.

## Speichern und abschließen {#save-and-finalize}

Die Schaltfläche **[!UICONTROL Save]** wird aktiviert, nachdem alle erforderlichen Felder ausgefüllt wurden. Klicken Sie auf **[!UICONTROL Save]** , um den Prozess zum Erstellen des Ziels abzuschließen.

## Unternehmensziele löschen {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

So löschen Sie ein Ziel:

1. Klicken Sie auf **[!UICONTROL Companies]**, suchen und klicken Sie auf das gewünschte Unternehmen und dann auf die Registerkarte **[!UICONTROL Destinations]** .
1. Klicken Sie in der Spalte **[!UICONTROL Actions]** des gewünschten Ziels auf ![](assets/icon_delete.png) .
1. Klicken Sie auf **[!UICONTROL OK]** , um den Löschvorgang zu bestätigen.

>[!NOTE]
>
>Sie können ein Ziel nicht löschen, wenn ihm Segmente zugeordnet sind.
