---
description: Политика метаданных фотографии для свойства System. Image. Колорспаце.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Политика метаданных фотографии System. Image. Колорспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702311"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="c1b37-103">Политика метаданных фотографии System. Image. Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="c1b37-104">Политика метаданных фотографии для свойства [System. Image. колорспаце](../properties/props-system-image-colorspace.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b37-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c1b37-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c1b37-105">PKEY</span></span>

<span data-ttu-id="c1b37-106">\_Колорспаце образа \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="c1b37-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="c1b37-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="c1b37-107">Containers</span></span>

<span data-ttu-id="c1b37-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c1b37-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c1b37-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1b37-109">Read-Only</span></span>

<span data-ttu-id="c1b37-110">Да</span><span class="sxs-lookup"><span data-stu-id="c1b37-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c1b37-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="c1b37-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c1b37-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="c1b37-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="c1b37-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="c1b37-113">Input Type</span></span>

<span data-ttu-id="c1b37-114">UShort</span><span class="sxs-lookup"><span data-stu-id="c1b37-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c1b37-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="c1b37-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c1b37-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="c1b37-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c1b37-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="c1b37-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c1b37-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c1b37-118">Read Paths</span></span>



| <span data-ttu-id="c1b37-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-119">Order</span></span> | <span data-ttu-id="c1b37-120">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-120">Path</span></span>                          | <span data-ttu-id="c1b37-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c1b37-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c1b37-122">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-122">1</span></span>     | <span data-ttu-id="c1b37-123">/APP1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="c1b37-124">ushort</span><span class="sxs-lookup"><span data-stu-id="c1b37-124">ushort</span></span>      |
| <span data-ttu-id="c1b37-125">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-125">2</span></span>     | <span data-ttu-id="c1b37-126">/КСМП/ексиф: Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="c1b37-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="c1b37-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c1b37-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c1b37-128">Write Paths</span></span>



| <span data-ttu-id="c1b37-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-129">Order</span></span> | <span data-ttu-id="c1b37-130">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-130">Path</span></span>                          | <span data-ttu-id="c1b37-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c1b37-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c1b37-132">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-132">1</span></span>     | <span data-ttu-id="c1b37-133">/APP1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="c1b37-134">ushort</span><span class="sxs-lookup"><span data-stu-id="c1b37-134">ushort</span></span>      |
| <span data-ttu-id="c1b37-135">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-135">2</span></span>     | <span data-ttu-id="c1b37-136">/КСМП/ексиф: Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="c1b37-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="c1b37-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c1b37-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c1b37-138">Remove Paths</span></span>



| <span data-ttu-id="c1b37-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-139">Order</span></span> | <span data-ttu-id="c1b37-140">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c1b37-141">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-141">1</span></span>     | <span data-ttu-id="c1b37-142">/APP1/IFD/EXIF/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="c1b37-143">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-143">2</span></span>     | <span data-ttu-id="c1b37-144">/КСМП/ексиф: колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="c1b37-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="c1b37-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c1b37-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c1b37-146">Read Paths</span></span>



| <span data-ttu-id="c1b37-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-147">Order</span></span> | <span data-ttu-id="c1b37-148">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-148">Path</span></span>                     | <span data-ttu-id="c1b37-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c1b37-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c1b37-150">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-150">1</span></span>     | <span data-ttu-id="c1b37-151">/ИФД/ексиф/{ушорт = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="c1b37-152">ushort</span><span class="sxs-lookup"><span data-stu-id="c1b37-152">ushort</span></span>      |
| <span data-ttu-id="c1b37-153">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-153">2</span></span>     | <span data-ttu-id="c1b37-154">/ИФД/КСМП/ексиф: Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="c1b37-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="c1b37-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c1b37-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c1b37-156">Write Paths</span></span>



| <span data-ttu-id="c1b37-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-157">Order</span></span> | <span data-ttu-id="c1b37-158">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-158">Path</span></span>                     | <span data-ttu-id="c1b37-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c1b37-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c1b37-160">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-160">1</span></span>     | <span data-ttu-id="c1b37-161">/ИФД/ексиф/{ушорт = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="c1b37-162">ushort</span><span class="sxs-lookup"><span data-stu-id="c1b37-162">ushort</span></span>      |
| <span data-ttu-id="c1b37-163">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-163">2</span></span>     | <span data-ttu-id="c1b37-164">/ИФД/КСМП/ексиф: Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="c1b37-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="c1b37-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c1b37-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c1b37-166">Remove Paths</span></span>



| <span data-ttu-id="c1b37-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="c1b37-167">Order</span></span> | <span data-ttu-id="c1b37-168">Путь</span><span class="sxs-lookup"><span data-stu-id="c1b37-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c1b37-169">1</span><span class="sxs-lookup"><span data-stu-id="c1b37-169">1</span></span>     | <span data-ttu-id="c1b37-170">/ИФД/ексиф/{ушорт = 40961}</span><span class="sxs-lookup"><span data-stu-id="c1b37-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="c1b37-171">2</span><span class="sxs-lookup"><span data-stu-id="c1b37-171">2</span></span>     | <span data-ttu-id="c1b37-172">/ИФД/КСМП/ексиф: колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1b37-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1b37-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1b37-174">См. также</span><span class="sxs-lookup"><span data-stu-id="c1b37-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b37-175">System. Image. Колорспаце</span><span class="sxs-lookup"><span data-stu-id="c1b37-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
