---
description: Политика метаданных фотографии для свойства System. GPS. Имгдиректионреф.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Политика метаданных фотографии System. GPS. Имгдиректионреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272295"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="5d3c8-103">Политика метаданных фотографии System. GPS. Имгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="5d3c8-104">Политика метаданных фотографии для свойства [System. GPS. имгдиректионреф](../properties/props-system-gps-imgdirectionref.md) .</span><span class="sxs-lookup"><span data-stu-id="5d3c8-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5d3c8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5d3c8-105">PKEY</span></span>

<span data-ttu-id="5d3c8-106">PKEY \_ , GPS. имгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="5d3c8-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="5d3c8-107">Containers</span></span>

<span data-ttu-id="5d3c8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5d3c8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5d3c8-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d3c8-109">Read-Only</span></span>

<span data-ttu-id="5d3c8-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5d3c8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5d3c8-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5d3c8-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5d3c8-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="5d3c8-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="5d3c8-113">Input Type</span></span>

<span data-ttu-id="5d3c8-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="5d3c8-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5d3c8-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="5d3c8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5d3c8-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="5d3c8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="5d3c8-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="5d3c8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5d3c8-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="5d3c8-118">Read Paths</span></span>



| <span data-ttu-id="5d3c8-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-119">Order</span></span> | <span data-ttu-id="5d3c8-120">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-120">Path</span></span>                         | <span data-ttu-id="5d3c8-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5d3c8-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="5d3c8-122">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-122">1</span></span>     | <span data-ttu-id="5d3c8-123">/APP1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="5d3c8-124">ascii</span><span class="sxs-lookup"><span data-stu-id="5d3c8-124">ascii</span></span>       |
| <span data-ttu-id="5d3c8-125">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-125">2</span></span>     | <span data-ttu-id="5d3c8-126">/КСМП/ексиф: Гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="5d3c8-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="5d3c8-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5d3c8-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="5d3c8-128">Write Paths</span></span>



| <span data-ttu-id="5d3c8-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-129">Order</span></span> | <span data-ttu-id="5d3c8-130">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-130">Path</span></span>                         | <span data-ttu-id="5d3c8-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5d3c8-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="5d3c8-132">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-132">1</span></span>     | <span data-ttu-id="5d3c8-133">/APP1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="5d3c8-134">ascii</span><span class="sxs-lookup"><span data-stu-id="5d3c8-134">ascii</span></span>       |
| <span data-ttu-id="5d3c8-135">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-135">2</span></span>     | <span data-ttu-id="5d3c8-136">/КСМП/ексиф: Гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="5d3c8-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="5d3c8-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5d3c8-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="5d3c8-138">Remove Paths</span></span>



| <span data-ttu-id="5d3c8-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-139">Order</span></span> | <span data-ttu-id="5d3c8-140">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="5d3c8-141">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-141">1</span></span>     | <span data-ttu-id="5d3c8-142">/APP1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="5d3c8-143">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-143">2</span></span>     | <span data-ttu-id="5d3c8-144">/КСМП/ексиф: гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="5d3c8-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="5d3c8-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5d3c8-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="5d3c8-146">Read Paths</span></span>



| <span data-ttu-id="5d3c8-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-147">Order</span></span> | <span data-ttu-id="5d3c8-148">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-148">Path</span></span>                             | <span data-ttu-id="5d3c8-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5d3c8-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="5d3c8-150">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-150">1</span></span>     | <span data-ttu-id="5d3c8-151">/ИФД/ГПС/{ушорт = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="5d3c8-152">ascii</span><span class="sxs-lookup"><span data-stu-id="5d3c8-152">ascii</span></span>       |
| <span data-ttu-id="5d3c8-153">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-153">2</span></span>     | <span data-ttu-id="5d3c8-154">/ИФД/КСМП/ексиф: Гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="5d3c8-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="5d3c8-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5d3c8-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="5d3c8-156">Write Paths</span></span>



| <span data-ttu-id="5d3c8-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-157">Order</span></span> | <span data-ttu-id="5d3c8-158">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-158">Path</span></span>                             | <span data-ttu-id="5d3c8-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5d3c8-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="5d3c8-160">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-160">1</span></span>     | <span data-ttu-id="5d3c8-161">/ИФД/ГПС/{ушорт = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="5d3c8-162">ascii</span><span class="sxs-lookup"><span data-stu-id="5d3c8-162">ascii</span></span>       |
| <span data-ttu-id="5d3c8-163">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-163">2</span></span>     | <span data-ttu-id="5d3c8-164">/ИФД/КСМП/ексиф: Гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="5d3c8-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="5d3c8-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5d3c8-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="5d3c8-166">Remove Paths</span></span>



| <span data-ttu-id="5d3c8-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="5d3c8-167">Order</span></span> | <span data-ttu-id="5d3c8-168">Путь</span><span class="sxs-lookup"><span data-stu-id="5d3c8-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="5d3c8-169">1</span><span class="sxs-lookup"><span data-stu-id="5d3c8-169">1</span></span>     | <span data-ttu-id="5d3c8-170">/ИФД/ГПС/{ушорт = 16}</span><span class="sxs-lookup"><span data-stu-id="5d3c8-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="5d3c8-171">2</span><span class="sxs-lookup"><span data-stu-id="5d3c8-171">2</span></span>     | <span data-ttu-id="5d3c8-172">/ИФД/КСМП/ексиф: гпсимгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5d3c8-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d3c8-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d3c8-174">См. также</span><span class="sxs-lookup"><span data-stu-id="5d3c8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3c8-175">System. GPS. Имгдиректионреф</span><span class="sxs-lookup"><span data-stu-id="5d3c8-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
