---
description: Verwenden Sie die Seite OAuth2-Clients , um eine Liste der OAuth2-Clients in Ihrer Audience Manager-Konfiguration anzuzeigen. Sie können vorhandene Clients bearbeiten oder löschen oder neue Clients erstellen, sofern Ihnen die entsprechenden Benutzerrollen zugewiesen sind.
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2-Clients
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# OAuth2-Clients {#oauth-clients}

Verwenden Sie die Seite &quot;[!UICONTROL OAuth2 Clients]&quot;, um eine Liste der [!UICONTROL OAuth2] Clients in Ihrer [!DNL Audience Manager] -Konfiguration anzuzeigen. Sie können vorhandene Clients bearbeiten oder löschen oder neue Clients erstellen, sofern Ihnen die entsprechenden Benutzerrollen zugewiesen sind.

## Überblick {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Stellen Sie sicher, dass Ihr Kunde die Dokumentation [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) im Benutzerhandbuch für Audience Manager liest.

[!DNL OAuth2] ist ein offener Standard für die Autorisierung, um einen gesicherten delegierten Zugriff auf [!DNL Audience Manager] -Ressourcen im Namen eines Ressourceneigentümers bereitzustellen.

![](assets/oauth.png)

Sie können jede Spalte in auf- oder absteigender Reihenfolge sortieren, indem Sie auf die Kopfzeile der gewünschten Spalte klicken.

Verwenden Sie das Feld [!UICONTROL Search] oder die Paginierungssteuerelemente am unteren Rand der Liste, um den gewünschten Client zu finden.

## Erstellen oder Bearbeiten eines OAuth2-Clients {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Verwenden Sie die Seite &quot;[!UICONTROL OAuth2 Clients]&quot;im Tool &quot;Audience Manager [!UICONTROL Admin]&quot;, um einen neuen [!UICONTROL Oauth2] Client zu erstellen oder einen vorhandenen Client zu bearbeiten.

1. Um einen neuen [!UICONTROL OAuth2] -Client zu erstellen, klicken Sie auf **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Um einen vorhandenen [!UICONTROL OAuth2] -Client zu bearbeiten, klicken Sie in der Spalte **[!UICONTROL Client ID]** auf den gewünschten Client.
1. Geben Sie den gewünschten Namen für diesen [!UICONTROL OAuth2]-Client an. Beachten Sie, dass dies nur ein Name für den Datensatz ist.
1. Geben Sie die E-Mail-Adresse des [!UICONTROL OAuth2]-Clients an. Es gibt eine Grenze von einer E-Mail-Adresse.
1. Wählen Sie aus der Dropdownliste **[!UICONTROL Partner]** den gewünschten Partner aus.
1. Geben Sie im Feld **[!UICONTROL Client ID]** die gewünschte ID an. Dies ist der Wert, der beim Senden von [!DNL API] -Anfragen verwendet wird. Das Präfix wird automatisch ausgefüllt, wenn Sie mit der Eingabe beginnen, nachdem Sie in der Dropdown-Liste im vorherigen Schritt eine &quot;[!UICONTROL Partner]&quot; ausgewählt haben. Das richtige Format ist &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **[!UICONTROL Restrict to Partner Users]** nach Bedarf. Wenn dieses Kontrollkästchen aktiviert ist, muss der Benutzer ein [!DNL Audience Manager] Benutzer sein, der für den ausgewählten Partner aufgelistet ist. Es hat sich bewährt, diese Option zu wählen.
1. Aktivieren bzw. deaktivieren Sie im Abschnitt **[!UICONTROL Scope]** die Kontrollkästchen **[!UICONTROL Read]** und **[!UICONTROL Write]** nach Bedarf.
1. Wählen Sie im Abschnitt **[!UICONTROL Grant Type]** die gewünschten Autorisierungsmöglichkeiten aus. Es wird empfohlen, die Standardeinstellungen der Optionen [!UICONTROL Password] und [!UICONTROL Refresh-token] zu verwenden.

   * **[!UICONTROL Implicit]**: Wenn Sie diese Option auswählen, ist das Feld [!UICONTROL Redirect URI] aktiviert. Der Benutzer erhält nach der Authentifizierung ein automatisches Zugriffstoken und wird sofort an die Umleitung [!DNL URI] gesendet.
   * **[!UICONTROL Authorization Code]**: Wenn Sie diese Option auswählen, ist das Feld [!UICONTROL Redirect URI] aktiviert. Der Benutzer wird nach der Authentifizierung an den Client zurückgegeben und dann an die Umleitung [!DNL URI] gesendet.
   * **[!UICONTROL Password]**: Der Benutzer wird mit einem vom Benutzer eingegebenen Kennwort authentifiziert und nicht mit einem automatischen Validierungsversuch über einen Autorisierungsserver.
   * **[!UICONTROL Refresh_token]**: Wird verwendet, um ein abgelaufenes Zugriffstoken für einen längeren Zeitraum zu aktualisieren.

1. Geben Sie im Feld **[!UICONTROL Redirect URI]** den gewünschten [!DNL URI] an. Diese Option ist nur aktiviert, wenn Sie die Grant-Typen **[!UICONTROL Implicit]** und **[!UICONTROL Authorization_code]** auswählen. Mit dem Feld **[!UICONTROL Redirect URI]** können Sie einen kommagetrennten Wert von akzeptablen [!DNL URI] -Werten angeben. Dies ist der [!DNL URI] , zu dem ein Benutzer eines Clients umgeleitet wird, nachdem er den Client für den Zugriff auf [!DNL API] genehmigt hat.
1. Geben Sie die gewünschte Ablaufzeit (in Sekunden) für den Ablauf des Zugriffs- und Aktualisierungstokens an.

   * **[!UICONTROL Access Token Expiration Time]**: Die Anzahl der Sekunden, nach der ein Zugriffstoken gültig ist. Kann null sein, um den Plattformstandard zu verwenden (12 Stunden). Kann auch -1 sein, um anzugeben, dass das Zugriffstoken nicht abläuft.
   * **[!UICONTROL Refresh Token Expiration Time]**: Die Anzahl der Sekunden, nach der ein Aktualisierungstoken gültig ist. Kann null sein, um den Plattformstandard zu verwenden (30 Tage).

1. Klicken Sie auf **[!UICONTROL Save]**.

Um einen [!UICONTROL OAuth2] -Client zu löschen, klicken Sie auf **[!UICONTROL OAuth2 Clients]** und dann auf ![](assets/icon_delete.png) in der Spalte **[!UICONTROL Actions]** für den gewünschten Client.

>[!MORELIKETHIS]
>
>* [API-Anforderungen und -Empfehlungen](../admin-oauth2/aam-admin-api-requirements.md)
