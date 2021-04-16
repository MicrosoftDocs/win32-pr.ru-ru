---
description: Порождено как ИСТИНное элементом контейнера, чтобы показать, что его дочерние элементы не должны перечисляться индексатором, если элемент контейнера не был изменен с момента последнего сканирования при добавочном сканировании индекса.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. Исклоседдиректори
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719662"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="f98a5-103">System. Search. Исклоседдиректори</span><span class="sxs-lookup"><span data-stu-id="f98a5-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="f98a5-104">Порождено как **истинное** элементом контейнера, чтобы показать, что его дочерние элементы не должны перечисляться индексатором, если элемент контейнера не был изменен с момента последнего сканирования при добавочном сканировании индекса.</span><span class="sxs-lookup"><span data-stu-id="f98a5-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="f98a5-105">Это способствует оптимизации производительности индексатора.</span><span class="sxs-lookup"><span data-stu-id="f98a5-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="f98a5-106">В этих вариантах контейнеров (примерах являются сообщения электронной почты с вложениями или сжатый файл с расширением ZIP), дочерние элементы могли от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="f98a5-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="f98a5-107">Например, если свойство [System. DateModified](./props-system-datemodified.md) содержащегося элемента изменяется, значение System. DateModified контейнера изменяется на Match.</span><span class="sxs-lookup"><span data-stu-id="f98a5-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="f98a5-108">Кроме того, при удалении родительского элемента также удаляются и все дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="f98a5-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="f98a5-109">Таким образом, если контейнер не изменился, индексатор знает, что в нем ничего не изменилось и ему не нужно открывать контейнер для проверки содержимого по отдельности.</span><span class="sxs-lookup"><span data-stu-id="f98a5-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="f98a5-110">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f98a5-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="f98a5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f98a5-111">Remarks</span></span>

<span data-ttu-id="f98a5-112">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="f98a5-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f98a5-113">Если элемент порождает **значение true** для этого свойства, все его дочерние элементы должны порождать свойство [System. Search. исфулликонтаинед](./props-system-search-isfullycontained.md) как **true** , чтобы предотвратить удаление этих элементов из индекса.</span><span class="sxs-lookup"><span data-stu-id="f98a5-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f98a5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f98a5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f98a5-115">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="f98a5-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f98a5-116">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="f98a5-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f98a5-117">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="f98a5-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f98a5-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f98a5-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f98a5-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f98a5-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f98a5-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f98a5-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f98a5-121">булеанформат</span><span class="sxs-lookup"><span data-stu-id="f98a5-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f98a5-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f98a5-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f98a5-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f98a5-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f98a5-124">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="f98a5-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f98a5-125">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="f98a5-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f98a5-126">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="f98a5-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f98a5-127">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="f98a5-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f98a5-128">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="f98a5-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
