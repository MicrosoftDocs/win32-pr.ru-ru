---
description: Режим измерения, используемый камерой, взятый из данных файла образа (EXIF).
ms.assetid: 9dd031a8-f1fa-4753-a86b-18051c624a00
title: System. photo. Метерингмоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e90fff67abe04486504ecda67684f85cb5ac1a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692976"
---
# <a name="systemphotometeringmode"></a><span data-ttu-id="3b3d2-103">System. photo. Метерингмоде</span><span class="sxs-lookup"><span data-stu-id="3b3d2-103">System.Photo.MeteringMode</span></span>

<span data-ttu-id="3b3d2-104">Режим измерения, используемый камерой, взятый из данных файла образа (EXIF).</span><span class="sxs-lookup"><span data-stu-id="3b3d2-104">The metering mode used by the camera, taken from the Exchangeable Image File (EXIF) information.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="3b3d2-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b3d2-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = PHOTO_METERINGMODE_UNKNOWN
         enum
            name = Average
            value = 1
            text = Average
            defineToken = PHOTO_METERINGMODE_AVERAGE
         enum
            name = Center
            value = 2
            text = Center Weighted Average
            defineToken = PHOTO_METERINGMODE_CENTER
         enum
            name = Spot
            value = 3
            text = Spot
            defineToken = PHOTO_METERINGMODE_SPOT
         enum
            name = MultiSpot
            value = 4
            text = Multi Spot
            defineToken = PHOTO_METERINGMODE_MULTISPOT
         enum
            name = Pattern
            value = 5
            text = Pattern
            defineToken = PHOTO_METERINGMODE_PATTERN
         enum
            name = Partial
            value = 6
            text = Partial
            defineToken = PHOTO_METERINGMODE_PARTIAL
```

## <a name="windows-vista"></a><span data-ttu-id="3b3d2-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b3d2-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.MeteringMode
   shellPKey = PKEY_Photo_MeteringMode
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37383
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Unknown
            defineName = PHOTO_METERINGMODE_UNKNOWN
         enum
            value = 1
            text = Average
            defineName = PHOTO_METERINGMODE_AVERAGE
         enum
            value = 2
            text = Center Weighted Average
            defineName = PHOTO_METERINGMODE_CENTER
         enum
            value = 3
            text = Spot
            defineName = PHOTO_METERINGMODE_SPOT
         enum
            value = 4
            text = Multi Spot
            defineName = PHOTO_METERINGMODE_MULTISPOT
         enum
            value = 5
            text = Pattern
            defineName = PHOTO_METERINGMODE_PATTERN
         enum
            value = 6
            text = Partial
            defineName = PHOTO_METERINGMODE_PARTIAL
```

## <a name="remarks"></a><span data-ttu-id="3b3d2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b3d2-107">Remarks</span></span>

<span data-ttu-id="3b3d2-108">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="3b3d2-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b3d2-109">См. также</span><span class="sxs-lookup"><span data-stu-id="3b3d2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3d2-110">Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2</span><span class="sxs-lookup"><span data-stu-id="3b3d2-110">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="3b3d2-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="3b3d2-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="3b3d2-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="3b3d2-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3b3d2-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3b3d2-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3b3d2-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-117">булеанформат</span><span class="sxs-lookup"><span data-stu-id="3b3d2-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="3b3d2-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3b3d2-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-120">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="3b3d2-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-121">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="3b3d2-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-122">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="3b3d2-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-123">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="3b3d2-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3b3d2-124">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="3b3d2-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
