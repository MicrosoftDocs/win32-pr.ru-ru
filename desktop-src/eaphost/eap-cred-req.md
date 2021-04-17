---
title: Запрос \_ на \_ выеаптипесий EAP
description: Хранит учетные данные безопасности EAP в \_ \_ структуре массива входных полей конфигурации EAP \_ \_ . | Запрос \_ на \_ выеаптипесий EAP
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694025"
---
# <a name="eap_cred_req"></a>Заявка на для EAP \_ cred \_

В структуре **EAP \_ cred \_ req** хранятся учетные данные безопасности EAP в структуре [**\_ \_ \_ \_ массива входных полей конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**Заявка на для EAP \_ cred \_**
</dt> <dd>

В **структуре \_ EAP CRED \_ req** хранятся как старые, так и новые УЧЕТные данные безопасности EAP, на которые указывает параметр *пбуидата* структуры [**\_ данных интерактивного \_ пользовательского интерфейса \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) , если параметр *двдататипе* [**\_ \_ \_ \_ типа данных интерактивного пользовательского интерфейса EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) указывает тип запроса учетных данных.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для поддержки единого входа (SSO) используется структура **EAP \_ cred \_ req** .

Структура **\_ \_ требования** к назначению EAP идентична структуре [**\_ \_ ОТВ для CRED**](eap-cred-resp.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Еаптипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры запрашивающего сторона EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**подотчетное от EAP \_ cred \_**](eap-cred-resp.md)
</dt> <dt>

[**запрос \_ на \_ истечение срока действия CRED EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**\_отв. \_ истечение срока действия для истечения EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[Единый вход и PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

