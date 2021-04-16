---
description: Политика метаданных фотографии для свойства System. photo. Камерамануфактурер.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Политика метаданных фото для System. photo. Камерамануфактурер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702905"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a><span data-ttu-id="7bc26-103">Политика метаданных фото для System. photo. Камерамануфактурер</span><span class="sxs-lookup"><span data-stu-id="7bc26-103">System.Photo.CameraManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="7bc26-104">Политика метаданных фотографии для свойства [System. photo. камерамануфактурер](../properties/props-system-photo-cameramanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc26-104">The photo metadata policy for the [System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7bc26-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7bc26-105">PKEY</span></span>

<span data-ttu-id="7bc26-106">\_Камерамануфактурер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="7bc26-106">PKEY\_Photo\_CameraManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="7bc26-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="7bc26-107">Containers</span></span>

<span data-ttu-id="7bc26-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7bc26-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7bc26-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7bc26-109">Read-Only</span></span>

<span data-ttu-id="7bc26-110">Нет</span><span class="sxs-lookup"><span data-stu-id="7bc26-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7bc26-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="7bc26-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7bc26-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="7bc26-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7bc26-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="7bc26-113">Input Type</span></span>

<span data-ttu-id="7bc26-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="7bc26-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7bc26-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="7bc26-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7bc26-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="7bc26-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7bc26-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="7bc26-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7bc26-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="7bc26-118">Read Paths</span></span>



| <span data-ttu-id="7bc26-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-119">Order</span></span> | <span data-ttu-id="7bc26-120">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-120">Path</span></span>                   | <span data-ttu-id="7bc26-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7bc26-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7bc26-122">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-122">1</span></span>     | <span data-ttu-id="7bc26-123">/APP1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-123">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="7bc26-124">ascii</span><span class="sxs-lookup"><span data-stu-id="7bc26-124">ascii</span></span>       |
| <span data-ttu-id="7bc26-125">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-125">2</span></span>     | <span data-ttu-id="7bc26-126">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-126">/xmp/tiff:Make</span></span>         | <span data-ttu-id="7bc26-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-127">unicode</span></span>     |
| <span data-ttu-id="7bc26-128">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-128">3</span></span>     | <span data-ttu-id="7bc26-129">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-129">/xmp/tiff:make</span></span>         | <span data-ttu-id="7bc26-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7bc26-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="7bc26-131">Write Paths</span></span>



| <span data-ttu-id="7bc26-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-132">Order</span></span> | <span data-ttu-id="7bc26-133">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-133">Path</span></span>                   | <span data-ttu-id="7bc26-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7bc26-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7bc26-135">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-135">1</span></span>     | <span data-ttu-id="7bc26-136">/APP1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-136">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="7bc26-137">ascii</span><span class="sxs-lookup"><span data-stu-id="7bc26-137">ascii</span></span>       |
| <span data-ttu-id="7bc26-138">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-138">2</span></span>     | <span data-ttu-id="7bc26-139">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-139">/xmp/tiff:Make</span></span>         | <span data-ttu-id="7bc26-140">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-140">unicode</span></span>     |
| <span data-ttu-id="7bc26-141">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-141">3</span></span>     | <span data-ttu-id="7bc26-142">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-142">/xmp/tiff:make</span></span>         | <span data-ttu-id="7bc26-143">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7bc26-144">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="7bc26-144">Remove Paths</span></span>



| <span data-ttu-id="7bc26-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-145">Order</span></span> | <span data-ttu-id="7bc26-146">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="7bc26-147">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-147">1</span></span>     | <span data-ttu-id="7bc26-148">/APP1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-148">/app1/ifd/{ushort=271}</span></span> |
| <span data-ttu-id="7bc26-149">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-149">2</span></span>     | <span data-ttu-id="7bc26-150">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-150">/xmp/tiff:Make</span></span>         |
| <span data-ttu-id="7bc26-151">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-151">3</span></span>     | <span data-ttu-id="7bc26-152">/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-152">/xmp/tiff:make</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="7bc26-153">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="7bc26-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7bc26-154">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="7bc26-154">Read Paths</span></span>



| <span data-ttu-id="7bc26-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-155">Order</span></span> | <span data-ttu-id="7bc26-156">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-156">Path</span></span>               | <span data-ttu-id="7bc26-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7bc26-157">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="7bc26-158">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-158">1</span></span>     | <span data-ttu-id="7bc26-159">/ИФД/{ушорт = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-159">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="7bc26-160">ascii</span><span class="sxs-lookup"><span data-stu-id="7bc26-160">ascii</span></span>       |
| <span data-ttu-id="7bc26-161">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-161">2</span></span>     | <span data-ttu-id="7bc26-162">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-162">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="7bc26-163">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-163">unicode</span></span>     |
| <span data-ttu-id="7bc26-164">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-164">3</span></span>     | <span data-ttu-id="7bc26-165">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-165">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="7bc26-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7bc26-167">Пути записи</span><span class="sxs-lookup"><span data-stu-id="7bc26-167">Write Paths</span></span>



| <span data-ttu-id="7bc26-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-168">Order</span></span> | <span data-ttu-id="7bc26-169">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-169">Path</span></span>               | <span data-ttu-id="7bc26-170">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7bc26-170">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="7bc26-171">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-171">1</span></span>     | <span data-ttu-id="7bc26-172">/ИФД/{ушорт = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-172">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="7bc26-173">ascii</span><span class="sxs-lookup"><span data-stu-id="7bc26-173">ascii</span></span>       |
| <span data-ttu-id="7bc26-174">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-174">2</span></span>     | <span data-ttu-id="7bc26-175">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-175">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="7bc26-176">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-176">unicode</span></span>     |
| <span data-ttu-id="7bc26-177">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-177">3</span></span>     | <span data-ttu-id="7bc26-178">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-178">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="7bc26-179">Юникод</span><span class="sxs-lookup"><span data-stu-id="7bc26-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7bc26-180">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="7bc26-180">Remove Paths</span></span>



| <span data-ttu-id="7bc26-181">Заказ</span><span class="sxs-lookup"><span data-stu-id="7bc26-181">Order</span></span> | <span data-ttu-id="7bc26-182">Путь</span><span class="sxs-lookup"><span data-stu-id="7bc26-182">Path</span></span>               |
|-------|--------------------|
| <span data-ttu-id="7bc26-183">1</span><span class="sxs-lookup"><span data-stu-id="7bc26-183">1</span></span>     | <span data-ttu-id="7bc26-184">/ИФД/{ушорт = 271}</span><span class="sxs-lookup"><span data-stu-id="7bc26-184">/ifd/{ushort=271}</span></span>  |
| <span data-ttu-id="7bc26-185">2</span><span class="sxs-lookup"><span data-stu-id="7bc26-185">2</span></span>     | <span data-ttu-id="7bc26-186">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-186">/ifd/xmp/tiff:Make</span></span> |
| <span data-ttu-id="7bc26-187">3</span><span class="sxs-lookup"><span data-stu-id="7bc26-187">3</span></span>     | <span data-ttu-id="7bc26-188">/ИФД/КСМП/Тифф: make</span><span class="sxs-lookup"><span data-stu-id="7bc26-188">/ifd/xmp/tiff:make</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7bc26-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bc26-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc26-190">См. также</span><span class="sxs-lookup"><span data-stu-id="7bc26-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc26-191">System. photo. Камерамануфактурер</span><span class="sxs-lookup"><span data-stu-id="7bc26-191">System.Photo.CameraManufacturer</span></span>](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
