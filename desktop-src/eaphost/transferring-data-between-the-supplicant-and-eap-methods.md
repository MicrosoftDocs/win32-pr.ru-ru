---
title: Передача данных между запрашивающим и методами EAP
description: Сведения о передаче данных между запрашивающим и методами EAP. Передача данных между методами выполняется с помощью атрибутов EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7675cac2c7e147804bc4c5ec86304e75063964bdc54cd44519fe535e28783f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085655"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a>Передача данных между запрашивающим и методами EAP

Использование атрибутов EAP позволяет обмениваться данными между отправителей запросов и методами EAP.

## <a name="attribute-consumption"></a>Использование атрибута

[**Еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) использует атрибуты EAP, которые передаются непосредственно в настроенный метод EAP. Аналогичным образом методы EAP могут возвращать код действия, указывающий на то, что атрибуты доступны и должны собираются атрибуты с помощью [**еафостпиржетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).

Дополнительные сведения см. в следующих статьях.

-   [Коды действий запрашивающих сторон EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).
-   [Коды причин однорангового запрашивающего устройства EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).
-   [коды действий методов Authenticator EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).

Отправителей запросов должны игнорировать атрибуты, которые они не распознают или не могут работать с ними. При использовании [**еафостпирсетреспонсеаттрибутес**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) эти игнорируемые атрибуты отправляются обратно в EAPHost и метод EAP.

## <a name="vendor-specific-attributes"></a>Атрибуты, зависящие от поставщика

С помощью атрибута EAP, зависящего от поставщика, методы EAP и отправителей запросов могут участвовать в обмене данными с конкретной целью. Атрибуты, зависящие от поставщика, игнорируются отправителей запросов и методами, которые не поддерживают атрибут, зависящий от поставщика.

Дополнительные сведения см. в следующих статьях.

-   [Атрибуты EAP](about-eap-attributes.md).
-   [**Протокол EAP \_ \_тип атрибута**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка пользовательского интерфейса метода EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Включение групповая политика](enabling-group-policy.md)
</dt> <dt>

[Реализация поддержки NAP In-Band для методов EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Реализация поддержки NAP для методов EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[EAPHost отправителей запросов](eaphost-supplicants.md)
</dt> </dl>

 

 




