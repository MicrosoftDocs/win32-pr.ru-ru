---
description: Сортирует список IP-адресов.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: Функция Сортипаддресслист
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710863"
---
# <a name="sortipaddresslist-function"></a><span data-ttu-id="5e6ee-103">Функция Сортипаддресслист</span><span class="sxs-lookup"><span data-stu-id="5e6ee-103">sortIpAddressList function</span></span>

<span data-ttu-id="5e6ee-104">Сортирует список IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="5e6ee-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e6ee-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e6ee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6ee-106">*ипаддресслист*</span><span class="sxs-lookup"><span data-stu-id="5e6ee-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="5e6ee-107">Строка, разделенная точкой с запятой, содержащая IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="5e6ee-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6ee-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e6ee-108">Return value</span></span>

<span data-ttu-id="5e6ee-109">Список упорядоченных IP-адресов, разделенных точкой с запятой, или пустая строка, если не удалось отсортировать список IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="5e6ee-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6ee-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e6ee-110">Remarks</span></span>

<span data-ttu-id="5e6ee-111">Разработчики Финдпроксифорурлекс должны добавить код, который разбивает строку IP-адресов, разделенных точками с запятой, на отдельные адреса.</span><span class="sxs-lookup"><span data-stu-id="5e6ee-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="5e6ee-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="5e6ee-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="5e6ee-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e6ee-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6ee-114">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="5e6ee-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="5e6ee-115">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="5e6ee-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



