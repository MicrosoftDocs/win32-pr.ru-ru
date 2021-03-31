---
title: Запрос \_ \_ учетного имени EAP \_ (еаптипес. h)
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071392"
---
# <a name="eap_cred_logon_req"></a>запрос \_ \_ учетного имени EAP \_

В структуре **EAP \_ cred \_ logon \_ req** ХРАНЯТСЯ учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**запрос \_ \_ учетного имени EAP \_**
</dt> <dd>

В **структуре \_ \_ \_ требования к входу** для удостоверения EAP ХРАНЯТСЯ учетные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ \_ \_ данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных. Поля ввода в этой структуре совпадают с полями ввода, возвращаемыми функцией [**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **Протокол EAP \_ Требование \_ к \_ входу** в учетную запись используется в первоначальном запросе Credential, и запрос на удостоверение [**EAP- \_ cred \_**](eap-cred-req.md) используется в запросе на повтор учетных данных во время проверки подлинности.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для поддержки единого входа (SSO) используется структура **EAP \_ cred \_ logon \_ req** .

Структура запросов на **\_ Вход в \_ учетную \_ запись EAP-CRED** идентична структуре [**\_ \_ \_ ОТВ для входа в систему**](eap-cred-logon-resp.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Еаптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ массив входных \_ полей \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**Заявка на для EAP \_ cred \_**](eap-cred-req.md)
</dt> <dt>

[**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**еафостпиркуерикредентиалинпутфиелдс**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





