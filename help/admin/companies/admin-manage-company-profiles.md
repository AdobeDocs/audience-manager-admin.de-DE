---
description: Verwenden Sie die Seite "Unternehmen"im Audience Manager-Admin-Tool, um ein neues Unternehmen zu erstellen.
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: Erstellen eines Firmenprofils
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 2%

---

# Erstellen eines Firmenprofils {#create-a-company-profile}

Verwenden Sie die Seite &quot;[!UICONTROL Companies]&quot;im Audience Manager-Admin-Tool, um ein neues Unternehmen zu erstellen.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Sie müssen über die Rolle &quot;**[!UICONTROL DEXADMIN]**&quot;verfügen, um neue Unternehmen zu erstellen.

1. Klicken Sie auf **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Füllen Sie die Felder aus:

   * **[!UICONTROL Name]**: (Erforderlich) Geben Sie den Namen des Unternehmens an.
   * **[!UICONTROL Description]**: (Erforderlich) Geben Sie beschreibende Informationen über das Unternehmen an, z. B. die Branche oder den vollständigen Namen.
   * **[!UICONTROL Subdomain]**: (Erforderlich) Geben Sie die Subdomäne des Unternehmens an. Der Text, den Sie eingeben, wird als Subdomäne des Ereignisaufrufs angezeigt. Das kann nicht geändert werden. Es muss sich um eine Zeichenfolge mit [!DNL URL] gültigen Zeichen handeln.

     Wenn Ihr Unternehmen beispielsweise &quot;[!DNL AcmeCorp]&quot; heißt, lautet die Subdomäne &quot;[!DNL acmecorp]&quot;.

     Audience Manager verwendet die Subdomäne für den DCS (0). [!UICONTROL Data Collection Server] Wenn im vorherigen Beispiel die vollständige [!DNL URL] in [!UICONTROL DCS] Ihres Unternehmens [!DNL acmecorp.demdex.net] wäre.

   * **[!UICONTROL Lifecyle]**: Geben Sie die gewünschte Phase für das Unternehmen an:
      * **[!UICONTROL Active]**: Geben Sie an, dass das Unternehmen ein aktiver Audience Manager-Client sein wird. Ein [!UICONTROL Active] -Konto bedeutet einen zahlenden Kunden, nicht nur zur Beratung, sondern für die Audience Manager-SKU.
      * **[!UICONTROL Demo]**: Geben Sie an, dass das Unternehmen nur zu Demozwecken dient. Berichtsdaten werden automatisch gefälscht.
      * **[!UICONTROL Prospect]**: Geben Sie an, dass es sich bei dem Unternehmen um einen potenziellen Audience Manager-Client handelt, z. B. wenn einem Unternehmen eine kostenlose [!DNL POC]-Nummer oder ein Konto für eine Verkaufsdemo zugewiesen wird.
      * **[!UICONTROL Test]**: Geben Sie an, dass das Unternehmen nur zu internen Testzwecken dient.

   * **[!UICONTROL Account Types]**: Geben Sie die vollständigen Kontotypen für dieses Unternehmen an. Kein Kontotyp schließt sich bei anderen Typen gegenseitig aus.
      * **[!UICONTROL Full AAM]**: Geben Sie an, dass das Unternehmen über ein vollständiges Adobe Audience Manager-Konto verfügt und Benutzer Zugriff auf die Anmeldung haben.
      * **[!UICONTROL MMP]**: Geben Sie an, dass das Unternehmen für die Verwendung der [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])-Funktionen aktiviert wurde. Mit dem [!UICONTROL MMP] können Zielgruppen über die Experience Cloud mit einem [!UICONTROL Experience Cloud ID] ([!DNL MCID]) freigegeben werden, der jedem Besucher zugewiesen und dann vom Audience Manager verwendet wird. Wenn Sie diesen Kontotyp auswählen, wird auch [!UICONTROL Experience Cloud ID Service] automatisch ausgewählt.

        Weitere Informationen finden Sie unter [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).

   * **[!UICONTROL Data Source]**: Geben Sie an, dass das Unternehmen ein Drittanbieter von Daten innerhalb von Audience Manager ist.
   * **[!UICONTROL Targeting Partner]**: Geben Sie an, dass das Unternehmen als Targeting-Plattform für Audience Manager-Kunden fungiert.
   * **[!UICONTROL Visitor ID Service]**: Geben Sie an, dass das Unternehmen für die Verwendung des [!UICONTROL Experience Cloud Visitor ID Service] aktiviert wurde.

     Der [!UICONTROL Experience Cloud Visitor ID Service] stellt eine universelle Besucher-ID für alle Experience Cloud-Lösungen bereit. Weitere Informationen finden Sie im Benutzerhandbuch für den [Experience Cloud-Besucher-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**: Geben Sie an, dass das Unternehmen über ein [!UICONTROL Agency] -Konto verfügt.

1. Klicken Sie auf **[!UICONTROL Create]**. Fahren Sie mit den Anweisungen unter [Bearbeiten eines Firmenprofils](../companies/admin-manage-company-profiles.md#edit-company-profile) fort.

   ![Schrittergebnis](assets/add_company.png)

## Bearbeiten von Firmenprofilen {#edit-company-profile}

Bearbeiten Sie das Profil eines Unternehmens, einschließlich Name, Beschreibung, Subdomäne, Lebenszyklus und mehr.

<!-- t_edit_company_profile.xml -->

1. Klicken Sie auf &quot;**[!UICONTROL Companies]**&quot;, suchen Sie das gewünschte Unternehmen und klicken Sie darauf, um dessen Seite &quot;[!UICONTROL Profile]&quot;anzuzeigen.

   Verwenden Sie das Feld [!UICONTROL Search] oder die Paginierungssteuerelemente am unteren Rand der Liste, um das gewünschte Unternehmen zu finden. Sie können jede Spalte in auf- oder absteigender Reihenfolge sortieren, indem Sie auf die Kopfzeile der gewünschten Spalte klicken.

   ![Schrittergebnis](assets/profile_company.png)

1. Bearbeiten Sie die Felder nach Bedarf:

   * **[!UICONTROL Name]**: Bearbeiten Sie den Namen des Unternehmens. Dies ist ein erforderliches Feld.
   * **[!UICONTROL Description]**: Bearbeiten Sie die Beschreibung des Unternehmens. Dies ist ein erforderliches Feld.
   * **[!UICONTROL Subdomain]**: (Erforderlich) Geben Sie die Subdomäne des Unternehmens an. Der Text, den Sie eingeben, wird als Subdomäne des Ereignisaufrufs angezeigt. Das kann nicht geändert werden. Es muss sich um eine Zeichenfolge mit [!DNL URL] gültigen Zeichen handeln.

     Wenn Ihr Unternehmen beispielsweise &quot;[!DNL AcmeCorp]&quot; heißt, lautet die Subdomäne &quot;[!DNL acmecorp]&quot;.

     Audience Manager verwendet die Subdomäne für den DCS (0). [!UICONTROL Data Collection Server] Wenn im vorherigen Beispiel die vollständige [!DNL URL] in [!UICONTROL DCS] Ihres Unternehmens [!DNL acmecorp.demdex.net] wäre.

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Mit dieser ID können Sie Ihr Unternehmen mit der Adobe Experience Cloud verbinden.
   * **[!UICONTROL Lifecyle]**: Geben Sie die gewünschte Phase für das Unternehmen an:
      * **[!UICONTROL Active]**: Geben Sie an, dass das Unternehmen ein aktiver Audience Manager-Client sein wird. Ein aktives Konto bedeutet einen zahlenden Kunden, nicht nur für Beratung, sondern für die Audience Manager-SKU.
      * **[!UICONTROL Demo]**: Geben Sie an, dass das Unternehmen nur zu Demozwecken dient. Berichtsdaten werden automatisch gefälscht.
      * **[!UICONTROL Prospect]**: Geben Sie an, dass es sich bei dem Unternehmen um einen potenziellen Audience Manager-Client handelt, z. B. wenn einem Unternehmen eine kostenlose [!DNL POC]-Nummer oder ein Konto für eine Verkaufsdemo zugewiesen wird.
      * **[!UICONTROL Test]**: Geben Sie an, dass das Unternehmen nur zu internen Testzwecken dient.
   * **[!UICONTROL Account Types]**: Geben Sie die vollständigen Kontotypen für dieses Unternehmen an. Kein Kontotyp schließt sich bei anderen Typen gegenseitig aus.
      * **[!UICONTROL Full AAM]**: Geben Sie an, dass das Unternehmen über ein vollständiges Adobe Audience Manager-Konto verfügt und Benutzer Zugriff auf die Anmeldung haben.
      * **[!UICONTROL MMP]**: Geben Sie an, dass das Unternehmen für die Verwendung der Funktionen des Master-Marketing-Profils ([!UICONTROL MMP]) aktiviert wurde.

        Wenn Sie diesen Kontotyp auswählen, wird auch **[!UICONTROL Visitor ID Service]** automatisch ausgewählt.
Weitere Informationen finden Sie unter [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).

   * **[!UICONTROL Data Source]**: Geben Sie an, dass das Unternehmen ein Drittanbieter von Daten innerhalb von Audience Manager ist.
   * **[!UICONTROL Targeting Partner]**: Geben Sie an, dass das Unternehmen als Targeting-Plattform für Audience Manager-Kunden fungiert.
   * **[!UICONTROL Visitor ID Service]**: Geben Sie an, dass das Unternehmen für die Verwendung des Experience Cloud-Besucher-ID-Diensts aktiviert wurde.

     Der Experience Cloud-Besucher-ID-Dienst stellt eine universale Besucher-ID für alle Experience Cloud-Lösungen bereit. Weitere Informationen finden Sie im Benutzerhandbuch zum [Experience Cloud ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**: Geben Sie an, dass das Unternehmen über ein Agenturkonto verfügen soll.
   * **[!UICONTROL Features]**: Wählen Sie die gewünschten Optionen aus:
      * **[!UICONTROL Password Expiration]**: Legt fest, dass alle Benutzerkennwörter in diesem Unternehmen nach 90 Tagen ablaufen, um die Sicherheit der Audience Manager zu erhöhen.
      * **[!UICONTROL Reporting]**: Aktiviert die Audience Manager-Berichterstellung für dieses Unternehmen.
      * **[!UICONTROL Role Based Access Controls]**: Aktivieren Sie rollenbasierte Zugriffskontrollen für dieses Unternehmen. Mit rollenbasierten Zugriffssteuerungen können Sie Benutzergruppen mit unterschiedlichen Zugriffsberechtigungen erstellen. Einzelanwender innerhalb dieser Gruppen können dann nur auf bestimmte Funktionen in Audience Manager zugreifen.

1. Klicken Sie auf **[!UICONTROL Submit Updates]**.

## Löschen eines Firmenprofils {#delete-company-profile}

Verwenden Sie die Seite &quot;[!UICONTROL Companies]&quot;im Tool &quot;Audience Manager [!UICONTROL Admin]&quot;, um ein bestehendes Unternehmen zu löschen.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Sie müssen über die Rolle &quot;[!UICONTROL DEXADMIN]&quot;verfügen, um vorhandene Unternehmen zu löschen.

1. Um ein vorhandenes Unternehmen zu löschen, klicken Sie auf **[!UICONTROL Companies]**.

   ![Schrittergebnis](assets/companies.png)

1. Klicken Sie in der Spalte **[!UICONTROL Actions]** des gewünschten Unternehmens auf ![](assets/icon_delete.png).
1. Klicken Sie auf **[!UICONTROL OK]** , um den Löschvorgang zu bestätigen.
