---
description: Die Gerätediagramm-Optionen stehen Unternehmen zur Verfügung, die an der Adobe Experience Cloud Device Co-op teilnehmen. Wenn ein Kunde auch eine vertragliche Beziehung zu einem Drittanbieter von Gerätediagrammen hat, der in Audience Manager integriert ist, werden in diesem Abschnitt Optionen für dieses Gerätediagramm angezeigt. Diese Optionen befinden sich unter Unternehmen > Firmenname > Profil > Gerätediagramm-Optionen.
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: Gerätediagramm-Optionen für Unternehmen
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---

# Gerätediagramm-Optionen für Unternehmen {#device-graph-options-for-companies}

Die [!UICONTROL Device Graph Options] stehen Unternehmen zur Verfügung, die an der [!DNL Adobe Experience Cloud Device Co-op] teilnehmen. Wenn ein Kunde auch eine vertragliche Beziehung zu einem Drittanbieter von Gerätediagrammen hat, der in Audience Manager integriert ist, werden in diesem Abschnitt Optionen für dieses Gerätediagramm angezeigt. Diese Optionen befinden sich unter [!UICONTROL Companies] > Firmenname > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

In dieser Abbildung werden generische Namen für die Diagrammoptionen von Drittanbietergeräten verwendet. In der Produktion stammen diese Namen vom Gerätediagramm-Anbieter und können von dem abweichen, was hier gezeigt wird. Zum Beispiel die [!DNL LiveRamp] Optionen für gewöhnlich (aber nicht immer):

* Mit &quot;[!DNL LiveRamp]&quot; beginnen
* Einen zweiten, variierenden Namen enthalten
* Mit &quot;[!UICONTROL - Household]&quot; oder &quot;[!UICONTROL -Person]&quot; enden

## Definierte Optionen für Gerätediagramm {#device-graph-options-defined}

Die hier ausgewählten Gerätediagramm-Optionen machen die [!UICONTROL Device Options] Optionen, die einem [!DNL Audience Manager] Kunden beim Erstellen eines [!UICONTROL Profile Merge Rule] zur Verfügung stehen, verfügbar oder blenden sie aus.

### Gerätediagramm für Kooperation {#co-op-graph}

Kunden, die an der [Adobe Experience Cloud Device Co-op teilnehmen, &#x200B;](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=de) diese Optionen, um eine [!UICONTROL Profile Merge Rule] mit (deterministischen [&#x200B; probabilistischen Daten) &#x200B;](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=de). Der [!DNL Corporate Provisioning Team] aktiviert und deaktiviert diese Option über einen Backend-[!DNL API]. Sie können diese Kontrollkästchen im [!DNL Admin UI] nicht aktivieren oder deaktivieren. Außerdem schließen sich die **[!UICONTROL Co-op Device Graph]**- und **[!UICONTROL Company Device Graph]** gegenseitig aus. Kunden können uns bitten, die eine oder die andere zu aktivieren, aber nicht beide. Wenn diese Option aktiviert ist, wird das **[!UICONTROL Co-op Device Graph]**-Steuerelement in den [!UICONTROL Device Options] für eine [!UICONTROL Profile Merge Rule] verfügbar gemacht.

![](assets/adminUI1.png)

### Gerätediagramm für Unternehmen {#company-graph}

Diese Option richtet sich an [!DNL Analytics] Kunden, die die [!UICONTROL People] in ihrer [!DNL Analytics] Report Suite verwenden. Der [!DNL Corporate Provisioning Team] aktiviert und deaktiviert diese Option über einen Backend-[!DNL API]. Sie können diese Kontrollkästchen im [!DNL Admin UI] nicht aktivieren oder deaktivieren. Außerdem schließen sich die **[!UICONTROL Company Device Graph]**- und **[!UICONTROL Co-op Device Graph]** gegenseitig aus. Kunden können uns bitten, die eine oder die andere zu aktivieren, aber nicht beide. Wenn aktiviert:

* Dieses Gerätediagramm verwendet deterministische Daten, die zu dem Unternehmen gehören, das Sie konfigurieren (keine probabilistischen Daten).
* [!DNL Audience Manager] erstellt automatisch eine [!UICONTROL Data Source] mit dem Namen `*`Partnername`*-Company Device Graph-Person`. Auf der Seite &quot;[!UICONTROL Data Source]&quot; können [!DNL Audience Manager] Kunden den Partnernamen und die Beschreibung ändern und [Datenexportsteuerelemente“ &#x200B;](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=de) diese Datenquelle anwenden.
* [!DNL Audience Manager] Kunden *nicht* wird im [!UICONTROL Device Options] Abschnitt eine neue Einstellung für eine [!UICONTROL Profile Merge Rule] angezeigt.

### LiveRamp-Gerätediagramm (Person oder Haushalt) {#liveramp-device-graph}

Diese Kontrollkästchen werden in der [!DNL Admin UI] aktiviert, wenn ein Partner eine [!UICONTROL Data Source] erstellt und **[!UICONTROL Use as an Authenticated Profile]** und/oder **[!UICONTROL Use as a Device Graph]** auswählt. Die Namen für diese Einstellungen werden vom Drittanbieter für Gerätediagramme bestimmt (z. B. [!DNL LiveRamp], [!DNL TapAd] usw.). Wenn diese Option aktiviert ist, verwendet das Unternehmen, das Sie konfigurieren, Daten, die von diesen Gerätediagrammen bereitgestellt werden.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Für Profilzusammenführungsrichtlinien definierte Optionen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=de)
>* [Einstellungen und Menüoptionen in Data Source](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=de)
