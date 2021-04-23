---
description: Политика метаданных фотографии для свойства System. GPS. Спутниковоеs.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Политика метаданных фотографии System. GPS. Спутниковое
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673875"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="c9688-103">Политика метаданных фотографии System. GPS. Спутниковое</span><span class="sxs-lookup"><span data-stu-id="c9688-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="c9688-104">Политика метаданных фотографии для свойства [System. GPS. спутниковоеs](../properties/props-system-gps-satellites.md) .</span><span class="sxs-lookup"><span data-stu-id="c9688-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c9688-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c9688-105">PKEY</span></span>

<span data-ttu-id="c9688-106">\_Вспомогательная лицензия GPS "PKEY" \_</span><span class="sxs-lookup"><span data-stu-id="c9688-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="c9688-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="c9688-107">Containers</span></span>

<span data-ttu-id="c9688-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c9688-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c9688-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c9688-109">Read-Only</span></span>

<span data-ttu-id="c9688-110">Нет</span><span class="sxs-lookup"><span data-stu-id="c9688-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c9688-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="c9688-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c9688-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c9688-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c9688-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="c9688-113">Input Type</span></span>

<span data-ttu-id="c9688-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="c9688-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c9688-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="c9688-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c9688-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="c9688-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c9688-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="c9688-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c9688-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c9688-118">Read Paths</span></span>



| <span data-ttu-id="c9688-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-119">Order</span></span> | <span data-ttu-id="c9688-120">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-120">Path</span></span>                     | <span data-ttu-id="c9688-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c9688-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c9688-122">1</span><span class="sxs-lookup"><span data-stu-id="c9688-122">1</span></span>     | <span data-ttu-id="c9688-123">/APP1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="c9688-124">ascii</span><span class="sxs-lookup"><span data-stu-id="c9688-124">ascii</span></span>       |
| <span data-ttu-id="c9688-125">2</span><span class="sxs-lookup"><span data-stu-id="c9688-125">2</span></span>     | <span data-ttu-id="c9688-126">/КСМП/ексиф: Гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="c9688-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="c9688-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c9688-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c9688-128">Write Paths</span></span>



| <span data-ttu-id="c9688-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-129">Order</span></span> | <span data-ttu-id="c9688-130">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-130">Path</span></span>                     | <span data-ttu-id="c9688-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c9688-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c9688-132">1</span><span class="sxs-lookup"><span data-stu-id="c9688-132">1</span></span>     | <span data-ttu-id="c9688-133">/APP1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="c9688-134">ascii</span><span class="sxs-lookup"><span data-stu-id="c9688-134">ascii</span></span>       |
| <span data-ttu-id="c9688-135">2</span><span class="sxs-lookup"><span data-stu-id="c9688-135">2</span></span>     | <span data-ttu-id="c9688-136">/КСМП/ексиф: Гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="c9688-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="c9688-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c9688-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c9688-138">Remove Paths</span></span>



| <span data-ttu-id="c9688-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-139">Order</span></span> | <span data-ttu-id="c9688-140">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c9688-141">1</span><span class="sxs-lookup"><span data-stu-id="c9688-141">1</span></span>     | <span data-ttu-id="c9688-142">/APP1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="c9688-143">2</span><span class="sxs-lookup"><span data-stu-id="c9688-143">2</span></span>     | <span data-ttu-id="c9688-144">/КСМП/ексиф: гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="c9688-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="c9688-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c9688-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c9688-146">Read Paths</span></span>



| <span data-ttu-id="c9688-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-147">Order</span></span> | <span data-ttu-id="c9688-148">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-148">Path</span></span>                        | <span data-ttu-id="c9688-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c9688-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="c9688-150">1</span><span class="sxs-lookup"><span data-stu-id="c9688-150">1</span></span>     | <span data-ttu-id="c9688-151">/ИФД/ГПС/{ушорт = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="c9688-152">ascii</span><span class="sxs-lookup"><span data-stu-id="c9688-152">ascii</span></span>       |
| <span data-ttu-id="c9688-153">2</span><span class="sxs-lookup"><span data-stu-id="c9688-153">2</span></span>     | <span data-ttu-id="c9688-154">/ИФД/КСМП/ексиф: Гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="c9688-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="c9688-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c9688-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c9688-156">Write Paths</span></span>



| <span data-ttu-id="c9688-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-157">Order</span></span> | <span data-ttu-id="c9688-158">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-158">Path</span></span>                        | <span data-ttu-id="c9688-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c9688-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="c9688-160">1</span><span class="sxs-lookup"><span data-stu-id="c9688-160">1</span></span>     | <span data-ttu-id="c9688-161">/ИФД/ГПС/{ушорт = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="c9688-162">ascii</span><span class="sxs-lookup"><span data-stu-id="c9688-162">ascii</span></span>       |
| <span data-ttu-id="c9688-163">2</span><span class="sxs-lookup"><span data-stu-id="c9688-163">2</span></span>     | <span data-ttu-id="c9688-164">/ИФД/КСМП/ексиф: Гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="c9688-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="c9688-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c9688-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c9688-166">Remove Paths</span></span>



| <span data-ttu-id="c9688-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="c9688-167">Order</span></span> | <span data-ttu-id="c9688-168">Путь</span><span class="sxs-lookup"><span data-stu-id="c9688-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="c9688-169">1</span><span class="sxs-lookup"><span data-stu-id="c9688-169">1</span></span>     | <span data-ttu-id="c9688-170">/ИФД/ГПС/{ушорт = 8}</span><span class="sxs-lookup"><span data-stu-id="c9688-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="c9688-171">2</span><span class="sxs-lookup"><span data-stu-id="c9688-171">2</span></span>     | <span data-ttu-id="c9688-172">/ИФД/КСМП/ексиф: гпссателлитес</span><span class="sxs-lookup"><span data-stu-id="c9688-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c9688-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9688-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9688-174">См. также</span><span class="sxs-lookup"><span data-stu-id="c9688-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9688-175">System. GPS. спутники</span><span class="sxs-lookup"><span data-stu-id="c9688-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
