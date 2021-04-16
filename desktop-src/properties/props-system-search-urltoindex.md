---
description: Создается контейнером IFilter для каждого дочернего URL-адреса в контейнере. В итоге дочерние элементы обрабатываются индексатором, если они находятся в пределах области.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. Search. Урлтоиндекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712136"
---
# <a name="systemsearchurltoindex"></a><span data-ttu-id="19a9c-104">System. Search. Урлтоиндекс</span><span class="sxs-lookup"><span data-stu-id="19a9c-104">System.Search.UrlToIndex</span></span>

<span data-ttu-id="19a9c-105">Создается контейнером [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для каждого дочернего URL-адреса в контейнере.</span><span class="sxs-lookup"><span data-stu-id="19a9c-105">Emitted by a container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) for each child URL within the container.</span></span> <span data-ttu-id="19a9c-106">В итоге дочерние элементы обрабатываются индексатором, если они находятся в пределах области.</span><span class="sxs-lookup"><span data-stu-id="19a9c-106">The children are eventually crawled by the indexer if they are within scope.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="19a9c-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19a9c-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="19a9c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19a9c-108">Remarks</span></span>

<span data-ttu-id="19a9c-109">Это свойство содержит URL-адрес и порождается обработчиком протокола для каждого дочернего URL-адреса или директой под текущим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="19a9c-109">This property contains a URL and is emitted by a protocol handler for each child URL or directoy under the current URL.</span></span> <span data-ttu-id="19a9c-110">Индексатор обращается к обработчику протокола и запрашивает индексирование этого документа.</span><span class="sxs-lookup"><span data-stu-id="19a9c-110">The indexer calls back into the protocol handler, and asks for that document to be indexed.</span></span> <span data-ttu-id="19a9c-111">[System. Search. урлтоиндекс](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) назывался PID \_ ГСР \_ дирлинк в более ранних версиях операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="19a9c-111">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) was called PID\_GTHR\_DIRLINK in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="19a9c-112">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="19a9c-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19a9c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="19a9c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a9c-114">System. Search. Урлтоиндексвисмодификатионтиме</span><span class="sxs-lookup"><span data-stu-id="19a9c-114">System.Search.UrlToIndexWithModificationTime</span></span>](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[<span data-ttu-id="19a9c-115">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="19a9c-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="19a9c-116">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="19a9c-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="19a9c-117">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="19a9c-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="19a9c-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="19a9c-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="19a9c-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="19a9c-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="19a9c-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="19a9c-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="19a9c-121">булеанформат</span><span class="sxs-lookup"><span data-stu-id="19a9c-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="19a9c-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="19a9c-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="19a9c-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="19a9c-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="19a9c-124">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="19a9c-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="19a9c-125">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="19a9c-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="19a9c-126">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="19a9c-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="19a9c-127">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="19a9c-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="19a9c-128">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="19a9c-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
