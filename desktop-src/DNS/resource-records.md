---
title: Записи ресурсов
description: Запись ресурса, обычно называемая записью ресурса, представляет собой элемент "единица информации" в файлах зоны DNS; Записи RR — это основные стандартные блоки сведений об имени узла и IP-адреса, которые используются для разрешения всех запросов DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778335"
---
# <a name="resource-records"></a><span data-ttu-id="76061-103">Записи ресурсов</span><span class="sxs-lookup"><span data-stu-id="76061-103">Resource Records</span></span>

<span data-ttu-id="76061-104">Запись ресурса, обычно называемая записью ресурса, представляет собой элемент "единица информации" в файлах зоны DNS; Записи RR — это основные стандартные блоки сведений об имени узла и IP-адреса, которые используются для разрешения всех запросов DNS.</span><span class="sxs-lookup"><span data-stu-id="76061-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="76061-105">Записи ресурсов существуют как многие типы для предоставления расширенных служб разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="76061-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="76061-106">Различные типы записей ресурсов имеют разные форматы, так как они содержат разные данные.</span><span class="sxs-lookup"><span data-stu-id="76061-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="76061-107">Однако в общем случае многие записи ресурсов совместно используют общий формат, как показано в следующем примере записей об адресах.</span><span class="sxs-lookup"><span data-stu-id="76061-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="76061-108">В следующем вымышленном примере объясняются поля, найденные в записи ресурса A:</span><span class="sxs-lookup"><span data-stu-id="76061-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="76061-109">Первое поле (microsoft.com) обозначает владельца.</span><span class="sxs-lookup"><span data-stu-id="76061-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="76061-110">Второе поле (600) — это параметр срока жизни (TTL) в секундах.</span><span class="sxs-lookup"><span data-stu-id="76061-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="76061-111">Третье поле (в) — это поле класса, представляющее семейство протоколов, которое почти всегда используется для класса Интернета.</span><span class="sxs-lookup"><span data-stu-id="76061-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="76061-112">Четвертым полем (A) является тип ресурса, который представляет запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="76061-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="76061-113">Пятое поле (150.150.150.1) — это данные ресурсов или RDATA.</span><span class="sxs-lookup"><span data-stu-id="76061-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="76061-114">Это поле представляет собой тип переменной, который предоставляет сведения, соответствующие типу ресурса. в данном случае это 32-разрядный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="76061-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="76061-115">В DNS обычно используются следующие типы записей ресурсов:</span><span class="sxs-lookup"><span data-stu-id="76061-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="76061-116">Начальная запись зоны (SOA)</span><span class="sxs-lookup"><span data-stu-id="76061-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="76061-117">Сервер имен (NS)</span><span class="sxs-lookup"><span data-stu-id="76061-117">Name server (NS)</span></span>
-   <span data-ttu-id="76061-118">[*Запись указателя*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="76061-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="76061-119">Адрес (A)</span><span class="sxs-lookup"><span data-stu-id="76061-119">Address (A)</span></span>
-   <span data-ttu-id="76061-120">IPv6-адрес (AAAA)</span><span class="sxs-lookup"><span data-stu-id="76061-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="76061-121">Обмен почтой (MX)</span><span class="sxs-lookup"><span data-stu-id="76061-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="76061-122">[*Каноническое имя*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="76061-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="76061-123">Windows Internet Служба именования (WINS)</span><span class="sxs-lookup"><span data-stu-id="76061-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="76061-124">Обратный просмотр WINS (WINSR)</span><span class="sxs-lookup"><span data-stu-id="76061-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="76061-125">В DNS существует много других типов записей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76061-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="76061-126">Дополнительные сведения см. в [справочнике по поставщику WMI DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="76061-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




