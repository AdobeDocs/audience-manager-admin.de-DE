---
description: Um das versehentliche Einbinden von Dateien und Daten in Zieldatenquellen anderer Partner oder Kunden zu verhindern, hat Audience Manager eine Zuordnungsanforderung zwischen Partner-ID (PID) und den Datenquellen anderer Partner hinzugefügt.
title: Onboarding-Zugriff für Zweitanbieterdaten verwalten
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Onboarding-Zugriff für Daten von Zweitanbietern verwalten {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> Die Zielgruppe für diese Seite sind Adobe-interne Mitarbeiter. Wenn Sie Audience Manager sind und eine Zuordnung zu einer Datenquelle von Zweitanbietern wie auf dieser Seite beschrieben anfordern, wenden Sie sich an die Kundenunterstützung oder Ihren technischen Kundenbetreuer.
> Beachten Sie, dass nicht erforderlich ist, um eine Zuordnung für bestehende Datenfreigabe-Beziehungen anzufordern. Die Zuordnung ist auch nicht erforderlich, wenn Daten in Zieldatenquellen integriert werden, die zu Ihrer PID gehören.

Um das versehentliche Einbinden von Dateien und Daten in Zieldatenquellen anderer Partner zu verhindern, hat der Audience Manager eine Zuordnungsanforderung zwischen Partner-ID (PID) und Datenquellen (DPID) anderer Partner hinzugefügt. Weitere Informationen zu PID und DPID finden Sie im [Index der Audience Manager-IDs](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

Wenn ein Audience Manager-Partner oder -Kunde zu Zwecken der Datenfreigabe von Zweitanbietern Dateien in eine Zieldatenquelle aufnehmen möchte, deren Eigentümer er nicht ist, muss er eine Zuordnung zwischen seiner Partner-ID (PID) und dieser spezifischen Datenquelle (DPID) anfordern. Wenn die Zuordnung fehlt, werden die Dateien nicht vom eingehenden Datenauftrag verarbeitet und die Daten werden nicht in Audience Manager integriert.

Um dieses Mapping zu erstellen, senden Sie ein Jira-Ticket an das Audience Manager-Engineering-Team. Sehen Sie sich ein Jira-Beispielticket [hier](https://jira.corp.adobe.com/browse/AAM-60353) an. Sie müssen keine Zuordnungen für bestehende Datenfreigabe-Beziehungen anfordern.
