---
description: Политика метаданных фотографии для свойства System. GPS. Дестбеарингреф.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Политика метаданных фотографии System. GPS. Дестбеарингреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265293"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="b2b9e-103">Политика метаданных фотографии System. GPS. Дестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="b2b9e-104">Политика метаданных фотографии для свойства [System. GPS. дестбеарингреф](../properties/props-system-gps-destbearingref.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b9e-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b2b9e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b2b9e-105">PKEY</span></span>

<span data-ttu-id="b2b9e-106">PKEY \_ GPS \_ дестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="b2b9e-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="b2b9e-107">Containers</span></span>

<span data-ttu-id="b2b9e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b2b9e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b2b9e-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b2b9e-109">Read-Only</span></span>

<span data-ttu-id="b2b9e-110">Нет</span><span class="sxs-lookup"><span data-stu-id="b2b9e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b2b9e-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b2b9e-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b2b9e-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b2b9e-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="b2b9e-113">Input Type</span></span>

<span data-ttu-id="b2b9e-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b2b9e-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="b2b9e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b2b9e-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="b2b9e-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="b2b9e-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b2b9e-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="b2b9e-118">Read Paths</span></span>



| <span data-ttu-id="b2b9e-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-119">Order</span></span> | <span data-ttu-id="b2b9e-120">Путь</span><span class="sxs-lookup"><span data-stu-id="b2b9e-120">Path</span></span>                        | <span data-ttu-id="b2b9e-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b2b9e-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="b2b9e-122">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-122">1</span></span>     | <span data-ttu-id="b2b9e-123">/APP1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="b2b9e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="b2b9e-124">ascii</span></span>       |
| <span data-ttu-id="b2b9e-125">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-125">2</span></span>     | <span data-ttu-id="b2b9e-126">/КСМП/ексиф: Гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="b2b9e-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="b2b9e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b2b9e-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="b2b9e-128">Write Paths</span></span>



| <span data-ttu-id="b2b9e-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-129">Order</span></span> | <span data-ttu-id="b2b9e-130">Путь</span><span class="sxs-lookup"><span data-stu-id="b2b9e-130">Path</span></span>                        | <span data-ttu-id="b2b9e-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b2b9e-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="b2b9e-132">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-132">1</span></span>     | <span data-ttu-id="b2b9e-133">/APP1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="b2b9e-134">ascii</span><span class="sxs-lookup"><span data-stu-id="b2b9e-134">ascii</span></span>       |
| <span data-ttu-id="b2b9e-135">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-135">2</span></span>     | <span data-ttu-id="b2b9e-136">/КСМП/ексиф: Гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="b2b9e-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="b2b9e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b2b9e-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="b2b9e-138">Remove Paths</span></span>



| <span data-ttu-id="b2b9e-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-139">Order</span></span> | <span data-ttu-id="b2b9e-140">Путь</span><span class="sxs-lookup"><span data-stu-id="b2b9e-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="b2b9e-141">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-141">1</span></span>     | <span data-ttu-id="b2b9e-142">/APP1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="b2b9e-143">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-143">2</span></span>     | <span data-ttu-id="b2b9e-144">/КСМП/ексиф: гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b2b9e-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="b2b9e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b2b9e-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="b2b9e-146">Read Paths</span></span>



| <span data-ttu-id="b2b9e-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-147">Order</span></span> | <span data-ttu-id="b2b9e-148">Путь</span><span class="sxs-lookup"><span data-stu-id="b2b9e-148">Path</span></span>                            | <span data-ttu-id="b2b9e-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b2b9e-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b2b9e-150">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-150">1</span></span>     | <span data-ttu-id="b2b9e-151">/ИФД/ГПС/{ушорт = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="b2b9e-152">ascii</span><span class="sxs-lookup"><span data-stu-id="b2b9e-152">ascii</span></span>       |
| <span data-ttu-id="b2b9e-153">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-153">2</span></span>     | <span data-ttu-id="b2b9e-154">/ИФД/КСМП/ексиф: Гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="b2b9e-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="b2b9e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b2b9e-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="b2b9e-156">Write Paths</span></span>



| <span data-ttu-id="b2b9e-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="b2b9e-157">Order</span></span> | <span data-ttu-id="b2b9e-158">Путь</span><span class="sxs-lookup"><span data-stu-id="b2b9e-158">Path</span></span>                            | <span data-ttu-id="b2b9e-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b2b9e-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b2b9e-160">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-160">1</span></span>     | <span data-ttu-id="b2b9e-161">/ИФД/ГПС/{ушорт = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="b2b9e-162">ascii</span><span class="sxs-lookup"><span data-stu-id="b2b9e-162">ascii</span></span>       |
| <span data-ttu-id="b2b9e-163">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-163">2</span></span>     | <span data-ttu-id="b2b9e-164">/ИФД/КСМП/ексиф: Гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="b2b9e-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="b2b9e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b2b9e-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="b2b9e-166">Remove Paths</span></span>



| <span data-ttu-id="b2b9e-167">порядок</span><span class="sxs-lookup"><span data-stu-id="b2b9e-167">order</span></span> | <span data-ttu-id="b2b9e-168">path</span><span class="sxs-lookup"><span data-stu-id="b2b9e-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="b2b9e-169">1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-169">1</span></span>     | <span data-ttu-id="b2b9e-170">/ИФД/ГПС/{ушорт = 23}</span><span class="sxs-lookup"><span data-stu-id="b2b9e-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="b2b9e-171">2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-171">2</span></span>     | <span data-ttu-id="b2b9e-172">/ИФД/КСМП/ексиф: гпсдестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b2b9e-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2b9e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b9e-174">См. также</span><span class="sxs-lookup"><span data-stu-id="b2b9e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b9e-175">System. GPS. Дестбеарингреф</span><span class="sxs-lookup"><span data-stu-id="b2b9e-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
