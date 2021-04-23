---
description: Определяет, находится ли IP-адрес в определенной подсети.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: Функция Исиннетекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702893"
---
# <a name="isinnetex-function"></a><span data-ttu-id="1dade-103">Функция Исиннетекс</span><span class="sxs-lookup"><span data-stu-id="1dade-103">isInNetEx function</span></span>

<span data-ttu-id="1dade-104">Определяет, находится ли IP-адрес в определенной подсети.</span><span class="sxs-lookup"><span data-stu-id="1dade-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dade-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dade-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dade-106">*IP*</span><span class="sxs-lookup"><span data-stu-id="1dade-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="1dade-107">Строка, содержащая адреса IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="1dade-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="1dade-108">*иппрефикс*</span><span class="sxs-lookup"><span data-stu-id="1dade-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="1dade-109">Строка, содержащая префикс IP с разделителями-двоеточием с старшими n битами, указанными в битовом поле (т. е. 3FFE: 8311: FFFF::/48 или 123.112.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="1dade-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dade-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dade-110">Return value</span></span>

<span data-ttu-id="1dade-111">Значение TRUE, если узел находится в той же подсети; в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="1dade-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="1dade-112">Также возвращает значение FALSE, если префикс имеет неправильный формат или если в сравнении используются адреса и префиксы различных типов (т. е. префикс IPv4 и IPv6-адрес).</span><span class="sxs-lookup"><span data-stu-id="1dade-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="1dade-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="1dade-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="1dade-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dade-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dade-115">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="1dade-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="1dade-116">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="1dade-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



