---
description: Это свойство аналогично System. Search. Урлтоиндекс, за исключением того, что оно включает время последнего изменения URL-адреса.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. Урлтоиндексвисмодификатионтиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712636"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="51a5a-103">System. Search. Урлтоиндексвисмодификатионтиме</span><span class="sxs-lookup"><span data-stu-id="51a5a-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="51a5a-104">Это свойство аналогично [**System. Search. урлтоиндекс**](props-system-search-urltoindex.md) , за исключением того, что оно включает время последнего изменения URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="51a5a-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="51a5a-105">Это оптимизация индексатора, поэтому ему не нужно обращаться к обработчику протокола, чтобы запросить эти сведения, чтобы определить, нужно ли повторно индексировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="51a5a-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="51a5a-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51a5a-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="51a5a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51a5a-107">Remarks</span></span>

<span data-ttu-id="51a5a-108">Это свойство [System. Search. урлтоиндексвисмодификатионтиме]() совпадает со свойством [System. Search. урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , за исключением того, что вы также передаете время последнего изменения документа.</span><span class="sxs-lookup"><span data-stu-id="51a5a-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="51a5a-109">Если время последнего изменения совпадает, индексатор предполагает, что документ уже проиндексирован и не выдает уведомление.</span><span class="sxs-lookup"><span data-stu-id="51a5a-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="51a5a-110">Это свойство является вектором с двумя элементами — значением **VT \_ LPWSTR** , которое содержит URL-адрес и значение **VT \_ fileTime** , которое содержит время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="51a5a-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="51a5a-111">[System. Search. урлтоиндексвисмодификатионтиме]() назывался PID \_ ГСР \_ дирлинк \_ с \_ временем в более ранних версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="51a5a-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="51a5a-112">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="51a5a-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a5a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="51a5a-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51a5a-114">[System. Search. Урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51a5a-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="51a5a-115">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="51a5a-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="51a5a-116">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="51a5a-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="51a5a-117">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="51a5a-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="51a5a-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="51a5a-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="51a5a-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="51a5a-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="51a5a-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="51a5a-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="51a5a-121">булеанформат</span><span class="sxs-lookup"><span data-stu-id="51a5a-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="51a5a-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="51a5a-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="51a5a-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="51a5a-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="51a5a-124">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="51a5a-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="51a5a-125">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="51a5a-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="51a5a-126">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="51a5a-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="51a5a-127">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="51a5a-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="51a5a-128">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="51a5a-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
