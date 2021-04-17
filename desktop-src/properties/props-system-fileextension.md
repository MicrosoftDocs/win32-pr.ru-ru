---
description: Определяет расширение файла элемента на основе файла, включая начальную точку.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656603"
---
# <a name="systemfileextension"></a><span data-ttu-id="b27d6-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="b27d6-103">System.FileExtension</span></span>

<span data-ttu-id="b27d6-104">Определяет расширение файла элемента на основе файла, включая начальную точку.</span><span class="sxs-lookup"><span data-stu-id="b27d6-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="b27d6-105">Это свойство является производным от System. FileName.</span><span class="sxs-lookup"><span data-stu-id="b27d6-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="b27d6-106">Если System. имя_файла либо не имеет расширения файла, либо имеет значение VT \_ Empty, значением этого свойства должно быть VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="b27d6-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="b27d6-107">Чтобы получить тип любого элемента (включая элемент, который не является файлом), используйте System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="b27d6-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b27d6-108">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b27d6-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="b27d6-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b27d6-109">Remarks</span></span>

<span data-ttu-id="b27d6-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="b27d6-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b27d6-111">Если [System. filename](./props-system-filename.md) является VT \_ пустым, это свойство также должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="b27d6-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="b27d6-112">В противном случае это свойство должно быть получено соответствующим образом источником данных из System. имя_файла.</span><span class="sxs-lookup"><span data-stu-id="b27d6-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="b27d6-113">Если System. имя_файла не включает расширение файла, [System. fileExtension]() должно иметь значение VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="b27d6-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="b27d6-114">Чтобы получить тип любого элемента (включая элемент, который не является файлом), используйте [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="b27d6-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="b27d6-115">Примеры свойств пути и расширения файла.</span><span class="sxs-lookup"><span data-stu-id="b27d6-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="b27d6-116">Путь</span><span class="sxs-lookup"><span data-stu-id="b27d6-116">Path</span></span>                               | <span data-ttu-id="b27d6-117">Расширение файла</span><span class="sxs-lookup"><span data-stu-id="b27d6-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="b27d6-118">c: \\ файлы \\ Personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="b27d6-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="b27d6-119">.txt</span><span class="sxs-lookup"><span data-stu-id="b27d6-119">.txt</span></span>           |
| <span data-ttu-id="b27d6-120">\\\\\\Общая папка сервера \\ MyDir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="b27d6-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="b27d6-121">.doc</span><span class="sxs-lookup"><span data-stu-id="b27d6-121">.doc</span></span>           |
| <span data-ttu-id="b27d6-122">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="b27d6-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="b27d6-123">.xls</span><span class="sxs-lookup"><span data-stu-id="b27d6-123">.xls</span></span>           |
| <span data-ttu-id="b27d6-124">\\\\\\Общая \\ папка сервера</span><span class="sxs-lookup"><span data-stu-id="b27d6-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="b27d6-125">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b27d6-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="b27d6-126">в. \\ \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="b27d6-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="b27d6-127">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b27d6-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="b27d6-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="b27d6-128">\[desktop\]</span></span>                        | <span data-ttu-id="b27d6-129">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b27d6-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="b27d6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b27d6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b27d6-131">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="b27d6-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b27d6-132">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="b27d6-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b27d6-133">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="b27d6-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b27d6-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="b27d6-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b27d6-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b27d6-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b27d6-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b27d6-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b27d6-137">булеанформат</span><span class="sxs-lookup"><span data-stu-id="b27d6-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b27d6-138">numberFormat</span><span class="sxs-lookup"><span data-stu-id="b27d6-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b27d6-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b27d6-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b27d6-140">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="b27d6-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b27d6-141">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="b27d6-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b27d6-142">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="b27d6-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b27d6-143">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="b27d6-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b27d6-144">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="b27d6-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
