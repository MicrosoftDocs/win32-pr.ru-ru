---
description: Указывает код FOURCC для видеопотока.
ms.assetid: c5054fc6-1273-4491-8fb9-30c4b8fc663f
title: System. Video. FourCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475b1cebc0d19a89c70e0ebae2be4b7673697c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265314"
---
# <a name="systemvideofourcc"></a><span data-ttu-id="f34c5-103">System. Video. FourCC</span><span class="sxs-lookup"><span data-stu-id="f34c5-103">System.Video.FourCC</span></span>

<span data-ttu-id="f34c5-104">Указывает код FOURCC для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="f34c5-104">Specifies the FOURCC code for the video stream.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="f34c5-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f34c5-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FourCC
   shellPKey = PKEY_Video_FourCC
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 44
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
```

## <a name="remarks"></a><span data-ttu-id="f34c5-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f34c5-106">Remarks</span></span>

<span data-ttu-id="f34c5-107">Код FOURCC — это 32-разрядное целое число без знака, которое создается путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="f34c5-107">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="f34c5-108">Например, объект FOURCC для H. 264 Video имеет значение "H264 Single bitrate" или 0x34363248.</span><span class="sxs-lookup"><span data-stu-id="f34c5-108">For example, the FOURCC for H.264 video is 'H264' or 0x34363248.</span></span>

<span data-ttu-id="f34c5-109">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="f34c5-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f34c5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f34c5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f34c5-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="f34c5-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f34c5-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="f34c5-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f34c5-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="f34c5-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f34c5-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f34c5-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f34c5-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f34c5-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f34c5-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f34c5-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f34c5-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="f34c5-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f34c5-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f34c5-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f34c5-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f34c5-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f34c5-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="f34c5-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f34c5-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="f34c5-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f34c5-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="f34c5-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f34c5-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="f34c5-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f34c5-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="f34c5-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
