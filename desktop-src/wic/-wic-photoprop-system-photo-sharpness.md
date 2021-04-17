---
description: Политика метаданных фотографии для свойства System. photo. четкости.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Политика метаданных фотографии System. photo. резкость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674129"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="6a83c-103">Политика метаданных фотографии System. photo. резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="6a83c-104">Политика метаданных фотографии для свойства [System. photo. четкости](../properties/props-system-photo-sharpness.md) .</span><span class="sxs-lookup"><span data-stu-id="6a83c-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6a83c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6a83c-105">PKEY</span></span>

<span data-ttu-id="6a83c-106">\_Четкость фото в PKEY \_</span><span class="sxs-lookup"><span data-stu-id="6a83c-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="6a83c-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="6a83c-107">Containers</span></span>

<span data-ttu-id="6a83c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6a83c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6a83c-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="6a83c-109">Read-Only</span></span>

<span data-ttu-id="6a83c-110">Нет</span><span class="sxs-lookup"><span data-stu-id="6a83c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6a83c-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="6a83c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6a83c-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6a83c-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="6a83c-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="6a83c-113">Input Type</span></span>

<span data-ttu-id="6a83c-114">UShort</span><span class="sxs-lookup"><span data-stu-id="6a83c-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6a83c-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="6a83c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6a83c-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="6a83c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6a83c-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="6a83c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a83c-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="6a83c-118">Read Paths</span></span>



| <span data-ttu-id="6a83c-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-119">Order</span></span> | <span data-ttu-id="6a83c-120">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-120">Path</span></span>                          | <span data-ttu-id="6a83c-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="6a83c-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6a83c-122">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-122">1</span></span>     | <span data-ttu-id="6a83c-123">/APP1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="6a83c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="6a83c-124">ushort</span></span>      |
| <span data-ttu-id="6a83c-125">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-125">2</span></span>     | <span data-ttu-id="6a83c-126">/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="6a83c-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="6a83c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6a83c-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="6a83c-128">Write Paths</span></span>



| <span data-ttu-id="6a83c-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-129">Order</span></span> | <span data-ttu-id="6a83c-130">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-130">Path</span></span>                          | <span data-ttu-id="6a83c-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="6a83c-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6a83c-132">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-132">1</span></span>     | <span data-ttu-id="6a83c-133">/APP1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="6a83c-134">ushort</span><span class="sxs-lookup"><span data-stu-id="6a83c-134">ushort</span></span>      |
| <span data-ttu-id="6a83c-135">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-135">2</span></span>     | <span data-ttu-id="6a83c-136">/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="6a83c-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="6a83c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6a83c-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="6a83c-138">Remove Paths</span></span>



| <span data-ttu-id="6a83c-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-139">Order</span></span> | <span data-ttu-id="6a83c-140">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6a83c-141">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-141">1</span></span>     | <span data-ttu-id="6a83c-142">/APP1/IFD/EXIF/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="6a83c-143">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-143">2</span></span>     | <span data-ttu-id="6a83c-144">/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="6a83c-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="6a83c-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a83c-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="6a83c-146">Read Paths</span></span>



| <span data-ttu-id="6a83c-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-147">Order</span></span> | <span data-ttu-id="6a83c-148">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-148">Path</span></span>                     | <span data-ttu-id="6a83c-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="6a83c-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a83c-150">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-150">1</span></span>     | <span data-ttu-id="6a83c-151">/ИФД/ексиф/{ушорт = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="6a83c-152">ushort</span><span class="sxs-lookup"><span data-stu-id="6a83c-152">ushort</span></span>      |
| <span data-ttu-id="6a83c-153">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-153">2</span></span>     | <span data-ttu-id="6a83c-154">/ИФД/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="6a83c-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="6a83c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6a83c-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="6a83c-156">Write Paths</span></span>



| <span data-ttu-id="6a83c-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-157">Order</span></span> | <span data-ttu-id="6a83c-158">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-158">Path</span></span>                     | <span data-ttu-id="6a83c-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="6a83c-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a83c-160">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-160">1</span></span>     | <span data-ttu-id="6a83c-161">/ИФД/ексиф/{ушорт = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="6a83c-162">ushort</span><span class="sxs-lookup"><span data-stu-id="6a83c-162">ushort</span></span>      |
| <span data-ttu-id="6a83c-163">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-163">2</span></span>     | <span data-ttu-id="6a83c-164">/ИФД/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="6a83c-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="6a83c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6a83c-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="6a83c-166">Remove Paths</span></span>



| <span data-ttu-id="6a83c-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="6a83c-167">Order</span></span> | <span data-ttu-id="6a83c-168">Путь</span><span class="sxs-lookup"><span data-stu-id="6a83c-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6a83c-169">1</span><span class="sxs-lookup"><span data-stu-id="6a83c-169">1</span></span>     | <span data-ttu-id="6a83c-170">/ИФД/ексиф/{ушорт = 41994}</span><span class="sxs-lookup"><span data-stu-id="6a83c-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="6a83c-171">2</span><span class="sxs-lookup"><span data-stu-id="6a83c-171">2</span></span>     | <span data-ttu-id="6a83c-172">/ИФД/КСМП/ексиф: резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="6a83c-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a83c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a83c-174">См. также</span><span class="sxs-lookup"><span data-stu-id="6a83c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a83c-175">System. photo. резкость</span><span class="sxs-lookup"><span data-stu-id="6a83c-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
