---
description: Политика метаданных фотографии для свойства System. GPS. долготы.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Политика метаданных фотографии System. GPS. долготы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674275"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="fcd22-103">Политика метаданных фотографии System. GPS. долготы</span><span class="sxs-lookup"><span data-stu-id="fcd22-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="fcd22-104">Политика метаданных фотографии для свойства [System. GPS. долготы](../properties/props-system-gps-longitude.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd22-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fcd22-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="fcd22-105">PKEY</span></span>

<span data-ttu-id="fcd22-106">PKEY \_ GPS \_ Долгота</span><span class="sxs-lookup"><span data-stu-id="fcd22-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="fcd22-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="fcd22-107">Containers</span></span>

<span data-ttu-id="fcd22-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fcd22-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fcd22-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcd22-109">Read-Only</span></span>

<span data-ttu-id="fcd22-110">Да</span><span class="sxs-lookup"><span data-stu-id="fcd22-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fcd22-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="fcd22-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fcd22-112">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="fcd22-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fcd22-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="fcd22-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="fcd22-114">Это значение можно записать с помощью записи в System. GPS. Лонгитуденумератор и System. GPS. Лонгитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="fcd22-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="fcd22-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="fcd22-115">It cannot be written directly.</span></span> <span data-ttu-id="fcd22-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="fcd22-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fcd22-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="fcd22-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fcd22-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="fcd22-118">Read Paths</span></span>



| <span data-ttu-id="fcd22-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-119">Order</span></span> | <span data-ttu-id="fcd22-120">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-120">Path</span></span>                     | <span data-ttu-id="fcd22-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="fcd22-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fcd22-122">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-122">1</span></span>     | <span data-ttu-id="fcd22-123">/APP1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="fcd22-124">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-124">2</span></span>     | <span data-ttu-id="fcd22-125">/КСМП/ексиф: Гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="fcd22-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="fcd22-126">Write Paths</span></span>



| <span data-ttu-id="fcd22-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-127">Order</span></span> | <span data-ttu-id="fcd22-128">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-128">Path</span></span>                     | <span data-ttu-id="fcd22-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="fcd22-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="fcd22-130">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-130">1</span></span>     | <span data-ttu-id="fcd22-131">/APP1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="fcd22-132">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-132">2</span></span>     | <span data-ttu-id="fcd22-133">/КСМП/ексиф: Гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fcd22-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="fcd22-134">Remove Paths</span></span>



| <span data-ttu-id="fcd22-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-135">Order</span></span> | <span data-ttu-id="fcd22-136">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="fcd22-137">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-137">1</span></span>     | <span data-ttu-id="fcd22-138">/APP1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="fcd22-139">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-139">2</span></span>     | <span data-ttu-id="fcd22-140">/КСМП/ексиф: гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="fcd22-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="fcd22-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fcd22-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="fcd22-142">Read Paths</span></span>



| <span data-ttu-id="fcd22-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-143">Order</span></span> | <span data-ttu-id="fcd22-144">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-144">Path</span></span>                       | <span data-ttu-id="fcd22-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="fcd22-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="fcd22-146">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-146">1</span></span>     | <span data-ttu-id="fcd22-147">/ИФД/ГПС/{ушорт = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="fcd22-148">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-148">2</span></span>     | <span data-ttu-id="fcd22-149">/ИФД/КСМП/ексиф: Гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="fcd22-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="fcd22-150">Write Paths</span></span>



| <span data-ttu-id="fcd22-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-151">Order</span></span> | <span data-ttu-id="fcd22-152">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-152">Path</span></span>                       | <span data-ttu-id="fcd22-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="fcd22-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="fcd22-154">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-154">1</span></span>     | <span data-ttu-id="fcd22-155">/ИФД/ГПС/{ушорт = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="fcd22-156">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-156">2</span></span>     | <span data-ttu-id="fcd22-157">/ИФД/КСМП/ексиф: Гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="fcd22-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="fcd22-158">Remove Paths</span></span>



| <span data-ttu-id="fcd22-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="fcd22-159">Order</span></span> | <span data-ttu-id="fcd22-160">Путь</span><span class="sxs-lookup"><span data-stu-id="fcd22-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="fcd22-161">1</span><span class="sxs-lookup"><span data-stu-id="fcd22-161">1</span></span>     | <span data-ttu-id="fcd22-162">/ИФД/ГПС/{ушорт = 4}</span><span class="sxs-lookup"><span data-stu-id="fcd22-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="fcd22-163">2</span><span class="sxs-lookup"><span data-stu-id="fcd22-163">2</span></span>     | <span data-ttu-id="fcd22-164">/ИФД/КСМП/ексиф: гпслонгитуде</span><span class="sxs-lookup"><span data-stu-id="fcd22-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fcd22-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcd22-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcd22-166">См. также</span><span class="sxs-lookup"><span data-stu-id="fcd22-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcd22-167">System. GPS. Долгота</span><span class="sxs-lookup"><span data-stu-id="fcd22-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
