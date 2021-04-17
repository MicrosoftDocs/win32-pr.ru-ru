---
description: Определяет, может ли данная строка узла разрешаться в IP-адрес.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: Функция Исресолвабликс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702891"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="7472d-103">Функция Исресолвабликс</span><span class="sxs-lookup"><span data-stu-id="7472d-103">isResolvableEx function</span></span>

<span data-ttu-id="7472d-104">Определяет, может ли данная строка узла разрешаться в IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7472d-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="7472d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7472d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7472d-106">*хост*</span><span class="sxs-lookup"><span data-stu-id="7472d-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="7472d-107">Строка, содержащая узел HTTP, который предоставляется в Финдпроксифорурл.</span><span class="sxs-lookup"><span data-stu-id="7472d-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7472d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7472d-108">Return value</span></span>

<span data-ttu-id="7472d-109">Значение TRUE, если узел разрешается в IPv4-или IPv6-адрес; в противном случае — значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="7472d-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="7472d-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="7472d-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="7472d-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7472d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7472d-112">Определения API вспомогательных функций прокси-сервера с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="7472d-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="7472d-113">Расширения IPv6 для формата файла автоматической настройки Navigator</span><span class="sxs-lookup"><span data-stu-id="7472d-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



