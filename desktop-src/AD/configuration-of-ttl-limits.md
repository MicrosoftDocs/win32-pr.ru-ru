---
title: Настройка ограничений TTL
description: Клиент может запросить значение TTL для записи в диапазоне от 1 до 31557600 (то есть от 1 секунды до 1 года).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Настройка ограничений срока жизни AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772731"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="5c376-104">Настройка ограничений TTL</span><span class="sxs-lookup"><span data-stu-id="5c376-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="5c376-105">Клиент может запросить значение TTL для записи в диапазоне от 1 до 31557600 (то есть от 1 секунды до 1 года).</span><span class="sxs-lookup"><span data-stu-id="5c376-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="5c376-106">Этот диапазон значений атрибута будет принудительно применен значениями атрибутов **ранжеловер** и **Ранжеуппер** в определении **attributeSchema** для атрибута **ентриттл** .</span><span class="sxs-lookup"><span data-stu-id="5c376-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="5c376-107">В соответствии с RFC 2589 серверы каталогов не обязаны принимать это значение и могут возвращать клиенту другое значение TTL.</span><span class="sxs-lookup"><span data-stu-id="5c376-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="5c376-108">Клиенты должны иметь возможность использовать это серверное значение в качестве периода обновления клиента (CRP), которое будет определять, как часто клиенту потребуется выполнить операцию обновления для динамической записи.</span><span class="sxs-lookup"><span data-stu-id="5c376-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="5c376-109">Домен Active Directory Services предоставляют администраторам возможность настройки значений по умолчанию и минимального срока жизни для леса.</span><span class="sxs-lookup"><span data-stu-id="5c376-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="5c376-110">Значение TTL по умолчанию будет назначено вновь созданной динамической записи, если срок жизни не указан явно.</span><span class="sxs-lookup"><span data-stu-id="5c376-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="5c376-111">Минимальный срок жизни переопределяет любое значение TTL, указанное ниже заданного минимума.</span><span class="sxs-lookup"><span data-stu-id="5c376-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="5c376-112">Не нужно указывать максимальное значение TTL, так как максимальное значение будет накладывается значением атрибута **ранжеуппер** в объекте **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="5c376-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="5c376-113">Предоставление администраторам возможности настраивать эти значения позволит им задать значения TTL, которые будут принудительно использовать трафик с низким уровнем обновления, или, в другой крайней степени, предоставить актуальный каталог.</span><span class="sxs-lookup"><span data-stu-id="5c376-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="5c376-114">Значения по умолчанию для двух настраиваемых параметров TTL будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5c376-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="5c376-115">Значение TTL по умолчанию = 86400 секунд (1 день)</span><span class="sxs-lookup"><span data-stu-id="5c376-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="5c376-116">Минимальное значение TTL = 900 секунд (15 минут)</span><span class="sxs-lookup"><span data-stu-id="5c376-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="5c376-117">Настраиваемые параметры TTL будут храниться в виде записей AVA (утверждение значения атрибута) в формате "<значение-имя>=</span><span class="sxs-lookup"><span data-stu-id="5c376-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="5c376-118">в атрибуте **MS-DS-Other-Settings** объекта NTDS-Service, заданного следующим DN в разделе конфигурации:</span><span class="sxs-lookup"><span data-stu-id="5c376-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="5c376-119">Точный синтаксис AVA для двух настраиваемых параметров TTL имеет следующий вид, где NNNN выражается в секундах:</span><span class="sxs-lookup"><span data-stu-id="5c376-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="5c376-120">Эти значения могут быть заданы администратором с помощью программы командной строки Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="5c376-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




