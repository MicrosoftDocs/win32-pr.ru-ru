---
description: Значение яркости изображения в единицах ВЕРШИНЕ, обычно в диапазоне от-99,99 до 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System. photo. яркость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131b7e2d51f402aa8da4d5e9b266fe1fc1b39b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711837"
---
# <a name="systemphotobrightness"></a><span data-ttu-id="501dd-103">System. photo. яркость</span><span class="sxs-lookup"><span data-stu-id="501dd-103">System.Photo.Brightness</span></span>

<span data-ttu-id="501dd-104">Значение яркости изображения в единицах ВЕРШИНЕ, обычно в диапазоне от-99,99 до 99,99.</span><span class="sxs-lookup"><span data-stu-id="501dd-104">The brightness value of the image, in APEX units, usually in the range of -99.99 to 99.99.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="501dd-105">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="501dd-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="501dd-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="501dd-106">Remarks</span></span>

<span data-ttu-id="501dd-107">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="501dd-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="501dd-108">Сравнение чисел [System. photo. яркость]() и Foot-Lambertных измерений см. в спецификации EXIF 2,2, приложении C.</span><span class="sxs-lookup"><span data-stu-id="501dd-108">See the EXIF 2.2 specification, Annex C, for a comparison of [System.Photo.Brightness]() numbers and Foot-Lambert measurements.</span></span> <span data-ttu-id="501dd-109">Это свойство вычисляется из [System. photo. бригхтнесснумератор](./props-system-photo-brightnessnumerator.md) и [System. photo. бригхтнессденоминатор](./props-system-photo-brightnessdenominator.md).</span><span class="sxs-lookup"><span data-stu-id="501dd-109">This property is calculated from [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) and [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md).</span></span> <span data-ttu-id="501dd-110">Если числитель записанного значения — FFFFFFFF. H, должно быть указано "Unknown".</span><span class="sxs-lookup"><span data-stu-id="501dd-110">If the numerator of the recorded value is FFFFFFFF.H, "Unknown" should be indicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="501dd-111">См. также</span><span class="sxs-lookup"><span data-stu-id="501dd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="501dd-112">Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2</span><span class="sxs-lookup"><span data-stu-id="501dd-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="501dd-113">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="501dd-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="501dd-114">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="501dd-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="501dd-115">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="501dd-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="501dd-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="501dd-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="501dd-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="501dd-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="501dd-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="501dd-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="501dd-119">булеанформат</span><span class="sxs-lookup"><span data-stu-id="501dd-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="501dd-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="501dd-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="501dd-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="501dd-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="501dd-122">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="501dd-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="501dd-123">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="501dd-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="501dd-124">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="501dd-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="501dd-125">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="501dd-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="501dd-126">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="501dd-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
