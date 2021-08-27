---
description: Представляет типы сетевых адресов. Используйте одну или несколько (как побитовое сочетание) следующих констант, чтобы создать маску сетевого адреса для использования с макросом Нетаддр \_ сеталловтипе.
title: NET_STRING (Ифлпапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111224"
---
# <a name="net_string"></a>\_строка NET

Представляет типы сетевых адресов. Используйте одну или несколько (как побитовое сочетание) следующих констант, чтобы создать маску сетевого адреса для использования с макросом [**нетаддр \_ сеталловтипе**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Константа                                                                                                                                                                                                                   | Описание                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**\_IPv4- \_ \_ адрес сетевой строки**</dt> </dl>                              | Строка определяет узел или маршрутизатор IPv4, используя литеральный адрес (порт или префикс запрещен).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**\_Служба NET String \_ IPv4 \_**</dt> </dl>                              | Строка идентифицирует службу IPv4, используя литеральный адрес (требуется порт; префикс не разрешен).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**\_ \_ \_ Сеть IPv4 сети**</dt> </dl>                              | Строка определяет сеть IPv4 (требуется префикс; порт не разрешен).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**\_ \_ Адрес IPv6 сетевой \_ строки**</dt> </dl>                              | Строка идентифицирует узел или маршрутизатор IPv6, используя литеральный адрес (порт или префикс запрещен; идентификатор области действия разрешен).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**NET \_ String \_ IPv6 \_ адрес \_ без \_ области**</dt> </dl> | Строка определяет узел или маршрутизатор IPv6, используя литеральный адрес, где уже известен контекст интерфейса (порт или префикс запрещен; область видимости не разрешена).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**\_Служба NET String \_ IPv6 \_**</dt> </dl>                              | Строка идентифицирует службу IPv6, используя литеральный адрес (требуется порт; префикс не разрешен; область видимости — допустимый идентификатор).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**\_Служба NET \_ String \_ IPv6 \_ без \_ области**</dt> </dl> | Строка определяет службу IPv6 с использованием литерального адреса, в котором уже известен контекст интерфейса (требуется порт; префикс не разрешен; Scope-ID не разрешен).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_ \_ Сеть IPv6 с \_ сетью NET String**</dt> </dl>                              | Строка определяет сеть IPv6 (требуется префикс; порт или идентификатор области не разрешены).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**СЕТЕВая \_ строка \_ с именованным \_ адресом**</dt> </dl>                           | Строка определяет Интернет-узел, использующий DNS (порт или префикс или идентификатор области действия не разрешены).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ String \_ Name \_ Service**</dt> </dl>                           | Строка определяет Интернет-службу с помощью DNS (требуется порт; префикс или идентификатор области действия не разрешены).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**СЕТЕВОЙ \_ \_ IP- \_ адрес строки**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ \| -адрес \_ строка NET String \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**СЕТЕВОЙ \_ \_ IP- \_ адрес строки \_ без \_ области**</dt> </dl>       | NET \_ String \_ IPv4 \_ адрес \| net \_ строка \_ IPv6 \_ адрес \_ без \_ области. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**\_Служба сетевой \_ IP-строки \_**</dt> </dl>                                    | NET \_ String \_ IPv4 \_ Служба \| net \_ String \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**Сетевая \_ Служба NET String \_ \_ \_ без \_ области**</dt> </dl>       | NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_ \_ Сетевая IP-строка ( \_ сеть)**</dt> </dl>                                    | Сетевая сеть IPv4 сети типа NET \_ String с \_ \_ \| \_ \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**Чистая \_ строка с \_ любым \_ адресом**</dt> </dl>                                 | \_строка NET String \_ с именем \_ address \| \_ строка \_ IP- \_ адрес.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**Чистая \_ строка \_ без \_ адреса \_ в \_ области**</dt> </dl>    | NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ String \_ любая \_ Служба**</dt> </dl>                                 | \_строка NET String \_ с именем \_ Service \| net \_ String \_ IP \_ .<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ String \_ любая \_ Служба \_ без \_ области**</dt> </dl>    | NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.<br/>                                                                                                 |



## <a name="remarks"></a>Remarks

Эти значения определены в Ифлпапи. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Ифлпапи. h</dt> </dl> |



 

 




