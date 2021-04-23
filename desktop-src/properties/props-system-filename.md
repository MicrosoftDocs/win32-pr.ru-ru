---
description: Имя файла, включая его расширение.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. имя_файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683314"
---
# <a name="systemfilename"></a><span data-ttu-id="2db28-103">System. имя_файла</span><span class="sxs-lookup"><span data-stu-id="2db28-103">System.FileName</span></span>

<span data-ttu-id="2db28-104">Имя файла, включая его расширение.</span><span class="sxs-lookup"><span data-stu-id="2db28-104">The file name, including its extension.</span></span> <span data-ttu-id="2db28-105">System. FileExtension является производным от этого свойства.</span><span class="sxs-lookup"><span data-stu-id="2db28-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="2db28-106">Возможно, элемент не существует в файловой системе (то есть он может быть не открыт с помощью CreateFile).</span><span class="sxs-lookup"><span data-stu-id="2db28-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="2db28-107">Тем не менее, если элемент представлен в виде файла, а его имя соответствует стандартному синтаксису именования файлов Win32, то источник данных должен выдать это свойство.</span><span class="sxs-lookup"><span data-stu-id="2db28-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="2db28-108">Если элемент не является файлом, источник данных должен порождать это свойство как VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="2db28-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2db28-109">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="2db28-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="2db28-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2db28-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="2db28-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2db28-111">Remarks</span></span>

<span data-ttu-id="2db28-112">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="2db28-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2db28-113">Элемент может не существовать в файловой системе (то есть он может быть не открыт с помощью CreateFile), но если элемент представлен в виде файла из логического датчика, а его имя соответствует стандартному синтаксису именования файлов Win32, то источник данных должен выдать это свойство.</span><span class="sxs-lookup"><span data-stu-id="2db28-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="2db28-114">Если элемент не является файлом, значение этого свойства — VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="2db28-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="2db28-115">См. раздел System. Итемнамедисплай.</span><span class="sxs-lookup"><span data-stu-id="2db28-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="2db28-116">Оно имеет то же значение, что и System. Парсингнаме для элементов, которые предоставляются в папке файлов оболочки.</span><span class="sxs-lookup"><span data-stu-id="2db28-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="2db28-117">В следующей таблице приведены примеры значений свойств Path и filename.</span><span class="sxs-lookup"><span data-stu-id="2db28-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="2db28-118">Путь</span><span class="sxs-lookup"><span data-stu-id="2db28-118">Path</span></span>                               | <span data-ttu-id="2db28-119">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2db28-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="2db28-120">c: \\ файлы \\ Personal \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="2db28-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="2db28-121">hello.txt</span><span class="sxs-lookup"><span data-stu-id="2db28-121">hello.txt</span></span>      |
| <span data-ttu-id="2db28-122">\\\\\\Общая папка сервера \\ MyDir \\news.doc</span><span class="sxs-lookup"><span data-stu-id="2db28-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="2db28-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="2db28-123">news.doc</span></span>       |
| <span data-ttu-id="2db28-124">\\\\\\Общая папка сервера \\numbers.xls</span><span class="sxs-lookup"><span data-stu-id="2db28-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="2db28-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="2db28-125">numbers.xls</span></span>    |
| <span data-ttu-id="2db28-126">в. \\ \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="2db28-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="2db28-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="2db28-127">MyFolder</span></span>       |
| <span data-ttu-id="2db28-128">\[сообщение электронной почты\]</span><span class="sxs-lookup"><span data-stu-id="2db28-128">\[email message\]</span></span>                  | <span data-ttu-id="2db28-129">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="2db28-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="2db28-130">\[песня. WMA на портативном устройстве\]</span><span class="sxs-lookup"><span data-stu-id="2db28-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="2db28-131">песня. WMA</span><span class="sxs-lookup"><span data-stu-id="2db28-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="2db28-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2db28-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db28-133">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="2db28-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2db28-134">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="2db28-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2db28-135">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="2db28-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2db28-136">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2db28-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2db28-137">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2db28-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2db28-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2db28-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2db28-139">булеанформат</span><span class="sxs-lookup"><span data-stu-id="2db28-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2db28-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2db28-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2db28-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2db28-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2db28-142">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="2db28-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2db28-143">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="2db28-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2db28-144">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="2db28-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2db28-145">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="2db28-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2db28-146">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="2db28-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
