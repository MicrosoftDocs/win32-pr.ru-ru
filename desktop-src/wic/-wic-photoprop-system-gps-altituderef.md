---
description: Политика метаданных фотографии для свойства System. GPS. Алтитудереф.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Политика метаданных фотографии System. GPS. Алтитудереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712801"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="e587d-103">Политика метаданных фотографии System. GPS. Алтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="e587d-104">Политика метаданных фотографии для свойства [System. GPS. алтитудереф](../properties/props-system-gps-altituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="e587d-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e587d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e587d-105">PKEY</span></span>

<span data-ttu-id="e587d-106">PKEY \_ GPS \_ алтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="e587d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e587d-107">Description</span></span>

<span data-ttu-id="e587d-108">Указывает высоту, используемую в качестве высоты ссылки.</span><span class="sxs-lookup"><span data-stu-id="e587d-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="e587d-109">Значение 0 указывает, что высота превышает уровень моря.</span><span class="sxs-lookup"><span data-stu-id="e587d-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="e587d-110">Значение 1 указывает на высоту ниже уровня Sea.</span><span class="sxs-lookup"><span data-stu-id="e587d-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="e587d-111">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e587d-111">Containers</span></span>

<span data-ttu-id="e587d-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e587d-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e587d-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e587d-113">Read-Only</span></span>

<span data-ttu-id="e587d-114">Нет</span><span class="sxs-lookup"><span data-stu-id="e587d-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e587d-115">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e587d-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e587d-116">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e587d-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="e587d-117">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="e587d-117">Input Type</span></span>

<span data-ttu-id="e587d-118">Двухбайтовых.</span><span class="sxs-lookup"><span data-stu-id="e587d-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e587d-119">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e587d-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="e587d-120">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e587d-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="e587d-121">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="e587d-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e587d-122">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e587d-122">Read Paths</span></span>



| <span data-ttu-id="e587d-123">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-123">Order</span></span> | <span data-ttu-id="e587d-124">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-124">Path</span></span>                     | <span data-ttu-id="e587d-125">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e587d-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e587d-126">1</span><span class="sxs-lookup"><span data-stu-id="e587d-126">1</span></span>     | <span data-ttu-id="e587d-127">/APP1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="e587d-128">byte</span><span class="sxs-lookup"><span data-stu-id="e587d-128">byte</span></span>        |
| <span data-ttu-id="e587d-129">2</span><span class="sxs-lookup"><span data-stu-id="e587d-129">2</span></span>     | <span data-ttu-id="e587d-130">/КСМП/ексиф: Гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="e587d-131">Юникод</span><span class="sxs-lookup"><span data-stu-id="e587d-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e587d-132">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e587d-132">Write Paths</span></span>



| <span data-ttu-id="e587d-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-133">Order</span></span> | <span data-ttu-id="e587d-134">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-134">Path</span></span>                     | <span data-ttu-id="e587d-135">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e587d-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e587d-136">1</span><span class="sxs-lookup"><span data-stu-id="e587d-136">1</span></span>     | <span data-ttu-id="e587d-137">/APP1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="e587d-138">byte</span><span class="sxs-lookup"><span data-stu-id="e587d-138">byte</span></span>        |
| <span data-ttu-id="e587d-139">2</span><span class="sxs-lookup"><span data-stu-id="e587d-139">2</span></span>     | <span data-ttu-id="e587d-140">/КСМП/ексиф: Гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="e587d-141">Юникод</span><span class="sxs-lookup"><span data-stu-id="e587d-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e587d-142">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e587d-142">Remove Paths</span></span>



| <span data-ttu-id="e587d-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-143">Order</span></span> | <span data-ttu-id="e587d-144">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e587d-145">1</span><span class="sxs-lookup"><span data-stu-id="e587d-145">1</span></span>     | <span data-ttu-id="e587d-146">/APP1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="e587d-147">2</span><span class="sxs-lookup"><span data-stu-id="e587d-147">2</span></span>     | <span data-ttu-id="e587d-148">/КСМП/ексиф: гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="e587d-149">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="e587d-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e587d-150">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e587d-150">Read Paths</span></span>



| <span data-ttu-id="e587d-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-151">Order</span></span> | <span data-ttu-id="e587d-152">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-152">Path</span></span>                         | <span data-ttu-id="e587d-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e587d-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e587d-154">1</span><span class="sxs-lookup"><span data-stu-id="e587d-154">1</span></span>     | <span data-ttu-id="e587d-155">/ИФД/ГПС/{ушорт = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="e587d-156">byte</span><span class="sxs-lookup"><span data-stu-id="e587d-156">byte</span></span>        |
| <span data-ttu-id="e587d-157">2</span><span class="sxs-lookup"><span data-stu-id="e587d-157">2</span></span>     | <span data-ttu-id="e587d-158">/ИФД/КСМП/ексиф: Гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="e587d-159">Юникод</span><span class="sxs-lookup"><span data-stu-id="e587d-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e587d-160">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e587d-160">Write Paths</span></span>



| <span data-ttu-id="e587d-161">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-161">Order</span></span> | <span data-ttu-id="e587d-162">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-162">Path</span></span>                         | <span data-ttu-id="e587d-163">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e587d-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e587d-164">1</span><span class="sxs-lookup"><span data-stu-id="e587d-164">1</span></span>     | <span data-ttu-id="e587d-165">/ИФД/ГПС/{ушорт = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="e587d-166">byte</span><span class="sxs-lookup"><span data-stu-id="e587d-166">byte</span></span>        |
| <span data-ttu-id="e587d-167">2</span><span class="sxs-lookup"><span data-stu-id="e587d-167">2</span></span>     | <span data-ttu-id="e587d-168">/ИФД/КСМП/ексиф: Гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="e587d-169">Юникод</span><span class="sxs-lookup"><span data-stu-id="e587d-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e587d-170">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e587d-170">Remove Paths</span></span>



| <span data-ttu-id="e587d-171">Заказ</span><span class="sxs-lookup"><span data-stu-id="e587d-171">Order</span></span> | <span data-ttu-id="e587d-172">Путь</span><span class="sxs-lookup"><span data-stu-id="e587d-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="e587d-173">1</span><span class="sxs-lookup"><span data-stu-id="e587d-173">1</span></span>     | <span data-ttu-id="e587d-174">/ИФД/ГПС/{ушорт = 5}</span><span class="sxs-lookup"><span data-stu-id="e587d-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="e587d-175">2</span><span class="sxs-lookup"><span data-stu-id="e587d-175">2</span></span>     | <span data-ttu-id="e587d-176">/ИФД/КСМП/ексиф: гпсалтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e587d-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e587d-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e587d-178">См. также</span><span class="sxs-lookup"><span data-stu-id="e587d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e587d-179">System. GPS. Алтитудереф</span><span class="sxs-lookup"><span data-stu-id="e587d-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
