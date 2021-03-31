---
title: Реализация поддержки NAP In-Band для методов EAP
description: Можно включить для методов протокола EAP для EAPHost, поддерживающих передачу объектов типа length-value (ТЛВС).
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797112"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Реализация поддержки NAP In-Band для методов EAP

Поддержку [защиты доступа к сети](/windows/desktop/NAP/network-access-protection-start-page) (NAP) для метода EAP можно включить для методов протокола EAP, поддерживающих передачу объектов типа length-value (ТЛВС). Если включена поддержка NAP в аппаратном контроллере, пакеты NAP передаются внутри пакетов методов EAP.

В противоположность этому, если включена поддержка нестандартного NAP, Обмен данными [о состоянии работоспособности](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) NAP выполняется через средства, отличные от внутренних для пакетов методов EAP.

Все ТЛВС относятся к конкретному поставщику.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Реализация поддержки NAP на одноранговых методах EAP

Реализация однорангового метода EAP получает TLV, содержащий TLV запроса [состояния работоспособности](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) от сервера EAP.

Затем реализация однорангового метода EAP передает TLV, содержащий TLV запроса SoH, в EAPHost следующим образом.

-   Реализация однорангового метода EAP возвращает код действия [**еаппирмесодреспонсеактионреспонд**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) в значение EAPHost при возврате из [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost вызывает [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) из реализации однорангового метода EAP. Атрибуты передаются в процесс.
-   Реализация однорангового метода EAP возвращает TLV, содержащий TLV запроса SoH в [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes). Атрибуты принимаются в процессе.

Реализация однорангового метода EAP получает TLV, содержащий TLV SoH из EAPHost, как показано ниже.

-   EAPHost вызывает [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) из реализации однорангового метода EAP. **Еаппирсетреспонсеаттрибутес** содержит TLV, в котором находится TLV состояния работоспособности.
-   Реализация однорангового метода EAP отправляет TLV SoH на сервер EAP.
-   Реализация однорангового метода EAP получает TLV, содержащий TLV ответа SoH от сервера EAP.

Реализация однорангового метода EAP передает TLV, содержащий TLV ответа SoH, в EAPHost следующим образом.

-   Реализация однорангового метода EAP возвращает код действия **еаппирмесодреспонсеактионреспонд** в значение EAPHost при возврате из [**еаппирпроцессрекуестпаккет**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).
-   EAPHost вызывает [**еаппиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) из реализаций однорангового метода EAP. Структура [**\_ атрибутов EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) передается в процессе.
-   Реализация однорангового метода EAP возвращает TLV, содержащий TLV ответа SoH в [**еаппирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).

> [!Note]  
> Элементу **еаптипе** структуры [**\_ атрибута EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) всегда будет присвоено значение **еатеаптлв** , а элемент **pValue** будет указывать на первый байт TLV, содержащего TLV ответа SoH.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Реализация поддержки NAP для методов сервера EAP

Реализация метода сервера EAP конструирует TLV, содержащий TLV запроса SoH. Реализация метода сервера EAP отправляет этот TLV, содержащий TLV запроса SoH, на узел EAP. Реализация метода сервера EAP получает TLV от узла EAP.

Реализация метода сервера EAP передает TLV, содержащий TLV SoH, в EAPHost следующим образом.

-   Реализация метода сервера EAP возвращает **\_ ответ на метод \_ проверки подлинности метода \_ EAP \_** для кода действия, реагирующий на EAPHost при возврате из [**еапмесодаусентикаторрецеивепаккет**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).
-   EAPHost вызывает [**еапмесодаусентикаторжетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) из реализации метода сервера EAP.
-   Реализация метода сервера EAP возвращает TLV, содержащий TLV SoH в [**еапмесодаусентикаторжетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).

Реализация метода сервера EAP получает TLV, содержащий TLV ответа SoH из EAPHost, как показано ниже.

-   EAPHost вызывает [**еапмесодаусентикаторсетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) из реализации метода сервера EAP.
-   TLV, содержащий TLV ответа SoH, возвращается в [ **еапмесодаусентикаторсетаттрибутес**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   Реализация метода сервера EAP отправляет TLV, содержащий TLV ответа SoH.

> [!Note]  
> Элементу **еаптипе** структуры [**\_ атрибута EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) всегда будет присвоено значение **еатеаптлв** , а элемент **pValue** будет указывать на первый байт TLV, содержащего TLV ответа SoH.

 

### <a name="messages"></a>Сообщения

TLV состояния работоспособности EAP используется для инкапсуляции протокола SoH для передачи с помощью метода EAP. Все ТЛВС состояния работоспособности EAP имеют одинаковую структуру, отличающуюся только ИДЕНТИФИКАТОРом сообщения и частью данных сообщения.

Дополнительные сведения см. в статье [уведомление о состоянии работоспособности защиты доступа к сети (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка пользовательского интерфейса метода EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Включение групповая политика](enabling-group-policy.md)
</dt> <dt>

[Реализация поддержки NAP для методов EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Передача данных между запрашивающим и методами EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost отправителей запросов](eaphost-supplicants.md)
</dt> </dl>

 

 