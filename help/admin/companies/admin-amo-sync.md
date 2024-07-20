---
description: Standardmäßig synchronisieren alle Unternehmen Daten mit Adobe Media Optimizer (AMO). In der Admin-Benutzeroberfläche verfügt jeder Unternehmens-Container über eine Datenquelle, die diesen Prozess verwaltet. Diese Datenquelle ist Adobe AMO (ID 411). Klicken Sie auf eine Behälterzeile (auf der Registerkarte Container ) für ein ausgewähltes Unternehmen, um diese Standardsynchronisierung zu deaktivieren oder dem AMO-Synchronisierungsprozess andere Datenquellen hinzuzufügen und zu entfernen.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: ID-Synchronisierung mit Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 2%

---

# ID-Synchronisierung mit Media Optimizer {#id-syncing-with-media-optimizer}

Standardmäßig synchronisieren alle Unternehmen Daten mit [!DNL Adobe Media Optimizer] ([!DNL AMO]). Im [!UICONTROL Admin UI] verfügt jeder Unternehmens-Container über eine Datenquelle, die diesen Prozess verwaltet. Diese Datenquelle ist [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Klicken Sie auf eine Containerzeile (auf der Registerkarte [!UICONTROL Containers] ) für ein ausgewähltes Unternehmen, um diese Standardsynchronisierung zu deaktivieren oder weitere Datenquellen zum Synchronisierungsprozess [!DNL AMO] hinzuzufügen und zu entfernen.

![](assets/id-sync.png)

## ID-Synchronisierungsstatus {#id-sync-status}

In der folgenden Tabelle wird der Synchronisierungsstatus einer Datenquelle beschrieben.

| Status | Beschreibung |
|------ | -------- |
| Aus | Entfernen Sie alle Datenquellen aus [!UICONTROL Selected Data Sources] für diesen Container, um die ID-Synchronisationen mit [!DNL AMO] zu deaktivieren. |
| On (unabhängig von der ID-Dienstversion) | Eine Datenquelle wird unabhängig von der Version des ID-Diensts mit [!DNL AMO] synchronisiert, wenn: <ul><li>Die Datenquelle wird in der Liste [!UICONTROL Selected Data Sources] angezeigt.</li><li>Das Kontrollkästchen [!DNL AMO] *ist nicht* ausgewählt.</li></ul> |
| On (unabhängig von der ID-Dienstversion) | Eine Datenquelle synchronisiert mit [!DNL AMO] mit dem ID-Dienst Version 2.0 (oder höher), wenn: <ul><li>Die Datenquelle wird in der Liste [!UICONTROL Selected Data Sources] angezeigt.</li><li>Das Kontrollkästchen [!DNL AMO] *ist* aktiviert.</li></ul> |

>[!MORELIKETHIS]
>
>* [Verwalten von Containern](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)
