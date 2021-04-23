---
description: Представляет URL-адрес правильного формата, указывающий на элемент.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. Итемурл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703071"
---
# <a name="systemitemurl"></a><span data-ttu-id="82b3a-103">System. Итемурл</span><span class="sxs-lookup"><span data-stu-id="82b3a-103">System.ItemUrl</span></span>

<span data-ttu-id="82b3a-104">Представляет URL-адрес правильного формата, указывающий на элемент.</span><span class="sxs-lookup"><span data-stu-id="82b3a-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="82b3a-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82b3a-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="82b3a-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82b3a-106">Remarks</span></span>

<span data-ttu-id="82b3a-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="82b3a-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="82b3a-108">Для ссылки на элементы пространства имен оболочки с помощью интерфейсов API оболочки используйте [System. парсингпас](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="82b3a-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="82b3a-109">Примеры значений</span><span class="sxs-lookup"><span data-stu-id="82b3a-109">Example values:</span></span>



| <span data-ttu-id="82b3a-110">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="82b3a-110">Item type</span></span> | <span data-ttu-id="82b3a-111">Пример</span><span class="sxs-lookup"><span data-stu-id="82b3a-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="82b3a-112">Файл</span><span class="sxs-lookup"><span data-stu-id="82b3a-112">File</span></span>      | <span data-ttu-id="82b3a-113">file:///c:/mydir/bar/hello.txt</span><span class="sxs-lookup"><span data-stu-id="82b3a-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="82b3a-114">Файл</span><span class="sxs-lookup"><span data-stu-id="82b3a-114">File</span></span>      | <span data-ttu-id="82b3a-115">CSC://{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="82b3a-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="82b3a-116">Сообщение</span><span class="sxs-lookup"><span data-stu-id="82b3a-116">Message</span></span>   | <span data-ttu-id="82b3a-117">mapi://...</span><span class="sxs-lookup"><span data-stu-id="82b3a-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="82b3a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="82b3a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82b3a-119">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="82b3a-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="82b3a-120">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="82b3a-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="82b3a-121">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="82b3a-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="82b3a-122">typeInfo</span><span class="sxs-lookup"><span data-stu-id="82b3a-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="82b3a-123">displayInfo</span><span class="sxs-lookup"><span data-stu-id="82b3a-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="82b3a-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="82b3a-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="82b3a-125">булеанформат</span><span class="sxs-lookup"><span data-stu-id="82b3a-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="82b3a-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="82b3a-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="82b3a-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="82b3a-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="82b3a-128">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="82b3a-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="82b3a-129">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="82b3a-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="82b3a-130">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="82b3a-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="82b3a-131">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="82b3a-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="82b3a-132">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="82b3a-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
