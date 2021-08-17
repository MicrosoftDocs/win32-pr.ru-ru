---
title: Структуры запрашивающего сторона EAPHost
description: Сведения о структурах API-ответчика EAPHost, таких как EAP \_ cred \_ req \_ и \_ свойство метода EAP \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904621"
---
# <a name="eaphost-supplicant-structures"></a>Структуры запрашивающего сторона EAPHost

Ниже приведены структуры API для запрашивающей сторона EAPHost.



| Структура                                                                        | Описание                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Заявка на для EAP \_ cred \_**](eap-cred-req.md)                                           | Содержит как старые, так и новые учетные данные EAP для операций изменения учетных данных.                                    |
| [**подотчетное от EAP \_ cred \_**](eap-cred-resp.md)                                         | Содержит как старые, так и новые учетные данные EAP для операций изменения учетных данных.                                    |
| [**запрос \_ на \_ истечение срока действия CRED EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Содержит старые и новые учетные данные EAP для операций истечения срока действия учетных данных.                                     |
| [**\_отв. \_ истечение срока действия для истечения EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Содержит как старые, так и новые учетные данные EAP для операций истечения срока действия учетных данных.                                    |
| [**запрос \_ \_ учетного имени EAP \_**](eap-cred-logon-req.md)                              | Содержит учетные данные EAP для проверки подлинности сети.                                                                 |
| [**\_ \_ центр регистрации имени для EAP \_**](eap-cred-logon-resp.md)                            | Содержит учетные данные EAP для проверки подлинности сети.                                                                 |
| [**\_Интерактивные \_ данные ПОЛЬЗОВАТЕЛЬСКОГО интерфейса EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Содержит сведения о конфигурации для компонентов интерактивного пользовательского интерфейса, создаваемых для запрашивающего устройства EAP.            |
| [**\_свойство метода \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 или более поздней версии: представляет свойство метода.                                                                    |
| [**\_ \_ массив свойств метода \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 или более поздней версии: содержит массив структур свойств метода.                                                 |
| [**\_ \_ значение свойства метода \_ EAP**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 или более поздней версии: содержит значение свойства метода.                                                                |
| [**\_ \_ \_ логическое значение свойства метода \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 или более поздней версии: содержит логическое значение свойства метода типа данных.                                                 |
| [**\_ \_ \_ значение \_ DWORD Свойства метода EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 или более поздней версии: содержит значение свойства метода типа данных DWORD.                                                |
| [**\_ \_ \_ строка значения свойства метода \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 или более поздней версии: содержит строковое значение свойства метода типа данных.                                               |
| [**\_сведения об аутентификации EAPHOST \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Описание текущих сведений о проверке подлинности на разных этапах процесса проверки подлинности EAP.          |
| [**еафостпирмесодресулт**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Содержит результирующие данные, созданные EAPHost во время сеанса проверки подлинности, который затем передается в метод EAP. |
| [**еафостпирнапинфо**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 или более поздней версии: содержит сведения о защите доступа к сети (NAP) на запрашивающем сторона EAP.                   |



 

 

 