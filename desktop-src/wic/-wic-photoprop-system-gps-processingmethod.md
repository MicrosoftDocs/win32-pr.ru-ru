---
description: Политика метаданных фотографии для свойства System. GPS. Процессингмесод.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Политика метаданных фотографии System. GPS. Процессингмесод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674387"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="cf33a-103">Политика метаданных фотографии System. GPS. Процессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="cf33a-104">Политика метаданных фотографии для свойства [System. GPS. процессингмесод](../properties/props-system-gps-processingmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="cf33a-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cf33a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cf33a-105">PKEY</span></span>

<span data-ttu-id="cf33a-106">PKEY \_ GPS \_ процессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="cf33a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="cf33a-107">Containers</span></span>

<span data-ttu-id="cf33a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cf33a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cf33a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf33a-109">Read-Only</span></span>

<span data-ttu-id="cf33a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="cf33a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cf33a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="cf33a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cf33a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cf33a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cf33a-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="cf33a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cf33a-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="cf33a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cf33a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="cf33a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cf33a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="cf33a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="cf33a-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="cf33a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cf33a-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="cf33a-118">Read Paths</span></span>



| <span data-ttu-id="cf33a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-119">Order</span></span> | <span data-ttu-id="cf33a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-120">Path</span></span>                          | <span data-ttu-id="cf33a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cf33a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cf33a-122">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-122">1</span></span>     | <span data-ttu-id="cf33a-123">/APP1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="cf33a-124">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-124">2</span></span>     | <span data-ttu-id="cf33a-125">/КСМП/ексиф: Гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="cf33a-126">Юникод</span><span class="sxs-lookup"><span data-stu-id="cf33a-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="cf33a-127">Пути записи</span><span class="sxs-lookup"><span data-stu-id="cf33a-127">Write Paths</span></span>



| <span data-ttu-id="cf33a-128">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-128">Order</span></span> | <span data-ttu-id="cf33a-129">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-129">Path</span></span>                          | <span data-ttu-id="cf33a-130">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cf33a-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cf33a-131">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-131">1</span></span>     | <span data-ttu-id="cf33a-132">/APP1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="cf33a-133">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-133">2</span></span>     | <span data-ttu-id="cf33a-134">/КСМП/ексиф: Гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="cf33a-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="cf33a-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="cf33a-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="cf33a-136">Remove Paths</span></span>



| <span data-ttu-id="cf33a-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-137">Order</span></span> | <span data-ttu-id="cf33a-138">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cf33a-139">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-139">1</span></span>     | <span data-ttu-id="cf33a-140">/APP1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="cf33a-141">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-141">2</span></span>     | <span data-ttu-id="cf33a-142">/КСМП/ексиф: гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="cf33a-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="cf33a-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cf33a-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="cf33a-144">Read Paths</span></span>



| <span data-ttu-id="cf33a-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-145">Order</span></span> | <span data-ttu-id="cf33a-146">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-146">Path</span></span>                              | <span data-ttu-id="cf33a-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cf33a-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="cf33a-148">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-148">1</span></span>     | <span data-ttu-id="cf33a-149">/ИФД/КСМП/ексиф: Гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="cf33a-150">Юникод</span><span class="sxs-lookup"><span data-stu-id="cf33a-150">unicode</span></span>     |
| <span data-ttu-id="cf33a-151">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-151">2</span></span>     | <span data-ttu-id="cf33a-152">/ИФД/ГПС/{ушорт = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="cf33a-153">Пути записи</span><span class="sxs-lookup"><span data-stu-id="cf33a-153">Write Paths</span></span>



| <span data-ttu-id="cf33a-154">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-154">Order</span></span> | <span data-ttu-id="cf33a-155">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-155">Path</span></span>                              | <span data-ttu-id="cf33a-156">Формат диска</span><span class="sxs-lookup"><span data-stu-id="cf33a-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="cf33a-157">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-157">1</span></span>     | <span data-ttu-id="cf33a-158">/ИФД/КСМП/ексиф: Гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="cf33a-159">Юникод</span><span class="sxs-lookup"><span data-stu-id="cf33a-159">unicode</span></span>     |
| <span data-ttu-id="cf33a-160">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-160">2</span></span>     | <span data-ttu-id="cf33a-161">/ИФД/ГПС/{ушорт = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="cf33a-162">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="cf33a-162">Remove Paths</span></span>



| <span data-ttu-id="cf33a-163">Заказ</span><span class="sxs-lookup"><span data-stu-id="cf33a-163">Order</span></span> | <span data-ttu-id="cf33a-164">Путь</span><span class="sxs-lookup"><span data-stu-id="cf33a-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="cf33a-165">1</span><span class="sxs-lookup"><span data-stu-id="cf33a-165">1</span></span>     | <span data-ttu-id="cf33a-166">/ИФД/КСМП/ексиф: гпспроцессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="cf33a-167">2</span><span class="sxs-lookup"><span data-stu-id="cf33a-167">2</span></span>     | <span data-ttu-id="cf33a-168">/ИФД/ГПС/{ушорт = 27}</span><span class="sxs-lookup"><span data-stu-id="cf33a-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="cf33a-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf33a-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf33a-170">См. также</span><span class="sxs-lookup"><span data-stu-id="cf33a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf33a-171">System. GPS. Процессингмесод</span><span class="sxs-lookup"><span data-stu-id="cf33a-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
