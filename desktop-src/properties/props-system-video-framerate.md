---
description: Указывает частоту кадров для потока видео в кадрах за 1000 секунд.
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System. Video. частота
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265313"
---
# <a name="systemvideoframerate"></a><span data-ttu-id="169c9-103">System. Video. частота</span><span class="sxs-lookup"><span data-stu-id="169c9-103">System.Video.FrameRate</span></span>

<span data-ttu-id="169c9-104">Указывает частоту кадров для потока видео в кадрах за 1000 секунд.</span><span class="sxs-lookup"><span data-stu-id="169c9-104">Indicates the frame rate for the video stream, in frames per 1000 seconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="169c9-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="169c9-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="169c9-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="169c9-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="169c9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="169c9-107">Remarks</span></span>

<span data-ttu-id="169c9-108">Чтобы уменьшить ошибку усечения, это свойство не использует стандартную меру частоты кадров в секунду (кадр/с).</span><span class="sxs-lookup"><span data-stu-id="169c9-108">To help reduce truncation error, this property does not use the standard frame rate measure of frames per second (FPS).</span></span> <span data-ttu-id="169c9-109">Вместо этого свойство измеряет частоту кадров в виде кадров на 1000 секунд (с умножением на 1000).</span><span class="sxs-lookup"><span data-stu-id="169c9-109">Instead, this property measures frame rate as frames per 1000 seconds (FPS multiplied by 1000).</span></span> <span data-ttu-id="169c9-110">Например, значение [System. Video.]() частота кадров будет выражаться в 29,97 кадров в виде целого числа 29970.</span><span class="sxs-lookup"><span data-stu-id="169c9-110">For example, [System.Video.FrameRate]() would express a frame rate of 29.97 FPS as an integer value of 29970.</span></span>

<span data-ttu-id="169c9-111">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="169c9-111">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="169c9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="169c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169c9-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="169c9-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="169c9-114">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="169c9-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="169c9-115">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="169c9-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="169c9-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="169c9-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="169c9-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="169c9-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="169c9-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="169c9-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="169c9-119">булеанформат</span><span class="sxs-lookup"><span data-stu-id="169c9-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="169c9-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="169c9-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="169c9-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="169c9-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="169c9-122">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="169c9-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="169c9-123">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="169c9-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="169c9-124">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="169c9-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="169c9-125">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="169c9-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="169c9-126">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="169c9-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
