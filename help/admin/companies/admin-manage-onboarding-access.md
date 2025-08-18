---
description: Um zu verhindern, dass Dateien und Daten versehentlich in Zieldatenquellen anderer Partner oder Kunden eingefügt werden, hat Audience Manager eine Zuordnungsanforderung zwischen der Partner-ID (PID) und den Datenquellen anderer Partner hinzugefügt.
title: Verwalten des Onboarding-Zugriffs für Second-Party-Daten
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Verwalten des Onboarding-Zugriffs für Second-Party-Daten {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> Die Zielgruppe für diese Seite sind Adobe-interne Mitarbeiter. Wenn Sie Audience Manager-Kunde sind und eine Zuordnung von Zweitanbieter-Datenquellen anfordern, wie auf dieser Seite beschrieben, wenden Sie sich an die Kundenunterstützung oder Ihren technischen Kundenbetreuer.
> &#x200B;> Beachten Sie, dass nicht erforderlich ist, um eine Zuordnung für bestehende Datenfreigabe-Beziehungen anzufordern. Die Zuordnung ist auch nicht erforderlich, wenn Daten in Zieldatenquellen integriert werden, die zu Ihrer PID gehören.

Um zu verhindern, dass Dateien und Daten versehentlich in Zieldatenquellen anderer Partner eingefügt werden, hat Audience Manager eine Zuordnungsanforderung zwischen der Partner-ID (PID) und den Datenquellen (DPID) anderer Partner hinzugefügt. Weitere Informationen zu PID und DPID finden Sie im [Index von Audience Manager IDs](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

Wenn Audience Manager-Partner oder -Kundinnen bzw. -Kunden zu Zwecken der Datenfreigabe von Zweitanbietern Dateien in eine Zieldatenquelle aufnehmen möchten, deren Eigentümer bzw. Eigentümerin sie nicht ist, müssen sie eine Zuordnung zwischen ihrer Partner-ID (PID) und dieser spezifischen Datenquelle (DPID) anfordern. Wenn die Zuordnung fehlt, werden die Dateien vom eingehenden Datenauftrag nicht verarbeitet und die Daten werden nicht in Audience Manager integriert.

Um diese Zuordnung zu erstellen, reichen Sie ein Jira-Ticket beim Audience Manager-Entwicklungsteam ein. Sehen Sie sich ein Beispiel-Jira-Ticket [hier](https://jira.corp.adobe.com/browse/AAM-60353) an. Für vorhandene Datenfreigabe-Beziehungen müssen keine Zuordnungen erstellt werden.
