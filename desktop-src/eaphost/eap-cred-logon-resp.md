---
title: Подотчетное \_ \_ имя входа EAP \_ (еаптипес. h)
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ . | Подотчетное \_ \_ имя входа EAP \_ (еаптипес. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694026"
---
# <a name="eap_cred_logon_resp"></a>\_ \_ центр регистрации имени для EAP \_

Структура **\_ ОТВ для \_ входа \_ в систему имени EAP** ХРАНИТ учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**\_ \_ центр регистрации имени для EAP \_**
</dt> <dd>

Структура **\_ ОТВ для \_ входа \_ в систему** удостоверений EAP ХРАНИТ учетные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных. Поля ввода в этой структуре будут совпадать с полями ввода, возвращаемыми функцией [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **Протокол EAP \_ При первом запросе учетных данных используется \_ регистрационное имя для входа \_ в систему** , а в запросе на повтор учетных данных используется [**протокол EAP \_ cred \_**](eap-cred-resp.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Структура **\_ ОТВ для \_ входа \_** в службу EAP используется для поддержки единого входа (SSO).

Структура **\_ ОТВ для \_ входа \_ в систему имени EAP** идентична структуре запросов на [**Вход в \_ \_ учетную \_ запись CRED**](eap-cred-logon-req.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Еаптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_ \_ массив входных \_ полей \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**запрос \_ \_ учетного имени EAP \_**](eap-cred-logon-req.md)
</dt> <dt>

[**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





