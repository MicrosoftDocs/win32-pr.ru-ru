---
description: Время раскрытия фотографии (в секундах), считанное из данных файла изображения (EXIF).
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: System. photo. Експосуретиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5811a3d375f41883d1db8f392e714b7bbe0dfa8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264235"
---
# <a name="systemphotoexposuretime"></a><span data-ttu-id="1dcb1-103">System. photo. Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="1dcb1-103">System.Photo.ExposureTime</span></span>

<span data-ttu-id="1dcb1-104">Время раскрытия фотографии (в секундах), считанное из данных файла изображения (EXIF).</span><span class="sxs-lookup"><span data-stu-id="1dcb1-104">The exposure time for the photo, in seconds, as read from the Exchangeable Image File (EXIF) information.</span></span> <span data-ttu-id="1dcb1-105">Это свойство вычисляется из [System. photo. експосуретименумератор](./props-system-photo-exposuretimenumerator.md) и [System. photo. експосуретимеденоминатор](./props-system-photo-exposuretimedenominator.md).</span><span class="sxs-lookup"><span data-stu-id="1dcb1-105">This property is calculated from [System.Photo.ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) and [System.Photo.ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md).</span></span>

<span data-ttu-id="1dcb1-106">Ниже приведен список возможных значений, взятых из спецификации EXIF 2,2.</span><span class="sxs-lookup"><span data-stu-id="1dcb1-106">The following is a list of possible values taken from the EXIF 2.2 specification.</span></span>

-   <span data-ttu-id="1dcb1-107">30</span><span class="sxs-lookup"><span data-stu-id="1dcb1-107">30</span></span>
-   <span data-ttu-id="1dcb1-108">15</span><span class="sxs-lookup"><span data-stu-id="1dcb1-108">15</span></span>
-   <span data-ttu-id="1dcb1-109">8</span><span class="sxs-lookup"><span data-stu-id="1dcb1-109">8</span></span>
-   <span data-ttu-id="1dcb1-110">4</span><span class="sxs-lookup"><span data-stu-id="1dcb1-110">4</span></span>
-   <span data-ttu-id="1dcb1-111">2</span><span class="sxs-lookup"><span data-stu-id="1dcb1-111">2</span></span>
-   <span data-ttu-id="1dcb1-112">1</span><span class="sxs-lookup"><span data-stu-id="1dcb1-112">1</span></span>
-   <span data-ttu-id="1dcb1-113">1/2</span><span class="sxs-lookup"><span data-stu-id="1dcb1-113">1/2</span></span>
-   <span data-ttu-id="1dcb1-114">1/4</span><span class="sxs-lookup"><span data-stu-id="1dcb1-114">1/4</span></span>
-   <span data-ttu-id="1dcb1-115">1/8</span><span class="sxs-lookup"><span data-stu-id="1dcb1-115">1/8</span></span>
-   <span data-ttu-id="1dcb1-116">1/15</span><span class="sxs-lookup"><span data-stu-id="1dcb1-116">1/15</span></span>
-   <span data-ttu-id="1dcb1-117">1/30</span><span class="sxs-lookup"><span data-stu-id="1dcb1-117">1/30</span></span>
-   <span data-ttu-id="1dcb1-118">1/60</span><span class="sxs-lookup"><span data-stu-id="1dcb1-118">1/60</span></span>
-   <span data-ttu-id="1dcb1-119">1/125</span><span class="sxs-lookup"><span data-stu-id="1dcb1-119">1/125</span></span>
-   <span data-ttu-id="1dcb1-120">1/250</span><span class="sxs-lookup"><span data-stu-id="1dcb1-120">1/250</span></span>
-   <span data-ttu-id="1dcb1-121">1/500</span><span class="sxs-lookup"><span data-stu-id="1dcb1-121">1/500</span></span>
-   <span data-ttu-id="1dcb1-122">1/1000</span><span class="sxs-lookup"><span data-stu-id="1dcb1-122">1/1000</span></span>
-   <span data-ttu-id="1dcb1-123">1/2000</span><span class="sxs-lookup"><span data-stu-id="1dcb1-123">1/2000</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1dcb1-124">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dcb1-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1dcb1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1dcb1-125">Remarks</span></span>

<span data-ttu-id="1dcb1-126">Значения PKEY определены в списке PKEY. h.</span><span class="sxs-lookup"><span data-stu-id="1dcb1-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dcb1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1dcb1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dcb1-128">Формат файла изображения для обмена по-прежнему для цифровых камер: EXIF версии 2,2</span><span class="sxs-lookup"><span data-stu-id="1dcb1-128">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="1dcb1-129">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="1dcb1-129">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-130">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="1dcb1-130">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-131">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="1dcb1-131">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-132">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1dcb1-132">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-133">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1dcb1-133">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-134">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1dcb1-134">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-135">булеанформат</span><span class="sxs-lookup"><span data-stu-id="1dcb1-135">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-136">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1dcb1-136">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-137">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1dcb1-137">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-138">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="1dcb1-138">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-139">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="1dcb1-139">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-140">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="1dcb1-140">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-141">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="1dcb1-141">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1dcb1-142">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="1dcb1-142">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
