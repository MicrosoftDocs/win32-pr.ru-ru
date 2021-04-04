---
description: Путь к пространству имен оболочки для элемента.
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. Парсингпас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909235"
---
# <a name="systemparsingpath"></a><span data-ttu-id="388df-103">System. Парсингпас</span><span class="sxs-lookup"><span data-stu-id="388df-103">System.ParsingPath</span></span>

<span data-ttu-id="388df-104">Путь к пространству имен оболочки для элемента.</span><span class="sxs-lookup"><span data-stu-id="388df-104">The Shell namespace path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="388df-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="388df-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="388df-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="388df-106">Remarks</span></span>

<span data-ttu-id="388df-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="388df-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="388df-108">Это значение можно передать в [**шпарседисплайнаме**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) , чтобы разобрать путь к правильной папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="388df-108">This value can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="388df-109">Если элемент является файлом, значение идентично значению [System. итемпасдисплай](./props-system-itempathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="388df-109">If the item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).</span></span> <span data-ttu-id="388df-110">Если доступ к элементу через пространство имен оболочки невозможен, это значение является VT \_ пустым.</span><span class="sxs-lookup"><span data-stu-id="388df-110">If the item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="388df-111">См. также</span><span class="sxs-lookup"><span data-stu-id="388df-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="388df-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="388df-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="388df-113">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="388df-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="388df-114">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="388df-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="388df-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="388df-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="388df-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="388df-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="388df-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="388df-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="388df-118">булеанформат</span><span class="sxs-lookup"><span data-stu-id="388df-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="388df-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="388df-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="388df-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="388df-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="388df-121">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="388df-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="388df-122">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="388df-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="388df-123">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="388df-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="388df-124">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="388df-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="388df-125">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="388df-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
