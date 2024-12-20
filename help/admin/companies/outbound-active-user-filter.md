---
description: Folgen Sie diesen Anweisungen, um eine vollständige Synchronisierungsdatei zu generieren, die nur die kürzlich aktiven Benutzer enthält. Sie können nach aktiven Benutzern filtern, um relevante Daten an ein Targeting-System auf der Site zu übertragen oder die Dateigröße zu begrenzen, die an eine DSP gesendet wird. Dieser Filter kann nicht mit inkrementeller Synchronisierung verwendet werden.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: Ausgehende Daten nur nach aktiven Benutzern filtern
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Ausgehende Daten nur nach aktiven Benutzern filtern {#filter-outbound-data-by-active-users-only}

Folgen Sie diesen Anweisungen, um eine vollständige Synchronisierungsdatei zu generieren, die nur die kürzlich aktiven Benutzer enthält. Sie können nach aktiven Benutzern filtern, um relevante Daten an ein Targeting-System auf der Site zu übertragen oder die Dateigröße zu begrenzen, die an eine DSP gesendet wird. Dieser Filter kann nicht mit inkrementeller Synchronisierung verwendet werden.

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
