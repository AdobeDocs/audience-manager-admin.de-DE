---
description: Listet die Makros auf, mit denen Sie FTP-basierte Datendateien erstellen können. Einige Makros können für alle Datendateifelder und -zeilen verwendet werden. Andere Makros sind nur für Kopfzeilen und Datenzeilen spezifisch.
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: Dateiformatmakros
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 1%

---

# Dateiformatmakros {#file-format-macros}

Listet die Makros auf, mit denen Sie [!DNL FTP]-basierte Datendateien erstellen können. Einige Makros können für alle Datendateifelder und -zeilen verwendet werden. Andere Makros sind nur für Kopfzeilen und Datenzeilen spezifisch.

## Häufige Makros {#common-macros}

Diese Makros können in jedem Formatfeld verwendet werden. Beispiele finden Sie unter [Beispiele für Dateiformatmakros](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Ein nicht druckbares ASCII-Zeichen. Er gibt den Anfang einer Zeile oder eines Inhaltsabschnitts an. Sie kann auch zum Trennen von Datenspalten in einer Datei verwendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>Target-Datenanbieter-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>Benutzer-ID-Schlüssel Datenanbieter-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>Bestell-/Ziel-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>Alias für eine Bestell-/Ziel-ID. </p> <p>Der Wert für diesen Alias wird im Feld <span class="wintitle"> ID des ausländischen Kontos </span> für ein Ziel festgelegt (im Abschnitt <span class="wintitle"> Grundlegende Einstellungen </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Gibt den Synchronisierungstyp an. Akzeptiert die folgenden optionalen Variablen: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Vollständige Synchronisierung. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Inkrementelle Synchronisation. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Gibt die Datenübertragungsmethode an. Akzeptiert die folgenden optionalen Variablen: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Ein 10-stelliger UTC-, Unix-Zeitstempel. </p> <p>Sie kann auch als <code>YYYYMMDDhhmmss</code> entsprechend den Java-Formatierungsregeln für Datum/Zeitstempel formatiert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kopfzeilenfeldmakros {#header-field-macros}

Makros, die nur in Kopfzeilenfeldern verwendet werden. Beispiele finden Sie unter [Beispiele für Dateiformatmakros](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Dieses Makro wird als Trennzeichen verwendet und fügt eine Registerkarte zwischen Feldern ein. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Datenzeilenmakros {#data-row-macros}

Nur in Datenzeilen verwendete Makros. Beispiele finden Sie unter [Beispiele für Dateiformatmakros](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makro </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Fügt eine geschlossene geschweifte Klammer <code>}</code> ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Fügt ein Komma ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Unique User Identifier für Datenpartner </span>. Gibt die ID zurück, die Sie einem Benutzer/Site-Besucher zugewiesen haben, wenn diese ID bereits mit einer Geräte-ID des Typs <span class="keyword"> Audience Manager </span> synchronisiert wurde. </p> <p>Wenn die DPID 0 beträgt, gibt dieses Makro die Kennung <span class="keyword"> Audience Manager </span> anstelle Ihrer ID für den Benutzer zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Gibt eine Liste mit mehreren IDs für einen Datenpartner zurück. Dies ist nützlich, wenn Sie eine große Organisation mit mehreren Unterteilungen oder anderen Organisationsgruppen haben, für die Sie Daten freigeben können. Dieses Makro gibt eine Liste der IDs für diese untergeordneten Gruppen zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>Die Ausgabe dieses Makros ordnet die Datenanbieter-ID (DPID) den zugehörigen eindeutigen Benutzer-IDs (DPUUID) zu. Dieses Makro muss über eine Formatierungszeichenfolge verfügen, um seine Ausgabe zu steuern. Die Beispielausgabe würde wie folgt aussehen: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>Die Einstellung <code>maxMappings</code> bestimmt, wie viele Zuordnungen das Makro zurückgeben soll. Wenn <code>maxMappings=0</code>, gibt dieses Makro alle Zuordnungen für jede angegebene DPID zurück. Die Daten werden nach Zeitstempel sortiert (neueste zuerst) und geben die Ergebnisse mit dem größten Zeitstempel zuerst zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Erforderlich bei Verwendung der bedingten Makros <code>if</code> und <code>SEGMENT_LIST</code> und <code>REMOVED_SEGMENT_LIST</code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Diese Kombination von Makros erstellt eine bedingte Anweisung, die auflistet, aus welchen Segmenten die Benutzer zu <i>und</i> gehören, entfernt wurden. Es wird eine leere Zeichenfolge zurückgegeben, wenn beide Bedingungen nicht erfüllt sind oder keine Daten vorliegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Fügt eine geöffnete geschweifte Klammer <code>{</code> ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Herabgestuft. Nicht verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Herabgestuft. Nicht verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Gibt <code>1</code> als statischen, fest codierten Wert zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>Partner-ID (PID). Die PID wird auf der Registerkarte <span class="wintitle"> Profil </span> in der Administrator-Benutzeroberfläche angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Gibt eine Liste mit entfernten Segmenten zurück, falls vorhanden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Gibt eine Liste von Segmenten in einer Liste zurück. Akzeptiert die folgenden optionalen Variablen: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: Legacy-ID. Herabgestuft. Verwenden Sie <code>sid</code> (nur Kleinbuchstaben). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: Legacy-ID. Herabgestuft. Verwenden Sie <code>sid</code> (nur Kleinbuchstaben). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: Segment-ID. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Gibt <code>5</code> zurück, einen statischen, fest codierten Wert, der Daten als Segmentdaten identifiziert. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Zuordnung des Segments. Herabgestuft. Verwenden Sie <code>sid</code> (nur Kleinbuchstaben). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: Ein Unix-Zeitstempel, der angibt, wann ein Segment zuletzt realisiert wurde. </li> 
    </ul> <p>Setzen Sie diese Variablen in geschweifte Klammern hinter das Makro. Dieser Code trennt beispielsweise die Ergebnisse mit dem senkrechten Strich "|": <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Gibt <code>1</code> als statischen, fest codierten Wert zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Fügt ein Tabulatortrennzeichen ein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Gibt eine Liste von Eigenschaften zurück. Akzeptiert die folgenden optionalen Argumente: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Eigenschaftstypen, die durch eine numerische ID identifiziert werden. Diese Variable gibt zurück: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> , der eine DPM-Eigenschaft angibt (offline, von einem eingehenden Auftrag integriert). </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code>, der eine regelbasierte Eigenschaft angibt (Echtzeit,; über den <span class="wintitle"> DCS </span> integriert). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: Eigenschaften-ID. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> 0: Das letzte Mal, dass die Eigenschaft realisiert wurde. <code>lastRealized</code> Unix-Zeitstempel. </li> 
    </ul> <p>Setzen Sie diese Variablen in geschweifte Klammern hinter das Makro. Dieser Code trennt beispielsweise die Ergebnisse mit dem senkrechten Strich "|": <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> Benutzer-ID. </p> </td> 
  </tr> 
 </tbody> 
</table>
