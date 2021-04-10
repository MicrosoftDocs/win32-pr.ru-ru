---
title: Реализация механизма LEAP для EAPHost
description: Описывает механизм EAPHost, позволяющий сторонним лицам писать модули LEAP для Windows.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104134742"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Реализация механизма LEAP для EAPHost

В этом разделе описывается механизм EAPHost, позволяющий сторонним лицам писать модули LEAP для Windows. LEAP — это устаревший метод проверки подлинности, созданный компанией Cisco в соответствии с [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Дополнительные сведения о LEAP см. [в статье Cisco LEAP Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>Процесс проверки подлинности EAPHost

Обычный процесс проверки подлинности EAPHost выполняется следующим образом.

-   Средство проверки подлинности отправляет запрос на проверку подлинности однорангового узла. Например, приложение вызывает [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) с конфигурацией EAPHost и данными пользователя.
-   Одноранговый узел отправляет ответный пакет в ответ на допустимый запрос. Например, успешный вызов возвращает обработчик сеанса **EAP \_ \_** .
-   Средство проверки подлинности отправляет дополнительный пакет запроса, а одноранговый узел отвечает с ответом. Например, приложение вызывает [**еафостпиржетсендпаккет**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) для получения пакетов EAP, полученных EAPHost во время сеанса. Каждый пакет обрабатывается вызовом [**еафостпирпроцессрецеиведпаккет**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket).
-   [**Еафостпирпроцессрецеиведпаккет**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) всегда будет возвращать код действия. Затем запрашивающий объект должен вызвать функцию, соответствующую коду действия.
-   Последовательность запросов и ответов продолжится при необходимости. Например, приложение может вызвать [**еафостпиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) для запроса доступных атрибутов EAP, а одноранговый узел будет отвечать на [**еафостпирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) , чтобы вернуть их.
-   После первоначального запроса невозможно отправить новый запрос, пока не будет получен допустимый ответ.
-   Диалог будет продолжен до тех пор, пока не будет выполнена проверка подлинности однорангового узла. в этом случае реализация средства проверки подлинности должна передать сбой EAP. Например, неприемлемые ответы на один или несколько запросов приведут к тому, что средство проверки подлинности передаст код 4 сбой EAP.
-   Кроме того, сеанс проверки подлинности может продолжаться до тех пор, пока средство проверки подлинности не определит, что была выполнена успешная аутентификация. в этом случае средство проверки подлинности должно передать успешное выполнение EAP (код 3
-   Если результат указывает на успешное выполнение или сбой, приложение вызывает [**еафостпирендсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) для завершения сеанса. В случае сбоя можно выполнить повторную проверку подлинности, открыв другой сеанс с EAPHost и указав то же или новое удостоверение.

### <a name="leap-authentication-process"></a>Процесс проверки подлинности LEAP

Процесс проверки подлинности LEAP отличается от обычного процесса проверки подлинности EAPhost следующим образом.

-   Проверка подлинности EAP инициируется сервером (Authenticator). LEAP, напротив, инициируется клиентом (одноранговым).
    -   Поэтому при написании модуля LEAP всегда необходимо убедиться, что пакет запроса на выходящий запрос от однорангового метода и ответ EAP от сервера EAP всегда должны иметь тот же идентификатор пакета, что и пакет EAP Success на сервере.

    <!-- -->

    -   В отличие от них, у всех пакетов запросов и ответов EAPHost, как правило, есть разные идентификаторы.
        > [!Note]  
        > Каждый запрос EAP имеет поле типа для указания того, что запрашивается. Как и в случае с пакетом запроса, каждый пакет ответа EAP содержит поле типа, соответствующее полю типа запроса. Примеры включают в себя запросы на идентификацию и запросы запросов.

         

-   В случае сбоя с EAPHost можно выполнить повторную проверку подлинности, открыв другой сеанс с EAPHost и указав то же удостоверение или новое удостоверение.

### <a name="leap-authenticator-method-implementation"></a>Реализация метода средства проверки подлинности LEAP

При разработке метода проверки подлинности LEAP необходимо убедиться в следующем:

-   Методы проверки подлинности LEAP должны возвращать код действия [**\_ \_ \_ \_ отправки ответа метода проверки**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) подлинности в ответ на первый этап аутентификации (одноранговая проверка подлинности). Затем, когда вызывается [**еапмесодаусентикаторсендпаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) , он должен вернуть допустимый [**ЕАППАККЕТ**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) с кодом EAP [**еапкодесукцесс**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode).
-   Методы проверки подлинности LEAP должны возвращать код действия [**\_ \_ \_ \_ результата ответа метода проверки**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) подлинности EAP, если 1-й этап одноранговой проверки подлинности не выполнен.
-   Методы проверки подлинности LEAP должны возвращать окончательный ответный пакет с кодом действия [**\_ \_ \_ \_ результата ответа метода EAP**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) при вызове [**еапмесодаусентикаторсендпаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) . Затем в последующих вызовах [**еапмесодаусентикаторжетресулт**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) для обнаружения сеанса с проверкой подлинности должен возвращаться **\_ \_ обработчик сеанса EAP** .
-   

### <a name="leap-peer-method-implementation"></a>Реализация однорангового метода LEAP

При разработке метода LEAP убедитесь в следующем.

-   Методы однорангового узла LEAP должны возвращать код действия [**еаппирмесодреспонсеактионсенд**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) после успешного завершения первого этапа проверки подлинности (одноранговая проверка подлинности).
-   Методы однорангового узла LEAP должны возвращать код действия [**еаппирмесодреспонсеактионресулт**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) после успешного выполнения второго этапа проверки подлинности.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Последовательность вызовов EAPHost](about-eaphost-call-sequences.md)
</dt> <dt>

[Использование EAPHost](using-eap-host.md)
</dt> </dl>

 

 




