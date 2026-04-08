---
description: Standardmäßig synchronisieren alle Unternehmen Daten mit Adobe Media Optimizer (AMO). In der Admin-Benutzeroberfläche verfügt jeder Unternehmens-Container über eine Datenquelle, die diesen Prozess verwaltet. Diese Datenquelle ist Adobe AMO (ID 411). Klicken Sie auf eine Container-Zeile (unter der Registerkarte Container ) für ein ausgewähltes Unternehmen, um diese Standardsynchronisierung zu deaktivieren oder andere Datenquellen zum AMO-Synchronisierungsvorgang hinzuzufügen und zu entfernen.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: ID-Synchronisierung mit Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
TQID: https://experienceleague.adobe.com/R6xtPWC964J1atGK-R0g6J5AG83PYJosHNE3-5LvMVE
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 2%

---

# ID-Synchronisierung mit Media Optimizer {#id-syncing-with-media-optimizer}

Standardmäßig synchronisieren alle Unternehmen Daten mit [!DNL Adobe Media Optimizer] ([!DNL AMO]). In der [!UICONTROL Admin UI] verfügt jeder Unternehmens-Container über eine Datenquelle, die diesen Prozess verwaltet. Diese Datenquelle ist [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Klicken Sie auf eine Container-Zeile (unter der Registerkarte [!UICONTROL Containers]) für ein ausgewähltes Unternehmen, um diese Standardsynchronisierung zu deaktivieren oder andere Datenquellen zum [!DNL AMO] hinzuzufügen und zu entfernen.

![](assets/id-sync.png)

## ID-Synchronisierungsstatus {#id-sync-status}

Die folgende Tabelle beschreibt den Synchronisierungsstatus einer Datenquelle.

| Status | Beschreibung |
|------ | -------- |
| Aus | Entfernen Sie alle Datenquellen aus [!UICONTROL Selected Data Sources] für diesen Container, um die ID-Synchronisierung mit [!DNL AMO] zu deaktivieren |
| Ein (unabhängig von der ID-Service-Version) | Eine Datenquelle synchronisiert mit [!DNL AMO] unabhängig von der ID-Service-Version, wenn: <ul><li>Die Datenquelle wird in der Liste [!UICONTROL Selected Data Sources] angezeigt.</li><li>Das [!DNL AMO] Kontrollkästchen *ist nicht* aktiviert.</li></ul> |
| Ein (unabhängig von der ID-Service-Version) | Eine Datenquelle wird mit [!DNL AMO] mit ID-Service Version 2.0 (oder höher) synchronisiert, wenn: <ul><li>Die Datenquelle wird in der Liste [!UICONTROL Selected Data Sources] angezeigt.</li><li>Das [!DNL AMO] Kontrollkästchen *ist* aktiviert.</li></ul> |

>[!MORELIKETHIS]
>
>* [Verwalten von Containern](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)
