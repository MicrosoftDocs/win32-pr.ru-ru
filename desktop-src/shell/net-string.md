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
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997254"
---
# <a name="net_string"></a><span data-ttu-id="b6d2f-104">\_строка NET</span><span class="sxs-lookup"><span data-stu-id="b6d2f-104">NET\_STRING</span></span>

<span data-ttu-id="b6d2f-105">Представляет типы сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-105">Represent network address types.</span></span> <span data-ttu-id="b6d2f-106">Используйте одну или несколько (как побитовое сочетание) следующих констант, чтобы создать маску сетевого адреса для использования с макросом [**нетаддр \_ сеталловтипе**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-106">Use one or more (as a bitwise combination) of the following constants to create a network address mask to use with the macro [**NetAddr\_SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).</span></span>



| <span data-ttu-id="b6d2f-107">Константа</span><span class="sxs-lookup"><span data-stu-id="b6d2f-107">Constant</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="b6d2f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b6d2f-108">Description</span></span>                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <span data-ttu-id="b6d2f-109"><dt>**\_IPv4- \_ \_ адрес сетевой строки**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-109"><dt>**NET\_STRING\_IPV4\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-110">Строка определяет узел или маршрутизатор IPv4, используя литеральный адрес (порт или префикс запрещен).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-110">The string identifies an IPv4 host/router using literal address (port or prefix not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <span data-ttu-id="b6d2f-111"><dt>**\_Служба NET String \_ IPv4 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-111"><dt>**NET\_STRING\_IPV4\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-112">Строка идентифицирует службу IPv4, используя литеральный адрес (требуется порт; префикс не разрешен).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-112">The string identifies an IPv4 service using literal address (port required; prefix not allowed).</span></span><br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <span data-ttu-id="b6d2f-113"><dt>**\_ \_ \_ Сеть IPv4 сети**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-113"><dt>**NET\_STRING\_IPV4\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-114">Строка определяет сеть IPv4 (требуется префикс; порт не разрешен).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-114">The string identifies an IPv4 network (prefix required; port not allowed).</span></span><br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <span data-ttu-id="b6d2f-115"><dt>**\_ \_ Адрес IPv6 сетевой \_ строки**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-115"><dt>**NET\_STRING\_IPV6\_ADDRESS**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-116">Строка идентифицирует узел или маршрутизатор IPv6, используя литеральный адрес (порт или префикс запрещен; идентификатор области действия разрешен).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-116">The string identifies an IPv6 Host/router using literal address (port or prefix not allowed; scope-id allowed.)</span></span><br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <span data-ttu-id="b6d2f-117"><dt>**NET \_ String \_ IPv6 \_ адрес \_ без \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-117"><dt>**NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="b6d2f-118">Строка определяет узел или маршрутизатор IPv6, используя литеральный адрес, где уже известен контекст интерфейса (порт или префикс запрещен; область видимости не разрешена).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-118">The string identifies an IPv6 Host/router using literal address where the interface context is already known (port or prefix not allowed; scope-id not allowed).</span></span><br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <span data-ttu-id="b6d2f-119"><dt>**\_Служба NET String \_ IPv6 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-119"><dt>**NET\_STRING\_IPV6\_SERVICE**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-120">Строка идентифицирует службу IPv6, используя литеральный адрес (требуется порт; префикс не разрешен; область видимости — допустимый идентификатор).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-120">The string identifies an IPv6 service using literal address (port required; prefix not allowed; scope-id allowed).</span></span><br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <span data-ttu-id="b6d2f-121"><dt>**\_Служба NET \_ String \_ IPv6 \_ без \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-121"><dt>**NET\_STRING\_IPV6\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl> | <span data-ttu-id="b6d2f-122">Строка определяет службу IPv6 с использованием литерального адреса, в котором уже известен контекст интерфейса (требуется порт; префикс не разрешен; Scope-ID не разрешен).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-122">The string identifies an IPv6 service using literal address where the interface context is already known (port required; prefix not allowed; scope-id not allowed).</span></span><br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <span data-ttu-id="b6d2f-123"><dt>**\_ \_ Сеть IPv6 с \_ сетью NET String**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-123"><dt>**NET\_STRING\_IPV6\_NETWORK**</dt></span></span> </dl>                              | <span data-ttu-id="b6d2f-124">Строка определяет сеть IPv6 (требуется префикс; порт или идентификатор области не разрешены).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-124">The string identifies an IPv6 network (prefix required; port or scope-id not allowed).</span></span><br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <span data-ttu-id="b6d2f-125"><dt>**СЕТЕВая \_ строка \_ с именованным \_ адресом**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-125"><dt>**NET\_STRING\_NAMED\_ADDRESS**</dt></span></span> </dl>                           | <span data-ttu-id="b6d2f-126">Строка определяет Интернет-узел, использующий DNS (порт или префикс или идентификатор области действия не разрешены).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-126">The string identifies an Internet Host using the DNS(port or prefix or scope-id not allowed).</span></span><br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <span data-ttu-id="b6d2f-127"><dt>**NET \_ String \_ Name \_ Service**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-127"><dt>**NET\_STRING\_NAMED\_SERVICE**</dt></span></span> </dl>                           | <span data-ttu-id="b6d2f-128">Строка определяет Интернет-службу с помощью DNS (требуется порт; префикс или идентификатор области действия не разрешены).</span><span class="sxs-lookup"><span data-stu-id="b6d2f-128">The string identifies an Internet service using DNS (port required; prefix or scope-id not allowed).</span></span><br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <span data-ttu-id="b6d2f-129"><dt>**СЕТЕВОЙ \_ \_ IP- \_ адрес строки**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-129"><dt>**NET\_STRING\_IP\_ADDRESS**</dt></span></span> </dl>                                    | <span data-ttu-id="b6d2f-130">NET \_ String \_ IPv4 \_ \| -адрес \_ строка NET String \_ IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-130">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <span data-ttu-id="b6d2f-131"><dt>**СЕТЕВОЙ \_ \_ IP- \_ адрес строки \_ без \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-131"><dt>**NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="b6d2f-132">NET \_ String \_ IPv4 \_ адрес \| net \_ строка \_ IPv6 \_ адрес \_ без \_ области.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-132">NET\_STRING\_IPV4\_ADDRESS \| NET\_STRING\_IPV6\_ADDRESS\_NO\_SCOPE.</span></span> <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <span data-ttu-id="b6d2f-133"><dt>**\_Служба сетевой \_ IP-строки \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-133"><dt>**NET\_STRING\_IP\_SERVICE**</dt></span></span> </dl>                                    | <span data-ttu-id="b6d2f-134">NET \_ String \_ IPv4 \_ Служба \| net \_ String \_ IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-134">NET\_STRING\_IPV4\_SERVICE \| NET\_STRING\_IPV6\_SERVICE.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <span data-ttu-id="b6d2f-135"><dt>**Сетевая \_ Служба NET String \_ \_ \_ без \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-135"><dt>**NET\_STRING\_IP\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>       | <span data-ttu-id="b6d2f-136">NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-136">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <span data-ttu-id="b6d2f-137"><dt>**\_ \_ Сетевая IP-строка ( \_ сеть)**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-137"><dt>**NET\_STRING\_IP\_NETWORK**</dt></span></span> </dl>                                    | <span data-ttu-id="b6d2f-138">Сетевая сеть IPv4 сети типа NET \_ String с \_ \_ \| \_ \_ IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-138">NET\_STRING\_IPV4\_NETWORK \| NET\_STRING\_IPV6\_NETWORK.</span></span><br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <span data-ttu-id="b6d2f-139"><dt>**Чистая \_ строка с \_ любым \_ адресом**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-139"><dt>**NET\_STRING\_ANY\_ADDRESS**</dt></span></span> </dl>                                 | <span data-ttu-id="b6d2f-140">\_строка NET String \_ с именем \_ address \| \_ строка \_ IP- \_ адрес.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-140">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <span data-ttu-id="b6d2f-141"><dt>**Чистая \_ строка \_ без \_ адреса \_ в \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-141"><dt>**NET\_STRING\_ANY\_ADDRESS\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="b6d2f-142">NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-142">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <span data-ttu-id="b6d2f-143"><dt>**NET \_ String \_ любая \_ Служба**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-143"><dt>**NET\_STRING\_ANY\_SERVICE**</dt></span></span> </dl>                                 | <span data-ttu-id="b6d2f-144">\_строка NET String \_ с именем \_ Service \| net \_ String \_ IP \_ .</span><span class="sxs-lookup"><span data-stu-id="b6d2f-144">NET\_STRING\_NAMED\_SERVICE \| NET\_STRING\_IP\_SERVICE.</span></span><br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <span data-ttu-id="b6d2f-145"><dt>**NET \_ String \_ любая \_ Служба \_ без \_ области**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-145"><dt>**NET\_STRING\_ANY\_SERVICE\_NO\_SCOPE**</dt></span></span> </dl>    | <span data-ttu-id="b6d2f-146">NET \_ String \_ с именем \_ адрес \| net \_ строка \_ IP- \_ адрес \_ без \_ области.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-146">NET\_STRING\_NAMED\_ADDRESS \| NET\_STRING\_IP\_ADDRESS\_NO\_SCOPE.</span></span><br/>                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="b6d2f-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6d2f-147">Remarks</span></span>

<span data-ttu-id="b6d2f-148">Эти значения определены в Ифлпапи. h.</span><span class="sxs-lookup"><span data-stu-id="b6d2f-148">These values are defined in Iphlpapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d2f-149">Требования</span><span class="sxs-lookup"><span data-stu-id="b6d2f-149">Requirements</span></span>



| <span data-ttu-id="b6d2f-150">Требование</span><span class="sxs-lookup"><span data-stu-id="b6d2f-150">Requirement</span></span> | <span data-ttu-id="b6d2f-151">Значение</span><span class="sxs-lookup"><span data-stu-id="b6d2f-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d2f-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6d2f-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d2f-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6d2f-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6d2f-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6d2f-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d2f-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6d2f-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6d2f-156">Header</span><span class="sxs-lookup"><span data-stu-id="b6d2f-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d2f-157"><dt>Ифлпапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d2f-157"><dt>Iphlpapi.h</dt></span></span> </dl> |



 

 




