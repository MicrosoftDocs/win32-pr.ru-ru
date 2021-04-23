---
description: Политика метаданных фотографии для свойства System. photo. Камерамодел.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Политика метаданных фото для System. photo. Камерамодел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912623"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="14e54-103">Политика метаданных фото для System. photo. Камерамодел</span><span class="sxs-lookup"><span data-stu-id="14e54-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="14e54-104">Политика метаданных фотографии для свойства [System. photo. камерамодел](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="14e54-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="14e54-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="14e54-105">PKEY</span></span>

<span data-ttu-id="14e54-106">\_Камерамодел фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="14e54-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="14e54-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="14e54-107">Containers</span></span>

<span data-ttu-id="14e54-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="14e54-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="14e54-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="14e54-109">Read-Only</span></span>

<span data-ttu-id="14e54-110">Нет</span><span class="sxs-lookup"><span data-stu-id="14e54-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="14e54-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="14e54-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="14e54-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="14e54-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="14e54-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="14e54-113">Input Type</span></span>

<span data-ttu-id="14e54-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="14e54-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="14e54-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="14e54-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="14e54-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="14e54-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="14e54-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="14e54-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="14e54-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="14e54-118">Read Paths</span></span>



| <span data-ttu-id="14e54-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-119">Order</span></span> | <span data-ttu-id="14e54-120">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-120">Path</span></span>                   | <span data-ttu-id="14e54-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14e54-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="14e54-122">1</span><span class="sxs-lookup"><span data-stu-id="14e54-122">1</span></span>     | <span data-ttu-id="14e54-123">/APP1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="14e54-124">ascii</span><span class="sxs-lookup"><span data-stu-id="14e54-124">ascii</span></span>       |
| <span data-ttu-id="14e54-125">2</span><span class="sxs-lookup"><span data-stu-id="14e54-125">2</span></span>     | <span data-ttu-id="14e54-126">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="14e54-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-127">unicode</span></span>     |
| <span data-ttu-id="14e54-128">3</span><span class="sxs-lookup"><span data-stu-id="14e54-128">3</span></span>     | <span data-ttu-id="14e54-129">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="14e54-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14e54-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="14e54-131">Write Paths</span></span>



| <span data-ttu-id="14e54-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-132">Order</span></span> | <span data-ttu-id="14e54-133">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-133">Path</span></span>                   | <span data-ttu-id="14e54-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14e54-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="14e54-135">1</span><span class="sxs-lookup"><span data-stu-id="14e54-135">1</span></span>     | <span data-ttu-id="14e54-136">/APP1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="14e54-137">ascii</span><span class="sxs-lookup"><span data-stu-id="14e54-137">ascii</span></span>       |
| <span data-ttu-id="14e54-138">2</span><span class="sxs-lookup"><span data-stu-id="14e54-138">2</span></span>     | <span data-ttu-id="14e54-139">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="14e54-140">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-140">unicode</span></span>     |
| <span data-ttu-id="14e54-141">3</span><span class="sxs-lookup"><span data-stu-id="14e54-141">3</span></span>     | <span data-ttu-id="14e54-142">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="14e54-143">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14e54-144">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="14e54-144">Remove Paths</span></span>



| <span data-ttu-id="14e54-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-145">Order</span></span> | <span data-ttu-id="14e54-146">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="14e54-147">1</span><span class="sxs-lookup"><span data-stu-id="14e54-147">1</span></span>     | <span data-ttu-id="14e54-148">/APP1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="14e54-149">2</span><span class="sxs-lookup"><span data-stu-id="14e54-149">2</span></span>     | <span data-ttu-id="14e54-150">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="14e54-151">3</span><span class="sxs-lookup"><span data-stu-id="14e54-151">3</span></span>     | <span data-ttu-id="14e54-152">/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="14e54-153">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="14e54-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="14e54-154">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="14e54-154">Read Paths</span></span>



| <span data-ttu-id="14e54-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-155">Order</span></span> | <span data-ttu-id="14e54-156">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-156">Path</span></span>                | <span data-ttu-id="14e54-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14e54-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="14e54-158">1</span><span class="sxs-lookup"><span data-stu-id="14e54-158">1</span></span>     | <span data-ttu-id="14e54-159">/ИФД/{ушорт = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="14e54-160">ascii</span><span class="sxs-lookup"><span data-stu-id="14e54-160">ascii</span></span>       |
| <span data-ttu-id="14e54-161">2</span><span class="sxs-lookup"><span data-stu-id="14e54-161">2</span></span>     | <span data-ttu-id="14e54-162">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="14e54-163">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-163">unicode</span></span>     |
| <span data-ttu-id="14e54-164">3</span><span class="sxs-lookup"><span data-stu-id="14e54-164">3</span></span>     | <span data-ttu-id="14e54-165">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="14e54-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14e54-167">Пути записи</span><span class="sxs-lookup"><span data-stu-id="14e54-167">Write Paths</span></span>



| <span data-ttu-id="14e54-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-168">Order</span></span> | <span data-ttu-id="14e54-169">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-169">Path</span></span>                | <span data-ttu-id="14e54-170">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14e54-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="14e54-171">1</span><span class="sxs-lookup"><span data-stu-id="14e54-171">1</span></span>     | <span data-ttu-id="14e54-172">/ИФД/{ушорт = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="14e54-173">ascii</span><span class="sxs-lookup"><span data-stu-id="14e54-173">ascii</span></span>       |
| <span data-ttu-id="14e54-174">2</span><span class="sxs-lookup"><span data-stu-id="14e54-174">2</span></span>     | <span data-ttu-id="14e54-175">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="14e54-176">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-176">unicode</span></span>     |
| <span data-ttu-id="14e54-177">3</span><span class="sxs-lookup"><span data-stu-id="14e54-177">3</span></span>     | <span data-ttu-id="14e54-178">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="14e54-179">Юникод</span><span class="sxs-lookup"><span data-stu-id="14e54-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14e54-180">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="14e54-180">Remove Paths</span></span>



| <span data-ttu-id="14e54-181">Заказ</span><span class="sxs-lookup"><span data-stu-id="14e54-181">Order</span></span> | <span data-ttu-id="14e54-182">Путь</span><span class="sxs-lookup"><span data-stu-id="14e54-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="14e54-183">1</span><span class="sxs-lookup"><span data-stu-id="14e54-183">1</span></span>     | <span data-ttu-id="14e54-184">/ИФД/{ушорт = 272}</span><span class="sxs-lookup"><span data-stu-id="14e54-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="14e54-185">2</span><span class="sxs-lookup"><span data-stu-id="14e54-185">2</span></span>     | <span data-ttu-id="14e54-186">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="14e54-187">3</span><span class="sxs-lookup"><span data-stu-id="14e54-187">3</span></span>     | <span data-ttu-id="14e54-188">/ИФД/КСМП/Тифф: модель</span><span class="sxs-lookup"><span data-stu-id="14e54-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14e54-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14e54-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e54-190">См. также</span><span class="sxs-lookup"><span data-stu-id="14e54-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e54-191">System. photo. Камерамодел</span><span class="sxs-lookup"><span data-stu-id="14e54-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
