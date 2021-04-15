---
description: Политика метаданных фотографии для свойства System. photo. Фокалленгсинфилм.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Политика метаданных фото для System. photo. Фокалленгсинфилм
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498030"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="dcdf2-103">Политика метаданных фото для System. photo. Фокалленгсинфилм</span><span class="sxs-lookup"><span data-stu-id="dcdf2-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="dcdf2-104">Политика метаданных фотографии для свойства [System. photo. фокалленгсинфилм](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="dcdf2-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="dcdf2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="dcdf2-105">PKEY</span></span>

<span data-ttu-id="dcdf2-106">PKEY \_ фокалленгсинфилм</span><span class="sxs-lookup"><span data-stu-id="dcdf2-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="dcdf2-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="dcdf2-107">Containers</span></span>

<span data-ttu-id="dcdf2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="dcdf2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="dcdf2-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="dcdf2-109">Read-Only</span></span>

<span data-ttu-id="dcdf2-110">Нет</span><span class="sxs-lookup"><span data-stu-id="dcdf2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="dcdf2-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="dcdf2-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="dcdf2-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="dcdf2-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="dcdf2-113">Input Type</span></span>

<span data-ttu-id="dcdf2-114">UShort</span><span class="sxs-lookup"><span data-stu-id="dcdf2-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="dcdf2-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="dcdf2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="dcdf2-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="dcdf2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="dcdf2-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="dcdf2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="dcdf2-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="dcdf2-118">Read Paths</span></span>



| <span data-ttu-id="dcdf2-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-119">Order</span></span> | <span data-ttu-id="dcdf2-120">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-120">Path</span></span>                            | <span data-ttu-id="dcdf2-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dcdf2-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="dcdf2-122">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-122">1</span></span>     | <span data-ttu-id="dcdf2-123">/APP1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="dcdf2-124">ushort</span><span class="sxs-lookup"><span data-stu-id="dcdf2-124">ushort</span></span>      |
| <span data-ttu-id="dcdf2-125">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-125">2</span></span>     | <span data-ttu-id="dcdf2-126">/КСМП/ексиф: FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="dcdf2-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="dcdf2-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="dcdf2-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="dcdf2-128">Write Paths</span></span>



| <span data-ttu-id="dcdf2-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-129">Order</span></span> | <span data-ttu-id="dcdf2-130">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-130">Path</span></span>                            | <span data-ttu-id="dcdf2-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dcdf2-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="dcdf2-132">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-132">1</span></span>     | <span data-ttu-id="dcdf2-133">/APP1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="dcdf2-134">ushort</span><span class="sxs-lookup"><span data-stu-id="dcdf2-134">ushort</span></span>      |
| <span data-ttu-id="dcdf2-135">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-135">2</span></span>     | <span data-ttu-id="dcdf2-136">/КСМП/ексиф: FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="dcdf2-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="dcdf2-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="dcdf2-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="dcdf2-138">Remove Paths</span></span>



| <span data-ttu-id="dcdf2-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-139">Order</span></span> | <span data-ttu-id="dcdf2-140">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="dcdf2-141">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-141">1</span></span>     | <span data-ttu-id="dcdf2-142">/APP1/IFD/EXIF/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="dcdf2-143">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-143">2</span></span>     | <span data-ttu-id="dcdf2-144">/КСМП/ексиф: focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="dcdf2-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="dcdf2-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="dcdf2-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="dcdf2-146">Read Paths</span></span>



| <span data-ttu-id="dcdf2-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-147">Order</span></span> | <span data-ttu-id="dcdf2-148">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-148">Path</span></span>                                | <span data-ttu-id="dcdf2-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dcdf2-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="dcdf2-150">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-150">1</span></span>     | <span data-ttu-id="dcdf2-151">/ИФД/ексиф/{ушорт = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="dcdf2-152">ushort</span><span class="sxs-lookup"><span data-stu-id="dcdf2-152">ushort</span></span>      |
| <span data-ttu-id="dcdf2-153">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-153">2</span></span>     | <span data-ttu-id="dcdf2-154">/ИФД/КСМП/ексиф: FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="dcdf2-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="dcdf2-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="dcdf2-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="dcdf2-156">Write Paths</span></span>



| <span data-ttu-id="dcdf2-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-157">Order</span></span> | <span data-ttu-id="dcdf2-158">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-158">Path</span></span>                                | <span data-ttu-id="dcdf2-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="dcdf2-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="dcdf2-160">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-160">1</span></span>     | <span data-ttu-id="dcdf2-161">/ИФД/ексиф/{ушорт = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="dcdf2-162">ushort</span><span class="sxs-lookup"><span data-stu-id="dcdf2-162">ushort</span></span>      |
| <span data-ttu-id="dcdf2-163">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-163">2</span></span>     | <span data-ttu-id="dcdf2-164">/ИФД/КСМП/ексиф: FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="dcdf2-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="dcdf2-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="dcdf2-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="dcdf2-166">Remove Paths</span></span>



| <span data-ttu-id="dcdf2-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="dcdf2-167">Order</span></span> | <span data-ttu-id="dcdf2-168">Путь</span><span class="sxs-lookup"><span data-stu-id="dcdf2-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="dcdf2-169">1</span><span class="sxs-lookup"><span data-stu-id="dcdf2-169">1</span></span>     | <span data-ttu-id="dcdf2-170">/ИФД/ексиф/{ушорт = 41989}</span><span class="sxs-lookup"><span data-stu-id="dcdf2-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="dcdf2-171">2</span><span class="sxs-lookup"><span data-stu-id="dcdf2-171">2</span></span>     | <span data-ttu-id="dcdf2-172">/ИФД/КСМП/ексиф: focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="dcdf2-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dcdf2-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcdf2-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcdf2-174">См. также</span><span class="sxs-lookup"><span data-stu-id="dcdf2-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcdf2-175">System. photo. Фокалленгсинфилм</span><span class="sxs-lookup"><span data-stu-id="dcdf2-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
