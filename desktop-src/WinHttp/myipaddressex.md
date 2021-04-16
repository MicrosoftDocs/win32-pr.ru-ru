---
description: Находит все IP-адреса для localhost.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: Функция Мипаддрессекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702516"
---
# <a name="myipaddressex-function"></a><span data-ttu-id="a1eb2-103">Функция Мипаддрессекс</span><span class="sxs-lookup"><span data-stu-id="a1eb2-103">myIPAddressEx function</span></span>

<span data-ttu-id="a1eb2-104">Находит все IP-адреса для localhost.</span><span class="sxs-lookup"><span data-stu-id="a1eb2-104">Finds all the IP addresses for localhost.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1eb2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1eb2-105">Parameters</span></span>

<span data-ttu-id="a1eb2-106">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a1eb2-106">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1eb2-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1eb2-107">Return value</span></span>

<span data-ttu-id="a1eb2-108">Строка, разделенная точками с запятой, содержащая все IP-адреса для localhost (IPv6 и/или IPv4), или пустая строка, если не удается разрешить localhost в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a1eb2-108">A semi-colon delimited string containing all IP addresses for localhost (IPv6 and/or IPv4), or an empty string if unable to resolve localhost to an IP address.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1eb2-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1eb2-109">Remarks</span></span>

<span data-ttu-id="a1eb2-110">Разработчики Финдпроксифорурлекс должны добавить код, который разбивает строку IP-адресов, разделенных точками с запятой, на отдельные адреса.</span><span class="sxs-lookup"><span data-stu-id="a1eb2-110">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="a1eb2-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="a1eb2-111">Examples</span></span>

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a><span data-ttu-id="a1eb2-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1eb2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1eb2-113">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="a1eb2-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="a1eb2-114">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="a1eb2-114">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



