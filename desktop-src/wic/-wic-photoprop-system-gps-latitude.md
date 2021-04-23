---
description: Политика метаданных фотографии для свойства System. GPS. Широта.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Политика метаданных фотографии System. GPS. Широта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702786"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="62424-103">Политика метаданных фотографии System. GPS. Широта</span><span class="sxs-lookup"><span data-stu-id="62424-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="62424-104">Политика метаданных фотографии для свойства [System. GPS. Широта](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="62424-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="62424-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="62424-105">PKEY</span></span>

<span data-ttu-id="62424-106">PKEY \_ GPS, \_ Широта</span><span class="sxs-lookup"><span data-stu-id="62424-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="62424-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="62424-107">Containers</span></span>

<span data-ttu-id="62424-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="62424-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="62424-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62424-109">Read-Only</span></span>

<span data-ttu-id="62424-110">Да</span><span class="sxs-lookup"><span data-stu-id="62424-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="62424-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="62424-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="62424-112">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="62424-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="62424-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="62424-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="62424-114">Это значение можно записать с помощью записи в System. GPS. Латитуденумератор и System. GPS. Латитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="62424-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="62424-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="62424-115">It cannot be written directly.</span></span> <span data-ttu-id="62424-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="62424-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="62424-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="62424-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="62424-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="62424-118">Read Paths</span></span>



| <span data-ttu-id="62424-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-119">Order</span></span> | <span data-ttu-id="62424-120">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-120">Path</span></span>                     | <span data-ttu-id="62424-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62424-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="62424-122">1</span><span class="sxs-lookup"><span data-stu-id="62424-122">1</span></span>     | <span data-ttu-id="62424-123">/APP1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="62424-124">2</span><span class="sxs-lookup"><span data-stu-id="62424-124">2</span></span>     | <span data-ttu-id="62424-125">/КСМП/ексиф: Гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="62424-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="62424-126">Write Paths</span></span>



| <span data-ttu-id="62424-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-127">Order</span></span> | <span data-ttu-id="62424-128">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-128">Path</span></span>                     | <span data-ttu-id="62424-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62424-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="62424-130">1</span><span class="sxs-lookup"><span data-stu-id="62424-130">1</span></span>     | <span data-ttu-id="62424-131">/APP1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="62424-132">2</span><span class="sxs-lookup"><span data-stu-id="62424-132">2</span></span>     | <span data-ttu-id="62424-133">/КСМП/ексиф: Гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62424-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="62424-134">Remove Paths</span></span>



| <span data-ttu-id="62424-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-135">Order</span></span> | <span data-ttu-id="62424-136">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="62424-137">1</span><span class="sxs-lookup"><span data-stu-id="62424-137">1</span></span>     | <span data-ttu-id="62424-138">/APP1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="62424-139">2</span><span class="sxs-lookup"><span data-stu-id="62424-139">2</span></span>     | <span data-ttu-id="62424-140">/КСМП/ексиф: гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="62424-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="62424-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="62424-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="62424-142">Read Paths</span></span>



| <span data-ttu-id="62424-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-143">Order</span></span> | <span data-ttu-id="62424-144">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-144">Path</span></span>                      | <span data-ttu-id="62424-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62424-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="62424-146">1</span><span class="sxs-lookup"><span data-stu-id="62424-146">1</span></span>     | <span data-ttu-id="62424-147">/ИФД/ГПС/{ушорт = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="62424-148">2</span><span class="sxs-lookup"><span data-stu-id="62424-148">2</span></span>     | <span data-ttu-id="62424-149">/ИФД/КСМП/ексиф: Гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="62424-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="62424-150">Write Paths</span></span>



| <span data-ttu-id="62424-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-151">Order</span></span> | <span data-ttu-id="62424-152">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-152">Path</span></span>                      | <span data-ttu-id="62424-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62424-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="62424-154">1</span><span class="sxs-lookup"><span data-stu-id="62424-154">1</span></span>     | <span data-ttu-id="62424-155">/ИФД/ГПС/{ушорт = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="62424-156">2</span><span class="sxs-lookup"><span data-stu-id="62424-156">2</span></span>     | <span data-ttu-id="62424-157">/ИФД/КСМП/ексиф: Гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62424-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="62424-158">Remove Paths</span></span>



| <span data-ttu-id="62424-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="62424-159">Order</span></span> | <span data-ttu-id="62424-160">Путь</span><span class="sxs-lookup"><span data-stu-id="62424-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="62424-161">1</span><span class="sxs-lookup"><span data-stu-id="62424-161">1</span></span>     | <span data-ttu-id="62424-162">/ИФД/ГПС/{ушорт = 2}</span><span class="sxs-lookup"><span data-stu-id="62424-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="62424-163">2</span><span class="sxs-lookup"><span data-stu-id="62424-163">2</span></span>     | <span data-ttu-id="62424-164">/ИФД/КСМП/ексиф: гпслатитуде</span><span class="sxs-lookup"><span data-stu-id="62424-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="62424-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62424-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="62424-166">См. также</span><span class="sxs-lookup"><span data-stu-id="62424-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62424-167">System. GPS. Широта</span><span class="sxs-lookup"><span data-stu-id="62424-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
