---
description: Политика метаданных фотографии для свойства System. photo. Исоспид.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Политика метаданных фото для System. photo. Исоспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346602"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="382ae-103">Политика метаданных фото для System. photo. Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="382ae-104">Политика метаданных фотографии для свойства [System. photo. исоспид](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="382ae-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="382ae-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="382ae-105">PKEY</span></span>

<span data-ttu-id="382ae-106">\_Исоспид фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="382ae-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="382ae-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="382ae-107">Containers</span></span>

<span data-ttu-id="382ae-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="382ae-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="382ae-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="382ae-109">Read-Only</span></span>

<span data-ttu-id="382ae-110">Нет</span><span class="sxs-lookup"><span data-stu-id="382ae-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="382ae-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="382ae-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="382ae-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="382ae-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="382ae-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="382ae-113">Input Type</span></span>

<span data-ttu-id="382ae-114">UShort</span><span class="sxs-lookup"><span data-stu-id="382ae-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="382ae-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="382ae-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="382ae-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="382ae-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="382ae-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="382ae-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="382ae-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="382ae-118">Read Paths</span></span>



| <span data-ttu-id="382ae-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-119">Order</span></span> | <span data-ttu-id="382ae-120">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-120">Path</span></span>                                    | <span data-ttu-id="382ae-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="382ae-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="382ae-122">1</span><span class="sxs-lookup"><span data-stu-id="382ae-122">1</span></span>     | <span data-ttu-id="382ae-123">/APP1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="382ae-124">ushort</span><span class="sxs-lookup"><span data-stu-id="382ae-124">ushort</span></span>      |
| <span data-ttu-id="382ae-125">2</span><span class="sxs-lookup"><span data-stu-id="382ae-125">2</span></span>     | <span data-ttu-id="382ae-126">/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="382ae-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-127">unicode</span></span>     |
| <span data-ttu-id="382ae-128">3</span><span class="sxs-lookup"><span data-stu-id="382ae-128">3</span></span>     | <span data-ttu-id="382ae-129">/КСМП/ексиф: Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="382ae-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="382ae-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="382ae-131">Write Paths</span></span>



| <span data-ttu-id="382ae-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-132">Order</span></span> | <span data-ttu-id="382ae-133">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-133">Path</span></span>                                    | <span data-ttu-id="382ae-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="382ae-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="382ae-135">1</span><span class="sxs-lookup"><span data-stu-id="382ae-135">1</span></span>     | <span data-ttu-id="382ae-136">/APP1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="382ae-137">ushort</span><span class="sxs-lookup"><span data-stu-id="382ae-137">ushort</span></span>      |
| <span data-ttu-id="382ae-138">2</span><span class="sxs-lookup"><span data-stu-id="382ae-138">2</span></span>     | <span data-ttu-id="382ae-139">/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="382ae-140">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-140">unicode</span></span>     |
| <span data-ttu-id="382ae-141">3</span><span class="sxs-lookup"><span data-stu-id="382ae-141">3</span></span>     | <span data-ttu-id="382ae-142">/КСМП/ексиф: Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="382ae-143">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="382ae-144">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="382ae-144">Remove Paths</span></span>



| <span data-ttu-id="382ae-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-145">Order</span></span> | <span data-ttu-id="382ae-146">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="382ae-147">1</span><span class="sxs-lookup"><span data-stu-id="382ae-147">1</span></span>     | <span data-ttu-id="382ae-148">/APP1/IFD/EXIF/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="382ae-149">2</span><span class="sxs-lookup"><span data-stu-id="382ae-149">2</span></span>     | <span data-ttu-id="382ae-150">/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="382ae-151">3</span><span class="sxs-lookup"><span data-stu-id="382ae-151">3</span></span>     | <span data-ttu-id="382ae-152">/КСМП/ексиф: исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="382ae-153">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="382ae-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="382ae-154">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="382ae-154">Read Paths</span></span>



| <span data-ttu-id="382ae-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-155">Order</span></span> | <span data-ttu-id="382ae-156">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-156">Path</span></span>                                        | <span data-ttu-id="382ae-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="382ae-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="382ae-158">1</span><span class="sxs-lookup"><span data-stu-id="382ae-158">1</span></span>     | <span data-ttu-id="382ae-159">/ИФД/ексиф/{ушорт = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="382ae-160">ushort</span><span class="sxs-lookup"><span data-stu-id="382ae-160">ushort</span></span>      |
| <span data-ttu-id="382ae-161">2</span><span class="sxs-lookup"><span data-stu-id="382ae-161">2</span></span>     | <span data-ttu-id="382ae-162">/ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="382ae-163">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-163">unicode</span></span>     |
| <span data-ttu-id="382ae-164">3</span><span class="sxs-lookup"><span data-stu-id="382ae-164">3</span></span>     | <span data-ttu-id="382ae-165">/ИФД/КСМП/ексиф: Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="382ae-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="382ae-167">Пути записи</span><span class="sxs-lookup"><span data-stu-id="382ae-167">Write Paths</span></span>



| <span data-ttu-id="382ae-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-168">Order</span></span> | <span data-ttu-id="382ae-169">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-169">Path</span></span>                                        | <span data-ttu-id="382ae-170">Формат диска</span><span class="sxs-lookup"><span data-stu-id="382ae-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="382ae-171">1</span><span class="sxs-lookup"><span data-stu-id="382ae-171">1</span></span>     | <span data-ttu-id="382ae-172">/ИФД/ексиф/{ушорт = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="382ae-173">ushort</span><span class="sxs-lookup"><span data-stu-id="382ae-173">ushort</span></span>      |
| <span data-ttu-id="382ae-174">2</span><span class="sxs-lookup"><span data-stu-id="382ae-174">2</span></span>     | <span data-ttu-id="382ae-175">/ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="382ae-176">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-176">unicode</span></span>     |
| <span data-ttu-id="382ae-177">3</span><span class="sxs-lookup"><span data-stu-id="382ae-177">3</span></span>     | <span data-ttu-id="382ae-178">/ИФД/КСМП/ексиф: Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="382ae-179">Юникод</span><span class="sxs-lookup"><span data-stu-id="382ae-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="382ae-180">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="382ae-180">Remove Paths</span></span>



| <span data-ttu-id="382ae-181">Заказ</span><span class="sxs-lookup"><span data-stu-id="382ae-181">Order</span></span> | <span data-ttu-id="382ae-182">Путь</span><span class="sxs-lookup"><span data-stu-id="382ae-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="382ae-183">1</span><span class="sxs-lookup"><span data-stu-id="382ae-183">1</span></span>     | <span data-ttu-id="382ae-184">/ИФД/ексиф/{ушорт = 34855}</span><span class="sxs-lookup"><span data-stu-id="382ae-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="382ae-185">2</span><span class="sxs-lookup"><span data-stu-id="382ae-185">2</span></span>     | <span data-ttu-id="382ae-186">/ИФД/КСМП/ <xmpseq> EXIF: исоспидратингс</span><span class="sxs-lookup"><span data-stu-id="382ae-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="382ae-187">3</span><span class="sxs-lookup"><span data-stu-id="382ae-187">3</span></span>     | <span data-ttu-id="382ae-188">/ИФД/КСМП/ексиф: исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="382ae-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="382ae-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="382ae-190">См. также</span><span class="sxs-lookup"><span data-stu-id="382ae-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="382ae-191">System. photo. Исоспид</span><span class="sxs-lookup"><span data-stu-id="382ae-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
