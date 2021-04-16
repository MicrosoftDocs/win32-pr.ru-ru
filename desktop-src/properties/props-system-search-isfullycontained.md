---
description: Порождено как ИСТИНное всеми дочерними элементами контейнера (например, электронной почтой или сжатым файлом с расширением ZIP), который создает System. Search. Исклоседдиректори как TRUE. Это гарантирует, что дочерние элементы будут включены в индекс поиска.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. Исфулликонтаинед
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546759"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="6a179-104">System. Search. Исфулликонтаинед</span><span class="sxs-lookup"><span data-stu-id="6a179-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="6a179-105">Порождено как **истинное** всеми дочерними элементами контейнера (например, электронной почтой или сжатым файлом с расширением ZIP), который создает [System. Search. исклоседдиректори](./props-system-search-iscloseddirectory.md) как **true**.</span><span class="sxs-lookup"><span data-stu-id="6a179-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="6a179-106">Это гарантирует, что дочерние элементы будут включены в индекс поиска.</span><span class="sxs-lookup"><span data-stu-id="6a179-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6a179-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a179-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="6a179-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a179-108">Remarks</span></span>

<span data-ttu-id="6a179-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="6a179-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6a179-110">Свойство [System. Search. исклоседдиректори](./props-system-search-iscloseddirectory.md) помогает оптимизировать производительность индексатора, позволяя индексатору пропустить перечисление дочерних элементов контейнера.</span><span class="sxs-lookup"><span data-stu-id="6a179-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="6a179-111">Тем не менее эти дочерние элементы помечаются индексатором как не посещенный, поэтому они будут удалены из индекса.</span><span class="sxs-lookup"><span data-stu-id="6a179-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="6a179-112">При выдаче [System. Search. исфулликонтаинед]() как **true** элемент не удаляется из индекса, несмотря на то, что он не был посещен.</span><span class="sxs-lookup"><span data-stu-id="6a179-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a179-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6a179-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a179-114">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="6a179-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6a179-115">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="6a179-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6a179-116">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="6a179-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6a179-117">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6a179-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6a179-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6a179-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6a179-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6a179-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6a179-120">булеанформат</span><span class="sxs-lookup"><span data-stu-id="6a179-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6a179-121">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6a179-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6a179-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6a179-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6a179-123">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="6a179-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6a179-124">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="6a179-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6a179-125">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="6a179-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6a179-126">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="6a179-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6a179-127">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="6a179-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
