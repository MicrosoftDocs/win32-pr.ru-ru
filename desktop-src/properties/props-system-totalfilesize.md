---
description: .
ms.assetid: 10e1f806-e408-48ab-8fe7-1d7a4d41f320
title: System. Тоталфилесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b85ff414a61e4a810045be1c69671835012494
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348695"
---
# <a name="systemtotalfilesize"></a><span data-ttu-id="53bf3-103">System. Тоталфилесизе</span><span class="sxs-lookup"><span data-stu-id="53bf3-103">System.TotalFileSize</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="53bf3-104">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="53bf3-104">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.TotalFileSize
   shellPKey = PKEY_TotalFileSize
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 14
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Empty
            minValue = 0
            setValue = 0
            text = Zero
            defineToken = TOTALFILESIZE_EMPTY
            mnemonics = empty
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 10 KB)
            defineToken = TOTALFILESIZE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 10241
            setValue = 10241
            text = Small (10 - 100 KB)
            defineToken = TOTALFILESIZE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 102401
            setValue = 102401
            text = Medium (100 KB - 1 MB)
            defineToken = TOTALFILESIZE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 1048577
            setValue = 1048577
            text = Large (1 - 16 MB)
            defineToken = TOTALFILESIZE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 16777217
            setValue = 16777217
            text = Huge (16 - 128 MB)
            defineToken = TOTALFILESIZE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 134217729
            setValue = 134217729
            text = Gigantic (>129 MB)
            defineToken = TOTALFILESIZE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a><span data-ttu-id="53bf3-105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53bf3-105">Windows Vista</span></span>

```
propertyDescription
   name = System.TotalFileSize
   shellPKey = PKEY_TotalFileSize
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 14
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Zero
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = Tiny (0 - 10 KB)
            mnemonics = tiny
         enumRange
            minValue = 10241
            setValue = 10241
            text = Small (10 - 100 KB)
            mnemonics = small
         enumRange
            minValue = 102401
            setValue = 102401
            text = Medium (100 KB - 1 MB)
            mnemonics = medium
         enumRange
            minValue = 1048577
            setValue = 1048577
            text = Large (1 - 16 MB)
            mnemonics = large
         enumRange
            minValue = 16777217
            setValue = 16777217
            text = Huge (16 - 128 MB)
            mnemonics = huge
         enumRange
            minValue = 134217729
            setValue = 134217729
            text = Gigantic (>129 MB)
            mnemonics = gigantic
```

## <a name="remarks"></a><span data-ttu-id="53bf3-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53bf3-106">Remarks</span></span>

<span data-ttu-id="53bf3-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="53bf3-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53bf3-108">См. также</span><span class="sxs-lookup"><span data-stu-id="53bf3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53bf3-109">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="53bf3-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="53bf3-110">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="53bf3-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="53bf3-111">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="53bf3-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="53bf3-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="53bf3-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="53bf3-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="53bf3-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="53bf3-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="53bf3-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="53bf3-115">булеанформат</span><span class="sxs-lookup"><span data-stu-id="53bf3-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="53bf3-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="53bf3-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="53bf3-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="53bf3-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="53bf3-118">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="53bf3-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="53bf3-119">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="53bf3-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="53bf3-120">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="53bf3-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="53bf3-121">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="53bf3-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="53bf3-122">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="53bf3-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
