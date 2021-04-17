---
description: При использовании параметра CONTAINS в индексе поиска Windows это число совпадений термина. Если имеется несколько элементов CONTAINS,, то при этом вычисляются минимальное число попаданий, а или — максимальное число попаданий.
ms.assetid: 2f0cddba-7535-451f-9bb5-846c06c426f8
title: System. Search. Хиткаунт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3954d891c1f7c913036449094c27f64cea7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719698"
---
# <a name="systemsearchhitcount"></a><span data-ttu-id="c2694-104">System. Search. Хиткаунт</span><span class="sxs-lookup"><span data-stu-id="c2694-104">System.Search.HitCount</span></span>

<span data-ttu-id="c2694-105">При использовании параметра CONTAINS в индексе поиска Windows это число совпадений термина.</span><span class="sxs-lookup"><span data-stu-id="c2694-105">When using CONTAINS over the Windows Search Index, this is the number of matches of the term.</span></span> <span data-ttu-id="c2694-106">Если имеется несколько элементов CONTAINS,, то при этом вычисляются минимальное число попаданий, а или — максимальное число попаданий.</span><span class="sxs-lookup"><span data-stu-id="c2694-106">If there are multiple CONTAINS, an AND computes the minimal number of hits, and an OR computes the maximal number of hits.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c2694-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2694-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.HitCount
   shellPKey = PKEY_Search_HitCount
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="c2694-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2694-108">Remarks</span></span>

<span data-ttu-id="c2694-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="c2694-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2694-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c2694-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2694-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="c2694-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c2694-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="c2694-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c2694-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="c2694-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c2694-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="c2694-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c2694-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c2694-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c2694-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c2694-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c2694-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="c2694-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c2694-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="c2694-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c2694-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c2694-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c2694-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="c2694-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c2694-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="c2694-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c2694-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="c2694-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c2694-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="c2694-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c2694-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="c2694-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
