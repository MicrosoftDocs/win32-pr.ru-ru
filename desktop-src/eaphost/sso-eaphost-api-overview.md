---
title: Обзор API EAPHost для единого входа
description: Содержит общие сведения о API-интерфейсах EAPHost, поддерживающих единый вход (SSO).
ms.assetid: 3c01d10a-9098-4965-8983-c7f65be31884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c047205946293c2116c1ab3537ad4d9250857d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069955"
---
# <a name="sso-eaphost-api-overview"></a>Обзор API EAPHost для единого входа

В этом разделе содержится обзор интерфейсов API EAPHost, поддерживающих единый вход (SSO). Конкретные сценарии единого входа см. в разделе [сценарии EAPHost для SSO](why-eaphost-sso.md).

## <a name="eaphost-enumerations"></a>Перечисления EAPHost

Следующие перечисления поддерживают единый вход.



| Имя                                                                    | Назначение                                                                                      |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ Тип входного \_ поля \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type)  | Определяет набор возможных типов полей ввода, доступных при запросе учетных данных пользователя.    |
| [**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) | Указывает типы данных интерактивного контекста пользовательского интерфейса, предоставляемые определенным вызовам API-запрашивающих. |



 

## <a name="eaphost-structures"></a>Структуры EAPHost

Следующие структуры данных поддерживают единый вход.



| Имя                                                                     | Назначение                                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ данные входного \_ поля \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Содержит данные, связанные с одним полем ввода.                                                                                                                         |
| [**\_ \_ массив входных \_ полей \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Содержит набор структур [**\_ \_ \_ \_ данных полей ввода конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) , которые вместе содержат данные пользовательского поля ввода, полученные от пользователя. |
| [**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)            | Содержит сведения о конфигурации для интерактивных компонентов пользовательского интерфейса, создаваемых для запрашивающего устройства EAP.                                                                                   |
| [**Заявка на для EAP \_ cred \_**](eap-cred-req.md)                                   | Содержит как старые, так и новые учетные данные EAP для операций изменения учетных данных.                                                                                               |
| [**подотчетное от EAP \_ cred \_**](eap-cred-resp.md)                                 | Содержит как старые, так и новые учетные данные EAP для операций изменения учетных данных.                                                                                               |
| [**запрос \_ на \_ истечение срока действия CRED EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                    | Содержит как старые, так и новые учетные данные EAP для операций с истекающим сроком действия учетных данных.                                                                                                 |
| [**\_отв. \_ истечение срока действия для истечения EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))              | Содержит как старые, так и новые учетные данные EAP для операций с истекающим сроком действия учетных данных.                                                                                                 |



 

## <a name="eaphost-peer-supplicant-apis"></a>Интерфейсы API однорангового узла EAPHost

Следующие функции для работы с запрашивающими сторона поддерживают единый вход.

Функции [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields) и [**еафостпиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) являются эксклюзивными для единого входа.



| Имя                                                                                                             | Назначение                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Порядок вызова |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**еафостпиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields)                     | Получает поля ввода для интерактивных компонентов пользовательского интерфейса, которые будут создаваться на запрашивающем сторона.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)                           | Позволяет пользователю определить, какие учетные данные требуются методам для выполнения проверки подлинности в сценарии единого входа.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 1            |
| [**еафостпиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields) | Преобразует сведения о пользователе в большой двоичный объект пользователя, который может использоваться функциями времени выполнения EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 5            |
| [**еафостпиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)   | Получает большой двоичный объект учетных данных, который можно использовать для запуска проверки подлинности из пользовательского ввода, полученного с помощью единого входа.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 2            |
| [**еафостпирбегинсессион**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)                                                       | Запрашивающий объект использует флаг EAP с флагом **\_ \_ предварительного \_ входа** , чтобы указать, что EAPHost должен обеспечивать единый вход. Если возвращается код действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) , EAPHost вызывает [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields), а затем вызывает [**еафостпиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)<br/> Если код действия [еафостпирреспонсеинвокеуи](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) не возвращается, EAPHost переходит к обычной последовательности вызовов без единого входа. Дополнительные сведения см. в разделе [последовательное обращение к API-интерфейсу](supplicant-api-call-sequence.md).<br/> | 3            |



 

## <a name="eaphost-peer-method-apis"></a>API однорангового метода EAPHost

Единый вход поддерживает следующие одноранговые функции.

Функции [**еаппиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields) и [**еаппиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) являются эксклюзивными для единого входа.



| Имя                                                                                                      | Назначение                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Порядок вызова |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields)                      | Определяет реализацию интерфейса API метода EAP, предоставляющего поля ввода для интерактивных компонентов пользовательского интерфейса, которые должны создаваться на запрашивающем.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | 4            |
| [**еаппиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields)                            | Определяет реализацию функции, зависящей от метода EAP, которая получает поля ввода учетных данных для единого входа EAP для этого метода EAP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 1            |
| [**еаппиркуерюиблобфроминтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields)  | Преобразует сведения о пользователе в большой двоичный объект пользователя, который может использоваться функциями времени выполнения EAPHost.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 5            |
| [**еаппиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields) | Определяет реализацию функции метода EAP, которая получает данные большого двоичного объекта пользователя, предоставляемые интерактивным пользовательским ИНТЕРФЕЙСом SSO, который создается на этом запрашивающем объекте.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2            |
| [**еаппирбегинсессион**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                                                        | Флаг EAP с флагом **\_ \_ предварительного \_ входа** указывает, что EAPHost должен обеспечивать единый вход. В сценарии единого входа, если возвращен код действия **еаппирреспонсеинвокеуи** , EAPHost вызывает [**еаппиркуеринтерактивеуиинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields), а затем вызывает [**еаппиркуерюсерблобфромкредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields)<br/> Если код действия **еаппирреспонсеинвокеуи** не возвращается, EAPHost переходит к обычной последовательности вызовов без единого входа. Дополнительные сведения см. в разделе [последовательность вызовов API однорангового метода](peer-method-api-call-sequence.md).<br/> | 3            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Единый вход и PLAP](understanding-sso-and-plap.md)
</dt> <dt>

[Сценарии для единого входа EAPHost](why-eaphost-sso.md)
</dt> </dl>

 

