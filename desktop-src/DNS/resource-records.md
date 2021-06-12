---
title: Записи ресурсов
description: Сведения о записях ресурсов. Запись ресурса — это запись блока данных в файлах зоны DNS, которая используется для разрешения всех запросов DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010677"
---
# <a name="resource-records"></a><span data-ttu-id="34f7a-104">Записи ресурсов</span><span class="sxs-lookup"><span data-stu-id="34f7a-104">Resource Records</span></span>

<span data-ttu-id="34f7a-105">Запись ресурса, обычно называемая записью ресурса, представляет собой элемент "единица информации" в файлах зоны DNS; Записи RR — это основные стандартные блоки сведений об имени узла и IP-адреса, которые используются для разрешения всех запросов DNS.</span><span class="sxs-lookup"><span data-stu-id="34f7a-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="34f7a-106">Записи ресурсов существуют как многие типы для предоставления расширенных служб разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="34f7a-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="34f7a-107">Различные типы записей ресурсов имеют разные форматы, так как они содержат разные данные.</span><span class="sxs-lookup"><span data-stu-id="34f7a-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="34f7a-108">Однако в общем случае многие записи ресурсов совместно используют общий формат, как показано в следующем примере записей об адресах.</span><span class="sxs-lookup"><span data-stu-id="34f7a-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="34f7a-109">В следующем вымышленном примере объясняются поля, найденные в записи ресурса A:</span><span class="sxs-lookup"><span data-stu-id="34f7a-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="34f7a-110">Первое поле (microsoft.com) обозначает владельца.</span><span class="sxs-lookup"><span data-stu-id="34f7a-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="34f7a-111">Второе поле (600) — это параметр срока жизни (TTL) в секундах.</span><span class="sxs-lookup"><span data-stu-id="34f7a-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="34f7a-112">Третье поле (в) — это поле класса, представляющее семейство протоколов, которое почти всегда используется для класса Интернета.</span><span class="sxs-lookup"><span data-stu-id="34f7a-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="34f7a-113">Четвертым полем (A) является тип ресурса, который представляет запись ресурса.</span><span class="sxs-lookup"><span data-stu-id="34f7a-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="34f7a-114">Пятое поле (150.150.150.1) — это данные ресурсов или RDATA.</span><span class="sxs-lookup"><span data-stu-id="34f7a-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="34f7a-115">Это поле представляет собой тип переменной, который предоставляет сведения, соответствующие типу ресурса. в данном случае это 32-разрядный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="34f7a-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="34f7a-116">В DNS обычно используются следующие типы записей ресурсов:</span><span class="sxs-lookup"><span data-stu-id="34f7a-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="34f7a-117">Начальная запись зоны (SOA)</span><span class="sxs-lookup"><span data-stu-id="34f7a-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="34f7a-118">Сервер имен (NS)</span><span class="sxs-lookup"><span data-stu-id="34f7a-118">Name server (NS)</span></span>
-   <span data-ttu-id="34f7a-119">[*Запись указателя*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="34f7a-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="34f7a-120">Адрес (A)</span><span class="sxs-lookup"><span data-stu-id="34f7a-120">Address (A)</span></span>
-   <span data-ttu-id="34f7a-121">IPv6-адрес (AAAA)</span><span class="sxs-lookup"><span data-stu-id="34f7a-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="34f7a-122">Обмен почтой (MX)</span><span class="sxs-lookup"><span data-stu-id="34f7a-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="34f7a-123">[*Каноническое имя*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="34f7a-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="34f7a-124">Windows Internet Служба именования (WINS)</span><span class="sxs-lookup"><span data-stu-id="34f7a-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="34f7a-125">Обратный просмотр WINS (WINSR)</span><span class="sxs-lookup"><span data-stu-id="34f7a-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="34f7a-126">В DNS существует много других типов записей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34f7a-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="34f7a-127">Дополнительные сведения см. в [справочнике по поставщику WMI DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="34f7a-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




