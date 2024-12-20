---
description: Alle Aktualisierungen (Ergänzungen, Streichungen und Korrekturen) des Audience Manager Admin-Handbuchs nach Datum.
seo-description: All updates (additions, deletions, and corrections) to the Audience Manager Admin Guide, by date.
seo-title: Documentation Updates
title: Dokumentation – Aktualisierungen
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
exl-id: 8221b4df-99c2-47d3-a2ea-186a701a2b20
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 94%

---

# Dokumentation – Aktualisierungen {#documentation-updates}

Alle Aktualisierungen (Ergänzungen, Streichungen und Korrekturen) des Audience Manager Admin-Handbuchs nach Datum.

Informationen zu Funktionsversionen, Verbesserungen und Fehlerbehebungen finden Sie in den [Experience Cloud-Versionshinweisen](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=en). [!DNL Audience Manager] Dokumentationsänderungen finden Sie unter [Aktualisierungen der Dokumentation](https://experienceleague.adobe.com/docs/audience-manager/user-guide/documentation-updates/docs-2019.html?lang=en).

## Aktualisierungen der Dokumentation zu AAM 2019 {#aam-2019-docs-updates}

| Thema | Beschreibung |
|--- |--- |
| HTTP-Formatmakros | Wir haben ein neues Makro `REGION_ID_LIST` und drei neue Felder `sda`, `sda` und `sda` zum Makro `USER_LIST` hinzugefügt. |
| HTTP-Formatmakros | Es wurden zwei neue Makros hinzugefügt: `ECID` und `MCID`. |

## Aktualisierungen der Dokumentation zu AAM 2018 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Thema </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Erstellen und Bearbeiten von FTP-Servern</a> </p> </td> 
   <td colname="col2"> <p>Es wurden weitere Informationen zur SSH-Schlüsselauthentifizierung für SFTP-Server hinzugefügt (Schritt 5). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Einrichten Ihrer Ziele für den Export von Experience Cloud ...</a> </p> </td> 
   <td colname="col2"> <p>Auf dieser Seite erfahren Sie, wie Sie Ziele einrichten, um Daten zu exportieren, die mit dem gewünschten ID-Typ in ausgehenden Datendateien versehen sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> Gewusst wie: Autorisieren des kontoübergreifenden Amazon S3-Behälterzugriffs für Batch-Ziele</a> </p> </td> 
   <td colname="col2"> <p>Unsere Kunden können in Amazon S3 kontoübergreifende Behälterzugriffsberechtigungen für ausgehende Dateien verwenden, wenn sie es vorziehen, keine Zugriffsschlüssel oder geheime Schlüssel für Amazon S3 freizugeben. In diesem Dokument erfahren Sie, wie Sie diese Alternative in der Audience Manager Admin-Benutzeroberfläche einrichten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aktualisierungen der Dokumentation zu AAM 2017 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Thema </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-Formatmakros</a> </td> 
   <td colname="col2">Das Makro <code>segmentId</code> wurde mit <code>legacySegmentId</code> ersetzt und das Makro <code>newSegmentId</code> hinzugefügt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> Verwalten von Firmenbeschränkungen</a> </td> 
   <td colname="col2"> Die Dokumentation der Beschränkungen wurde um die maximale Anzahl an Eigenschaftsordnern und die maximale Strukturtiefe für Eigenschaften erweitert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> Aktivieren von ausgehenden Hadoop-Sequenzdateitransfers</a> </td> 
   <td colname="col2"> Erfahren Sie, wie Sie Kunden in die Lage versetzen können, ausgehende SEQ-Dateien an ihre eigene Hadoop-Instanz zu senden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> Verwalten von Containern</a> </td> 
   <td colname="col2"> Es wurde eine kurze Anleitung zum Erstellen von Containern hinzugefügt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> Erstellen oder Bearbeiten von Firmenzielen</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">Es wurden Anweisungen zur ausgewogenen Verwendung vollständiger und inkrementeller Synchronisierungen hinzugefügt. </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7"><span class="keyword"> Adobe Media Optimizer</span> wird in <span class="keyword"> Adobe Media Optimizer</span> als ein <span class="keyword"> Audience Manager</span>-Ziel bereitgestellt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Verwalten von Firmenzielen</a> </p> </td> 
   <td colname="col2"> <p>Geringfügige Änderungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> ID-Synchronisierung mit Media Optimizer</a> </p> </td> 
   <td colname="col2"> <p>Neue Dokumentation, in der das Kontrollkästchen für die AMO-Synchronisierung in jedem Firmen-Container beschrieben wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> Gerätediagrammoptionen für Firmen</a> </p> </td> 
   <td colname="col2"> <p>Neue Dokumentation, in der die Konfiguration von Gerätediagrammoptionen beschrieben wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API-Anforderungen und -Empfehlungen</a> </p> </td> 
   <td colname="col2"> <p>Neue Dokumentation, in der einige Anforderungen und Empfehlungen beschrieben werden, die Sie kennen und an Kunden weitergeben sollten. Dies wird in den öffentlichen Dokumenten mit demselben Titel und Änderungen für eine andere Leserschaft dupliziert. Siehe <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=en#api-requirements-recommendations" format="https" scope="external">API-Anforderungen und -Empfehlungen</a> in den öffentlichen Dokumenten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aktualisierungen der Dokumentation zu AAM 2016 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Thema </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> Erstellen und Bearbeiten von FTP-Servern</a> </td> 
   <td colname="col2">Ausgangs-FTP IP <b>52.44.29.204</b> wurde hinzugefügt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Verwalten von Firmenzielen</a> </p> </td> 
   <td colname="col2"> <p>Geringfügige Änderungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> Erstellen und Bearbeiten von HTTP-Servern</a> </p> </td> 
   <td colname="col2"> <p>Dem Assistenten zum Erstellen von Server-Konfigurationen wurde die <b>HTTP-Signatur</b> hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> Beta-Umgebung</a> </p> </td> 
   <td colname="col2"> <p>Die URLs und Hostnamen in der Beta-Umgebung wurden aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> Filtern von ausgehenden Daten nur nach aktiven Benutzern</a> </p> </td> 
   <td colname="col2"> <p>Anweisungen zum Generieren einer vollständigen Synchronisierungsdatei, die nur aktive Benutzer enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP-Formatmakros</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>Neue Dokumentation, die eine Liste von HTTP-Makros und allgemeine Beispiele enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> Beispiele für HTTP-Formatmakros</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aktualisierungen der Dokumentation zu AAM 2015 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum und Thema </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dezember 2015 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formate</a> </p> </td> 
   <td colname="col2"> <p>Der Abschnitt zu den Makros wurde überarbeitet und Beispiele wurden hinzugefügt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aktualisierungen der Dokumentation zu AAM 2014 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum und Thema </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>12. November 2014 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formate</a> </p> </td> 
   <td colname="col2"> <p>Es wurden Informationen zum Makro &lt;MCID&gt; hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23. Oktober 2014 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> Erstellen oder Bearbeiten von Formaten</a> </p> </td> 
   <td colname="col2"> <p>Es wurden Informationen zur Empfangsoption <span class="wintitle"> .info </span> hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23. Oktober 2014 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> Formate</a> </p> </td> 
   <td colname="col2"> <p>Neue Seite. Beachten Sie, dass diese Seite noch in Bearbeitung ist und in den nächsten Tagen aktualisiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22. Oktober 2014 </p> <p><a href="admin-destination-troubleshooting.md#"> Fehlerbehebung bei der Zieleinrichtung</a> </p> </td> 
   <td colname="col2"> <p>Neues Thema. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21. Oktober 2014 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> Verwalten von Firmenzielen</a> </p> </td> 
   <td colname="col2"> <p>Das ganze Thema wurde überarbeitet. Es wurden zusätzliche Informationen und Einstellungen hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25. September 2014 </p> <p><a href="companies/admin-manage-company-profiles.md"> Erstellen von Firmen</a> </p> </td> 
   <td colname="col2"> <p>Es wurden zusätzliche Informationen zu den Abschnitten <span class="wintitle"> Lebenszyklus</span> und <span class="wintitle"> Kontotypen</span> hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25. September 2014 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> Bearbeiten von Firmenprofilen</a> </p> </td> 
   <td colname="col2"> <p>Es wurden zusätzliche Informationen zu den Abschnitten <span class="wintitle"> Lebenszyklus</span> und <span class="wintitle"> Kontotypen</span> hinzugefügt. </p> </td> 
  </tr> 
 </tbody> 
</table>
