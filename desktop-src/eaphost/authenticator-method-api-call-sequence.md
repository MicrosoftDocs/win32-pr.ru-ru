---
title: Authenticator Последовательность вызовов API метода
description: Сведения о последовательности вызовов API метода средства проверки подлинности. См. список, демонстрирующий последовательность вызовов, сделанных с помощью EAPHost в методе проверки подлинности EAP.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852294"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator Последовательность вызовов API метода

В этом разделе содержится конкретная последовательность вызовов для API метода средства проверки подлинности. Во время обычного сеанса проверки подлинности EAP EAPHost выполняет ряд вызовов метода EAP, реализующих API-интерфейсы метода проверки подлинности EAPHost.

В следующем списке показана последовательность вызовов, выполненных с помощью EAPHost в методе проверки подлинности EAP.

-   Сначала EAP Authenticator загружает библиотеку DLL метода EAP, используемую для конкретной проверки подлинности на сервере политики сети (NPS) или другом сервере проверки подлинности.
-   Вызывает [**еапаусентикаторжетинфо**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) для метода с заполненной структурой [**\_ типа EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) для получения списка указателей на функции, реализованные в библиотеке DLL. Последующие вызовы функций, выполняемые методами проверки подлинности (Server), предполагаются для реализации в библиотеке DLL.
-   Вызывает [**еапаусентикаторинитиализе**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) , чтобы указать библиотеке методов EAP подготовить по крайней мере один сеанс проверки подлинности с помощью этого метода проверки подлинности.
-   Вызывает [**еапмесодаусентикаторбегинсессион**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) , чтобы установить уникальный сеанс проверки подлинности.
-   Повторяет следующие шаги, пока [**еапмесодаусентикаторрецеивепаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) не указывает, что результат проверки подлинности доступен.
    -   Вызывает [**еапмесодаусентикаторсендпаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) с указателем на пакет запроса для передачи в запрашивающую сторона.
    -   Вызывает [**еапмесодаусентикаторрецеивепаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) , чтобы получить пакет ответа, отправленный с помощью запрашивающей стороны. Эта функция возвращает код **\_ \_ \_ \_ действия ответа метода проверки** подлинности EAP, который указывает на следующее действие, которое средство проверки подлинности должно пройти в сеансе проверки подлинности EAP.
    -   Если код действия [ \_ \_ \_ \_ отвечает на ответ метода проверки подлинности EAP Method](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), он указывает, что метод EAP имеет атрибуты, доступные для проверки подлинности и передачи в одноранговый метод. Authenticator вызывает [**еапмесодаусентикаторжетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) для получения различных атрибутов проверки подлинности eap из метода проверки подлинности eap. После того как средство проверки подлинности обрабатывает атрибуты, он вызывает [**еапмесодаусентикаторсетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) , который предоставляет обновленные атрибуты проверки подлинности EAP для установки в методе EAP Authenticator. Эта функция возвращает код **\_ \_ \_ \_ действия ответа метода проверки подлинности EAP** , который определяет последующее действие.
-   Если код действия является [ \_ \_ \_ \_ результатом ответа метода](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)аутентификации EAP, он указывает, что средство проверки подлинности определило результаты сеанса аутентификации, и эти результаты доступны для EAPHost. Authenticator вызывает [**еапмесодаусентикаторжетресулт**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) и получает результаты сеанса проверки подлинности.
-   За ним следует вызов [**еапмесодаусентикаторендсессион**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) , чтобы завершить сеанс проверки подлинности.
-   Наконец, выполняется вызов [**еапмесодаусентикаторшутдовн**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) для выгрузки библиотеки DLL метода средства проверки подлинности.
-   Выгружает библиотеку методов EAP.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_ \_ действие ответа метода проверки подлинности EAP \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Последовательность вызовов API-интерфейса для запрашивающих сторон](supplicant-api-call-sequence.md)
</dt> <dt>

[Последовательность вызовов API однорангового метода](peer-method-api-call-sequence.md)
</dt> <dt>

[Последовательности вызовов EAPHost](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




