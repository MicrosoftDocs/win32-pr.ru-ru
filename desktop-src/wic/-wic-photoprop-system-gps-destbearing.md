---
description: Политика метаданных фотографии для свойства System. GPS. Дестбеаринг.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Политика метаданных фотографии System. GPS. Дестбеаринг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348585"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="e8500-103">Политика метаданных фотографии System. GPS. Дестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="e8500-104">Политика метаданных фотографии для свойства [System. GPS. дестбеаринг](../properties/props-system-gps-destbearing.md) .</span><span class="sxs-lookup"><span data-stu-id="e8500-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e8500-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e8500-105">PKEY</span></span>

<span data-ttu-id="e8500-106">PKEY \_ GPS \_ дестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="e8500-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e8500-107">Containers</span></span>

<span data-ttu-id="e8500-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e8500-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e8500-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8500-109">Read-Only</span></span>

<span data-ttu-id="e8500-110">Да</span><span class="sxs-lookup"><span data-stu-id="e8500-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e8500-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e8500-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e8500-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e8500-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e8500-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e8500-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e8500-114">Это значение можно записать с помощью записи в System. GPS. Дестбеарингнумератор и System. GPS. Дестбеарингденоминатор.</span><span class="sxs-lookup"><span data-stu-id="e8500-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="e8500-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="e8500-115">It cannot be written directly.</span></span> <span data-ttu-id="e8500-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e8500-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e8500-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="e8500-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e8500-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e8500-118">Read Paths</span></span>



| <span data-ttu-id="e8500-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-119">Order</span></span> | <span data-ttu-id="e8500-120">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-120">Path</span></span>                      | <span data-ttu-id="e8500-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e8500-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e8500-122">1</span><span class="sxs-lookup"><span data-stu-id="e8500-122">1</span></span>     | <span data-ttu-id="e8500-123">/APP1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e8500-124">2</span><span class="sxs-lookup"><span data-stu-id="e8500-124">2</span></span>     | <span data-ttu-id="e8500-125">/КСМП/ексиф: Гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="e8500-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e8500-126">Write Paths</span></span>



| <span data-ttu-id="e8500-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-127">Order</span></span> | <span data-ttu-id="e8500-128">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-128">Path</span></span>                      | <span data-ttu-id="e8500-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e8500-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e8500-130">1</span><span class="sxs-lookup"><span data-stu-id="e8500-130">1</span></span>     | <span data-ttu-id="e8500-131">/APP1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e8500-132">2</span><span class="sxs-lookup"><span data-stu-id="e8500-132">2</span></span>     | <span data-ttu-id="e8500-133">/КСМП/ексиф: Гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e8500-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e8500-134">Remove Paths</span></span>



| <span data-ttu-id="e8500-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-135">Order</span></span> | <span data-ttu-id="e8500-136">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-136">Path</span></span>                      | <span data-ttu-id="e8500-137">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e8500-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e8500-138">1</span><span class="sxs-lookup"><span data-stu-id="e8500-138">1</span></span>     | <span data-ttu-id="e8500-139">/APP1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e8500-140">2</span><span class="sxs-lookup"><span data-stu-id="e8500-140">2</span></span>     | <span data-ttu-id="e8500-141">/КСМП/ексиф: гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="e8500-142">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="e8500-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e8500-143">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e8500-143">Read Paths</span></span>



| <span data-ttu-id="e8500-144">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-144">Order</span></span> | <span data-ttu-id="e8500-145">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-145">Path</span></span>                         | <span data-ttu-id="e8500-146">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e8500-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e8500-147">1</span><span class="sxs-lookup"><span data-stu-id="e8500-147">1</span></span>     | <span data-ttu-id="e8500-148">/ИФД/ГПС/{ушорт = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="e8500-149">2</span><span class="sxs-lookup"><span data-stu-id="e8500-149">2</span></span>     | <span data-ttu-id="e8500-150">/ИФД/КСМП/ексиф: Гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e8500-151">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e8500-151">Write Paths</span></span>



| <span data-ttu-id="e8500-152">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-152">Order</span></span> | <span data-ttu-id="e8500-153">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-153">Path</span></span>                         | <span data-ttu-id="e8500-154">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e8500-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e8500-155">1</span><span class="sxs-lookup"><span data-stu-id="e8500-155">1</span></span>     | <span data-ttu-id="e8500-156">/ИФД/ГПС/{ушорт = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="e8500-157">2</span><span class="sxs-lookup"><span data-stu-id="e8500-157">2</span></span>     | <span data-ttu-id="e8500-158">/ИФД/КСМП/ексиф: Гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e8500-159">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e8500-159">Remove Paths</span></span>



| <span data-ttu-id="e8500-160">Заказ</span><span class="sxs-lookup"><span data-stu-id="e8500-160">Order</span></span> | <span data-ttu-id="e8500-161">Путь</span><span class="sxs-lookup"><span data-stu-id="e8500-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="e8500-162">1</span><span class="sxs-lookup"><span data-stu-id="e8500-162">1</span></span>     | <span data-ttu-id="e8500-163">/ИФД/ГПС/{ушорт = 24}</span><span class="sxs-lookup"><span data-stu-id="e8500-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="e8500-164">2</span><span class="sxs-lookup"><span data-stu-id="e8500-164">2</span></span>     | <span data-ttu-id="e8500-165">/ИФД/КСМП/ексиф: гпсдестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e8500-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8500-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8500-167">См. также</span><span class="sxs-lookup"><span data-stu-id="e8500-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8500-168">System. GPS. Дестбеаринг</span><span class="sxs-lookup"><span data-stu-id="e8500-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
