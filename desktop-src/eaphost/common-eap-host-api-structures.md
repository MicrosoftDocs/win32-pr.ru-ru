---
title: Общие структуры API EAPHost
description: Сведения о распространенных структурах API EAPHost. См. список структур, используемых всеми технологиями EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793939"
---
# <a name="common-eaphost-api-structures"></a>Общие структуры API EAPHost

В следующей таблице перечислены структуры, общие для всех технологий API EAPHost.



| Структура                                                                | Описание                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_атрибут EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Содержит атрибут EAP.                                                                                                                                                                                              |
| [**\_АТРИБУТЫ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Содержит массив атрибутов EAP.                                                                                                                                                                                    |
| [**\_ \_ массив входных \_ полей \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Содержит набор структур [**\_ \_ \_ \_ данных входного поля конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) , которые вместе содержат данные пользовательского поля ввода, полученные в диалоговом окне настройки единого входа EAP. |
| [**\_ \_ данные входного \_ поля \_ конфигурации EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Содержит данные, связанные с одним полем ввода в диалоговом окне настройки единого входа EAP (SSO).                                                                                                              |
| [**\_ошибка EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Содержит данные об ошибке, возникшей во время операции EAPHost.                                                                                                                                                 |
| [**\_сведения о методе EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Содержит определенные данные для метода EAP.                                                                                                                                                                               |
| [**\_сведения о методе EAP \_ \_ ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: содержит определенные данные для метода EAP.                                                                                                                             |
| [**\_ \_ массив сведений о МЕТОДе EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Содержит сведения о методах EAP, установленных на клиентском компьютере.                                                                                                                                                   |
| [**\_массив сведений о методе EAP, \_ \_ \_ пример**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista с пакетом обновления 1 (SP1) или более поздней версии: содержит сведения обо всех методах EAP, установленных на клиентском компьютере.                                                                                                    |
| [**\_тип метода \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Содержит тип, идентификацию и авторские данные для метода EAP.                                                                                                                                                       |
| [**\_тип EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Содержит данные идентификации типа и поставщика для метода EAP.                                                                                                                                                         |
| [**еаппаккет**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Содержит пакет непрозрачных данных, отправленных во время сеанса проверки подлинности EAP.                                                                                                                                             |



 

 

 




