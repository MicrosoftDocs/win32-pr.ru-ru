---
title: расширенную защиту
description: Расширенная защита — это механизм для привязки внешнего безопасного канала, такого как SSL к протоколам проверки подлинности внутреннего канала, таким как Kerberos-АПРЕК и проверка подлинности заголовка HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Встроенная поддержка расширенной защиты — веб-службы
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e327d929b77108c1b675e6f42a311e4cad6dd9a056e5ac38b6d7e7f4558788c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927545"
---
# <a name="extended-protection"></a>расширенную защиту

Расширенная защита — это механизм для привязки внешнего безопасного канала, такого как SSL к протоколам проверки подлинности внутреннего канала, таким как Kerberos-АПРЕК и проверка подлинности заголовка HTTP.

Понятие расширенной защиты определяется в RFC2743.

Расширенная защита, если она доступна, настраивается на клиенте автоматически, но может потребовать настройки на сервере для сценариев, не заносящихся по умолчанию.

## <a name="supported-configurations"></a>Поддерживаемые конфигурации

расширенная защита поддерживается при использовании [**\_ \_ \_ привязки канала WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) с привязками безопасности с помощью Windows встроенных протоколов проверки подлинности, таких как [**\_ \_ \_ \_ \_ привязка безопасности HTTP-заголовка**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) authentication и [**\_ \_ \_ \_ \_ привязка безопасности сообщений ws KERBEROS апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding). Он настраивается с помощью следующих [**свойств безопасности**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property):

-   [**\_ \_ \_ Расширенная \_ Политика защиты в свойстве WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ \_ сценарий расширенной \_ защиты свойства WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ \_ удостоверения службы свойств безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Возможны следующие конфигурации, включающие расширенную защиту:

Клиент

-   [**Служба WS \_ \_ \_ \_ Привязка безопасности транспорта SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) используется с привязкой безопасности [**\_ сообщений WS Kerberos \_ апрек \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) или [**с \_ \_ \_ \_ защитой \_ аутентификации HTTP-заголовка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). В этой конфигурации привязка проверки подлинности привязана к SSL-соединению через маркер расширенной защиты, который автоматически извлекается из SSL-соединения.
-   SSL не используется, и задается [**\_ \_ \_ \_ \_ Привязка безопасности HTTP-заголовка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . Привязка проверки подлинности привязана через имя участника на сервере (SPN), которое аутонатикалли определено [**по \_ \_ адресу конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Сервер

-   [**Служба WS \_ \_ \_ \_ Привязка безопасности транспорта SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) используется с привязкой безопасности [**\_ сообщений WS Kerberos \_ апрек \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) или [**с \_ \_ \_ \_ защитой \_ аутентификации HTTP-заголовка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). В этой конфигурации привязка проверки подлинности привязана к SSL-соединению через маркер расширенной защиты, который извлекается из SSL-соединения и проверяется автоматически.
-   SSL не используется, и задается [**\_ \_ \_ \_ \_ Привязка безопасности HTTP-заголовка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . Привязка проверки подлинности привязана через имя участника-пользователя (SPN), которое должно быть предоставлено с помощью [**\_ \_ \_ \_ удостоверений службы свойств безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). При получении сообщения имя участника-службы извлекается и проверяется на предмет точного соответствия с указанными именами служб. Не предоставляя имена участников-служб — это эквивалентно настройке [**\_ расширенной \_ \_ политики \_ защиты WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   SSL не используется, указан [**\_ \_ \_ \_ связанный \_ сервер для сценария расширенной защиты WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) и [**используется \_ \_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) . В этой конфигурации не следует задавать [**\_ \_ \_ \_ удостоверения службы свойств безопасности WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) . Проверка имени участника-службы не выполняется помимо того, что выполняется в рамках протокола Kerberos.
-   [**Служба WS \_ Задано \_ \_ \_ Завершение сценария \_ расширенной защиты**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) , и используется привязка безопасности [**сообщений WS \_ Kerberos \_ Апрек \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) или [**\_ \_ \_ \_ \_ привязок безопасности HTTP-заголовка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . [**Служба WS \_ Должны быть заданы \_ \_ \_ удостоверения службы свойств безопасности**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) .

## <a name="supported-platforms"></a>Поддерживаемые платформы

Расширенная защита поддерживается на платформах с поддержкой этой функции в операционной системе. Windows 7 и Windows Server 2008 R2 предоставляют встроенную поддержку. Для других платформ может потребоваться обновление.

Если операционная система сервера не обеспечивает такую поддержку, все сведения о расширенной защите, отправленные клиентом, игнорируются. В результате клиенты, использующие расширенную защиту, могут взаимодействовать с таким сервером, но преимущество безопасности теряется. На клиенте [**\_ \_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) , Объединенная с [**\_ \_ \_ \_ привязкой безопасности транспорта WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) , поддерживает только расширенную защиту в Vista и более поздних версиях.

Примечание. Расширенная защита недоступна, не запрещает использование какой бы то ни было конкретной конфигурации.

## <a name="interoperability"></a>Совместимость

Сервер, настроенный по умолчанию, может взаимодействовать с клиентами SOAP независимо от того, использует ли они расширенную защиту или нет. единственным исключением являются Windows XP и Windows Server 2003 ввсапи, которые были обновлены для поддержки расширенной защиты и используют привязку [**\_ \_ \_ \_ безопасности \_ сообщений ws KERBEROS апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) и [**\_ \_ \_ \_ привязку безопасности транспорта ws SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Для поддержки таких клиентов [**\_ политика расширенной \_ защиты WS \_ \_ не**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) должна быть указана сервером. Серверы, настроенные с помощью **\_ политики расширенной защиты WS, \_ \_ \_ всегда** будут отклонять связь с клиентами, которые не используют расширенную защиту. На клиенте **\_ \_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos апрек** , Объединенная с **\_ \_ \_ \_ привязкой безопасности транспорта WS SSL** , приведет к отправке сообщения с использованием кодирования передачи фрагмента HTTP в Vista и более поздних версиях. Это может вызвать проблемы взаимодействия с серверами, которые не поддерживают поблочную пересылку.

Следующие перечисления/константы являются частью расширенной защиты:

-   [**\_Расширенная \_ Политика защиты WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**\_сценарий расширенной \_ защиты WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Следующие структуры являются частью расширенной защиты:

-   [**\_ \_ удостоверения безопасности службы \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




