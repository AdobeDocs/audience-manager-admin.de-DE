---
description: Einige Kunden möchten möglicherweise nicht ihren Zugriff auf den Amazon Simple Storage Service (Amazon S3) oder geheime Schlüssel zum Adobe bereitstellen, um das Hochladen von Zieldaten in ihre Buckets zu autorisieren.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Autorisieren des kontenübergreifenden Amazon S3-Bucket-Zugriffs für Batch-Ziele
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Autorisieren des kontenübergreifenden Amazon S3-Bucket-Zugriffs für Batch-Ziele{#authorize-cross-account-bucket-batch}

Einige Kunden möchten möglicherweise nicht ihren [!DNL Amazon S3] Zugriff oder ihre geheimen Schlüssel auf Adobe bereitstellen, um das Hochladen von Zieldaten in ihre Buckets zu autorisieren.

Eine Alternative, die wir unseren Kunden anbieten können, ist in [!DNL Amazon S3] [!UICONTROL Cross-Account Bucket Permissions]. Dieser Prozess wird in der Dokumentation zu [AWS beschrieben](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Gehen Sie wie folgt vor, um diese Alternative im Audience Manager zu aktivieren:

1. Navigieren Sie zu **[!UICONTROL Servers]** und wählen Sie **[!UICONTROL Create Server]** aus.
1. Wählen Sie **[!UICONTROL S3]** in der **[!UICONTROL Protocol/Credentials]** Dropdown-Maske aus.
1. Aktivieren Sie die Option **[!UICONTROL Use Internal Adobe Key]** .
1. Verwenden Sie das Konto und den Behälternamen Ihres Kunden in [!DNL Amazon S3].
1. Stellen Sie sicher, dass Ihr Kunde die `975822914085` des [!DNL Amazon S3] Kontos in seinem [!DNL S3] Bucket auflistet.

>[!NOTE]
>
>Unser Outbound-Publisher stellt sicher, dass die Berechtigungsstufe `bucket-owner-full-control` für hochgeladene Daten festgelegt wird, damit Ihr Kunde Inhaber dieser Daten sein kann.
