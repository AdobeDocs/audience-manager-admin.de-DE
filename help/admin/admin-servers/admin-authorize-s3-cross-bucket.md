---
description: Manche Kunden möchten Adobe möglicherweise keinen Zugriff auf den Amazon Simple Storage Service (Amazon S3) oder geheime Schlüssel bereitstellen, um das Hochladen von Zieldaten in ihre Buckets zu genehmigen.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Autorisieren des kontoübergreifenden Amazon S3-Behälterzugriffs für Batch-Ziele
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Autorisieren des kontoübergreifenden Amazon S3-Behälterzugriffs für Batch-Ziele{#authorize-cross-account-bucket-batch}

Einige Kunden möchten möglicherweise nicht ihren [!DNL Amazon S3] -Zugriff oder geheime Schlüssel für Adobe bereitstellen, um das Hochladen von Zieldaten in ihre Buckets zu genehmigen.

Eine Alternative, die wir unseren Kunden anbieten können, ist [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Dieser Vorgang wird in der [AWS-Dokumentation](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html) beschrieben. Gehen Sie wie folgt vor, um diese Alternative in Audience Manager zu aktivieren:

1. Gehen Sie zu **[!UICONTROL Servers]** und wählen Sie **[!UICONTROL Create Server]** aus.
1. Wählen Sie **[!UICONTROL S3]** in der Dropdownmaske **[!UICONTROL Protocol/Credentials]** aus.
1. Aktivieren Sie die Option **[!UICONTROL Use Internal Adobe Key]** .
1. Verwenden Sie den Konto- und Behälternamen Ihres Kunden in [!DNL Amazon S3].
1. Stellen Sie sicher, dass Ihr Kunde die [!DNL Amazon S3] Konto `975822914085` auf seinem [!DNL S3] Bucket auflistet.

>[!NOTE]
>
>Unser ausgehender Herausgeber stellt sicher, dass die Berechtigungsebene `bucket-owner-full-control` für hochgeladene Daten festgelegt wird, damit Ihr Kunde Eigentümer dieser Daten sein kann.
