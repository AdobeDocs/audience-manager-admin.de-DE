---
description: Die Beta-Umgebung dient zum Testen von Audience Manager-Implementierungen. In der Beta-Version vorgenommene Änderungen wirken sich nicht auf die Produktionsdaten aus. Die Audience Manager-Beta-Umgebung ist eine kleinere, eigenständige Version der Produktionsumgebung. Alle Daten, die getestet werden sollen, müssen in dieser Umgebung eingegeben und erfasst werden.
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: Beta-Umgebung
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---

# Beta-Umgebung {#beta-environment}

Die Beta-Umgebung dient zum Testen von Audience Manager-Implementierungen. In der Beta-Version vorgenommene Änderungen wirken sich nicht auf die Produktionsdaten aus. Die Audience Manager-Beta-Umgebung ist eine kleinere, eigenständige Version der Produktionsumgebung. Alle Daten, die getestet werden sollen, müssen in dieser Umgebung eingegeben und erfasst werden.

## Überblick {#overview}

<!-- beta_environment_admin.xml -->

| Service | URL/Hostname | Schritte zur Bereitstellung |
|--- |--- |--- |
| S3 | | Siehe [Bereitstellen von Amazon S3-Buckets](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https&amp;colon;//dcs-beta.demdex.net/… | Keine zusätzlichen Schritte von unserer Seite erforderlich. Siehe [Zugriff auf den DCS in der Beta-Umgebung](admin-beta-environment.md#access-dcs-beta-environment). |
| Benutzeroberfläche | https&amp;colon;//bank-beta.demdex.com | Die Daten werden monatlich aus der Produktion in die Beta-Umgebung kopiert. Die Produktions-Anmeldedaten sind für die Beta-Version gültig. |
| API | https&amp;colon;//api-beta.demdex.com/… | Die Daten werden monatlich aus der Produktion in die Beta-Umgebung kopiert. Die Produktions-Anmeldedaten sind für die Beta-Version gültig. |

## Amazon S3-Buckets bereitstellen {#provision-s3-buckets}

>[!NOTE]
>
>Wir bewegen uns weg von [!DNL FTP/SFTP]. Beachten Sie außerdem, dass ausgehende Datenübertragungen in der Beta-Umgebung nicht funktionieren.

So stellen Sie [!DNL S3] Buckets für eingehende Daten bereit:

1. Verwenden Sie die [**SKMS Request TechOps Help**](https://skms.adobe.com/)-Funktion.
1. Navigieren Sie zu **[!UICONTROL Request TechOps Help]** in der linken Navigationsleiste.
1. Geben Sie **[!UICONTROL Request Search]** in das Suchfeld Audience Manager ein.
1. Scrollen Sie in den Suchergebnissen nach unten und klicken Sie auf **Audience Manager - S3 Inbound/Outbound Account Provisioning**.
1. Füllen Sie die Felder im Bereitstellungsfenster aus und geben Sie **Feld „Sandbox** Umgebung“ **[!UICONTROL Environment]**.

>[!NOTE]
>
>Wir raten von der Verwendung von [!DNL FTP/SFTP] ab und fördern die Verwendung von [!UICONTROL Amazon S3]. Die Gründe, warum wir die Verwendung von [!UICONTROL Amazon S3] empfehlen, sind in [Amazon S3:About](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) aufgeführt.

## Zugreifen auf den DCS in der Beta-Umgebung {#access-dcs-beta-environment}

So greifen Sie in der Beta-Umgebung auf die [!UICONTROL DCS] zu:

1. Führen Sie einen [!UICONTROL DCS]-Aufruf mit dem [!DNL curl] [Befehl](https://curl.haxx.se/docs/manpage.html) durch. [!DNL Curl] ist ein Tool zum Übertragen von Daten von oder auf einen Server mithilfe eines von vielen unterstützten Protokollen.

   Beispiel: `curl -v https://dcs-beta.demdex.net/event`

1. Stellen Sie sicher, dass Ihre Anfrage im Beta-[!UICONTROL DCS] verarbeitet wurde, indem Sie im [!DNL sandbox]-Antwortheader nach &quot;[!UICONTROL DCS]&quot; suchen.

   Beispiel:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
