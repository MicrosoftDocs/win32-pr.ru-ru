---
description: Значение апертуры изображения в единицах ВЕРШИНЕ.
ms.assetid: ec8c0271-1e1e-4d37-a09a-f430d0682213
title: System. photo. Апертура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2273425c1974617b7d76657f818c4f1c39cd3aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264241"
---
# <a name="systemphotoaperture"></a><span data-ttu-id="38433-103">System. photo. Апертура</span><span class="sxs-lookup"><span data-stu-id="38433-103">System.Photo.Aperture</span></span>

<span data-ttu-id="38433-104">Значение апертуры изображения в единицах ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="38433-104">The aperture value of the image, in APEX units.</span></span> <span data-ttu-id="38433-105">Сравнение чисел [System. photo. апертуры]() и значений [System. photo. фнумбер](./props-system-photo-fnumber.md) см. в спецификации файла обмена изображениями (EXIF) 2,2, приложении C.</span><span class="sxs-lookup"><span data-stu-id="38433-105">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for a comparison of [System.Photo.Aperture]() numbers and [System.Photo.FNumber](./props-system-photo-fnumber.md) values.</span></span> <span data-ttu-id="38433-106">Это свойство вычисляется из [System. photo. апертуренумератор](./props-system-photo-aperturenumerator.md) и [System. photo. апертуреденоминатор](./props-system-photo-aperturedenominator.md).</span><span class="sxs-lookup"><span data-stu-id="38433-106">This property is calculated from [System.Photo.ApertureNumerator](./props-system-photo-aperturenumerator.md) and [System.Photo.ApertureDenominator](./props-system-photo-aperturedenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="38433-107">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="38433-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="38433-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38433-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Aperture
   shellPKey = PKEY_Photo_Aperture
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37378
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="38433-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38433-109">Remarks</span></span>

<span data-ttu-id="38433-110">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="38433-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38433-111">См. также</span><span class="sxs-lookup"><span data-stu-id="38433-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38433-112">Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2</span><span class="sxs-lookup"><span data-stu-id="38433-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="38433-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="38433-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="38433-114">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="38433-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="38433-115">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="38433-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="38433-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="38433-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="38433-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="38433-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="38433-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="38433-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="38433-119">булеанформат</span><span class="sxs-lookup"><span data-stu-id="38433-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="38433-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="38433-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="38433-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="38433-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="38433-122">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="38433-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="38433-123">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="38433-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="38433-124">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="38433-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="38433-125">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="38433-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="38433-126">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="38433-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
