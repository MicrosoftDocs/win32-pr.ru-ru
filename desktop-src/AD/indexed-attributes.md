---
title: Индексированные атрибуты (AD DS)
description: Атрибуты могут быть проиндексированы. Индексирование атрибута может повысить производительность запросов для этого атрибута.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Индексированные атрибуты Active Directory
- Атрибуты Active Directory, индексированные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654287"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="cd455-106">Индексированные атрибуты (AD DS)</span><span class="sxs-lookup"><span data-stu-id="cd455-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="cd455-107">Атрибуты могут быть проиндексированы.</span><span class="sxs-lookup"><span data-stu-id="cd455-107">Attributes may be indexed.</span></span> <span data-ttu-id="cd455-108">Индексирование атрибута может повысить производительность запросов для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="cd455-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="cd455-109">Атрибуты индексируются, если атрибут [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) в определении схемы атрибута имеет минимальный значащий бит, равный 1.</span><span class="sxs-lookup"><span data-stu-id="cd455-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="cd455-110">Установка для наименее значимого бита определения схемы атрибута **searchFlags** значение 1 приведет к динамической сборке индекса.</span><span class="sxs-lookup"><span data-stu-id="cd455-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="cd455-111">Установка значения 0 для наименее значимого бита определения схемы атрибута **searchFlags** приведет к удалению индекса атрибута.</span><span class="sxs-lookup"><span data-stu-id="cd455-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="cd455-112">Индекс будет автоматически создан фоновым потоком на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="cd455-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="cd455-113">В идеале индексированные атрибуты должны быть однозначными с строго уникальными значениями, равномерно распределенными по набору экземпляров.</span><span class="sxs-lookup"><span data-stu-id="cd455-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="cd455-114">Чем меньше уникальных значений атрибута, тем менее эффективным будет индекс.</span><span class="sxs-lookup"><span data-stu-id="cd455-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="cd455-115">Многозначные атрибуты также можно индексировать, но стоимость построения индекса для многозначного атрибута больше в плане хранения, обновления и времени поиска.</span><span class="sxs-lookup"><span data-stu-id="cd455-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="cd455-116">Требование уникальности для многозначного свойства такое же, как и для однозначного свойства — чем больше уникальных значений, тем эффективнее индекс.</span><span class="sxs-lookup"><span data-stu-id="cd455-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="cd455-117">Чем больше индексированных атрибутов у класса, тем больше времени потребуется для создания новых экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="cd455-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="cd455-118">Индексы применяются к атрибутам, а не к классам.</span><span class="sxs-lookup"><span data-stu-id="cd455-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="cd455-119">То есть, если атрибут помечен как индексированный, все экземпляры атрибута добавляются в индекс, а не только на экземпляры, являющиеся членами определенного класса.</span><span class="sxs-lookup"><span data-stu-id="cd455-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="cd455-120">Чтобы убедиться, что сервер использует индекс для обработки запроса, установите для следующего параметра реестра на контроллере домена значение 4.</span><span class="sxs-lookup"><span data-stu-id="cd455-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="cd455-121">Затем выполните запрос к этому контроллеру домена и найдите в журнале событий каталога данные о индексах (если таковые имеются), используемых для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="cd455-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="cd455-122">Дополнительные сведения о других битах в свойстве [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) см. в разделе [характеристики атрибутов](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cd455-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 