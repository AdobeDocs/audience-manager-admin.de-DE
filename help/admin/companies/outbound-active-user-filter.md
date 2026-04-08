---
description: Folgen Sie diesen Anweisungen, um eine vollständige Synchronisierungsdatei zu generieren, die nur die kürzlich aktiven Benutzer enthält. Sie können nach aktiven Benutzern filtern, um relevante Daten an ein Targeting-System auf der Site zu übertragen oder die Größe der an eine DSP gesendeten Dateien zu begrenzen. Dieser Filter kann nicht mit inkrementeller Synchronisierung verwendet werden.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: Ausgehende Daten nur nach aktiven Benutzern filtern
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
TQID: https://experienceleague.adobe.com/rr6ABB4pgrhkWG88VenqIcbyAaPQfbg258M6SVdE28k
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Ausgehende Daten nur nach aktiven Benutzern filtern {#filter-outbound-data-by-active-users-only}

Folgen Sie diesen Anweisungen, um eine vollständige Synchronisierungsdatei zu generieren, die nur die kürzlich aktiven Benutzer enthält. Sie können nach aktiven Benutzern filtern, um relevante Daten an ein Targeting-System auf der Site zu übertragen oder die Größe der an eine DSP gesendeten Dateien zu begrenzen. Dieser Filter kann nicht mit inkrementeller Synchronisierung verwendet werden.

>[!NOTE]
>
>Ein Besucher muss nicht auf einer ausgewählten Kunden-Site oder in seinem Anzeigen-Traffic gesehen werden, um als „aktiv“ zu gelten. Sie können von jedem [!DNL Audience Manager] Kunden oder Partner gesehen werden, der als „aktiv“ eingestuft wird.

So filtern Sie nur nach aktiven Benutzern:

1. Klicken Sie auf **[!UICONTROL Companies]**.
1. Wählen Sie das Unternehmen aus, mit dem Sie arbeiten möchten, und klicken Sie auf **[!UICONTROL Destinations]**.
1. Legen Sie im Abschnitt [!UICONTROL Batch Data] die folgenden Optionen fest:

   * **[!UICONTROL Sync Type]**: Wählen Sie **[!UICONTROL Customer]** oder **[!UICONTROL Platform]** aus.
   * **[!UICONTROL Sync Type Lookback Period]**: Dieses Zeitintervall definiert den Bereich Ihrer Datendatei. Zur Auswahl stehen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: **[!UICONTROL Never]** auswählen. Denken Sie daran, dass dieser Filter nur für vollständige Synchronisierungsdateien gilt.
   * **[!UICONTROL Full Sync Scheduled Run]**: Dadurch wird festgelegt, wie oft Sie diese Datei erhalten möchten. Die Optionen sind **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** oder **[!UICONTROL Never]** (zum Deaktivieren).

1. Klicken Sie auf **[!UICONTROL Save]**.
