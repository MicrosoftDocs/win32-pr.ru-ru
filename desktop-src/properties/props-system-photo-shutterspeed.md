---
description: Скорость затвора камеры, когда была сделана фотография. Это указывается в единицах ВЕРШИНЕ.
ms.assetid: 7f51b3b9-d701-4e7a-80bd-87c1a60e56f7
title: System. photo. Шуттерспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172ce97bf87e79dd86f83e68c91940748bbc283f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080703"
---
# <a name="systemphotoshutterspeed"></a><span data-ttu-id="be5f8-104">System. photo. Шуттерспид</span><span class="sxs-lookup"><span data-stu-id="be5f8-104">System.Photo.ShutterSpeed</span></span>

<span data-ttu-id="be5f8-105">Скорость затвора камеры, когда была сделана фотография.</span><span class="sxs-lookup"><span data-stu-id="be5f8-105">The shutter speed of the camera when the photo was taken.</span></span> <span data-ttu-id="be5f8-106">Это указывается в единицах ВЕРШИНЕ.</span><span class="sxs-lookup"><span data-stu-id="be5f8-106">This is given in APEX units.</span></span> <span data-ttu-id="be5f8-107">Это свойство вычисляется из [System. photo. шуттерспиднумератор](./props-system-photo-shutterspeednumerator.md) и [System. photo. шуттерспидденоминатор](./props-system-photo-shutterspeeddenominator.md).</span><span class="sxs-lookup"><span data-stu-id="be5f8-107">This property is calculated from [System.Photo.ShutterSpeedNumerator](./props-system-photo-shutterspeednumerator.md) and [System.Photo.ShutterSpeedDenominator](./props-system-photo-shutterspeeddenominator.md).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="be5f8-108">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="be5f8-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="be5f8-109">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be5f8-109">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ShutterSpeed
   shellPKey = PKEY_Photo_ShutterSpeed
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37377
   SearchInfo
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="be5f8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be5f8-110">Remarks</span></span>

<span data-ttu-id="be5f8-111">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="be5f8-111">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="be5f8-112">Чтобы преобразовать это значение в время выдержки, см. спецификацию файла обмена изображениями (EXIF) 2,2 в приложении C.</span><span class="sxs-lookup"><span data-stu-id="be5f8-112">See the Exchangeable Image File (EXIF) 2.2 specification, Annex C, for the conversion of this value to exposure time.</span></span> <span data-ttu-id="be5f8-113">Используйте [System. photo. експосуретиме](./props-system-photo-exposuretime.md) в любых представлениях оболочки вместо [System. photo. шуттерспид]().</span><span class="sxs-lookup"><span data-stu-id="be5f8-113">Use [System.Photo.ExposureTime](./props-system-photo-exposuretime.md) in any Shell views instead of [System.Photo.ShutterSpeed]().</span></span>

## <a name="related-topics"></a><span data-ttu-id="be5f8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="be5f8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be5f8-115">Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2</span><span class="sxs-lookup"><span data-stu-id="be5f8-115">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="be5f8-116">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="be5f8-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="be5f8-117">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="be5f8-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="be5f8-118">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="be5f8-118">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="be5f8-119">typeInfo</span><span class="sxs-lookup"><span data-stu-id="be5f8-119">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="be5f8-120">displayInfo</span><span class="sxs-lookup"><span data-stu-id="be5f8-120">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="be5f8-121">stringFormat</span><span class="sxs-lookup"><span data-stu-id="be5f8-121">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="be5f8-122">булеанформат</span><span class="sxs-lookup"><span data-stu-id="be5f8-122">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="be5f8-123">numberFormat</span><span class="sxs-lookup"><span data-stu-id="be5f8-123">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="be5f8-124">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="be5f8-124">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="be5f8-125">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="be5f8-125">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="be5f8-126">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="be5f8-126">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="be5f8-127">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="be5f8-127">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="be5f8-128">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="be5f8-128">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="be5f8-129">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="be5f8-129">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
