---
description: Политика метаданных фотографии для свойства System. photo. насыщенности.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Политика метаданных фотографии System. photo. насыщенности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081304"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="e6494-103">Политика метаданных фотографии System. photo. насыщенности</span><span class="sxs-lookup"><span data-stu-id="e6494-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="e6494-104">Политика метаданных фотографии для свойства [System. photo. насыщенности](../properties/props-system-photo-saturation.md) .</span><span class="sxs-lookup"><span data-stu-id="e6494-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e6494-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e6494-105">PKEY</span></span>

<span data-ttu-id="e6494-106">\_ \_ Насыщенность фото PKEY</span><span class="sxs-lookup"><span data-stu-id="e6494-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="e6494-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e6494-107">Containers</span></span>

<span data-ttu-id="e6494-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e6494-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e6494-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e6494-109">Read-Only</span></span>

<span data-ttu-id="e6494-110">Нет</span><span class="sxs-lookup"><span data-stu-id="e6494-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e6494-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e6494-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e6494-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e6494-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="e6494-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="e6494-113">Input Type</span></span>

<span data-ttu-id="e6494-114">UShort</span><span class="sxs-lookup"><span data-stu-id="e6494-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e6494-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e6494-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e6494-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e6494-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e6494-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="e6494-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e6494-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e6494-118">Read Paths</span></span>



| <span data-ttu-id="e6494-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-119">Order</span></span> | <span data-ttu-id="e6494-120">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-120">Path</span></span>                          | <span data-ttu-id="e6494-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e6494-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e6494-122">1</span><span class="sxs-lookup"><span data-stu-id="e6494-122">1</span></span>     | <span data-ttu-id="e6494-123">/APP1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="e6494-124">ushort</span><span class="sxs-lookup"><span data-stu-id="e6494-124">ushort</span></span>      |
| <span data-ttu-id="e6494-125">2</span><span class="sxs-lookup"><span data-stu-id="e6494-125">2</span></span>     | <span data-ttu-id="e6494-126">/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="e6494-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="e6494-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e6494-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e6494-128">Write Paths</span></span>



| <span data-ttu-id="e6494-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-129">Order</span></span> | <span data-ttu-id="e6494-130">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-130">Path</span></span>                          | <span data-ttu-id="e6494-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e6494-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e6494-132">1</span><span class="sxs-lookup"><span data-stu-id="e6494-132">1</span></span>     | <span data-ttu-id="e6494-133">/APP1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="e6494-134">ushort</span><span class="sxs-lookup"><span data-stu-id="e6494-134">ushort</span></span>      |
| <span data-ttu-id="e6494-135">2</span><span class="sxs-lookup"><span data-stu-id="e6494-135">2</span></span>     | <span data-ttu-id="e6494-136">/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="e6494-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="e6494-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e6494-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e6494-138">Remove Paths</span></span>



| <span data-ttu-id="e6494-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-139">Order</span></span> | <span data-ttu-id="e6494-140">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e6494-141">1</span><span class="sxs-lookup"><span data-stu-id="e6494-141">1</span></span>     | <span data-ttu-id="e6494-142">/APP1/IFD/EXIF/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="e6494-143">2</span><span class="sxs-lookup"><span data-stu-id="e6494-143">2</span></span>     | <span data-ttu-id="e6494-144">/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="e6494-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="e6494-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e6494-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e6494-146">Read Paths</span></span>



| <span data-ttu-id="e6494-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-147">Order</span></span> | <span data-ttu-id="e6494-148">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-148">Path</span></span>                     | <span data-ttu-id="e6494-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e6494-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e6494-150">1</span><span class="sxs-lookup"><span data-stu-id="e6494-150">1</span></span>     | <span data-ttu-id="e6494-151">/ИФД/ексиф/{ушорт = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="e6494-152">ushort</span><span class="sxs-lookup"><span data-stu-id="e6494-152">ushort</span></span>      |
| <span data-ttu-id="e6494-153">2</span><span class="sxs-lookup"><span data-stu-id="e6494-153">2</span></span>     | <span data-ttu-id="e6494-154">/ИФД/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="e6494-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="e6494-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e6494-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e6494-156">Write Paths</span></span>



| <span data-ttu-id="e6494-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-157">Order</span></span> | <span data-ttu-id="e6494-158">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-158">Path</span></span>                     | <span data-ttu-id="e6494-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e6494-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="e6494-160">1</span><span class="sxs-lookup"><span data-stu-id="e6494-160">1</span></span>     | <span data-ttu-id="e6494-161">/ИФД/ексиф/{ушорт = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="e6494-162">ushort</span><span class="sxs-lookup"><span data-stu-id="e6494-162">ushort</span></span>      |
| <span data-ttu-id="e6494-163">2</span><span class="sxs-lookup"><span data-stu-id="e6494-163">2</span></span>     | <span data-ttu-id="e6494-164">/ИФД/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="e6494-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="e6494-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e6494-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e6494-166">Remove Paths</span></span>



| <span data-ttu-id="e6494-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="e6494-167">Order</span></span> | <span data-ttu-id="e6494-168">Путь</span><span class="sxs-lookup"><span data-stu-id="e6494-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="e6494-169">1</span><span class="sxs-lookup"><span data-stu-id="e6494-169">1</span></span>     | <span data-ttu-id="e6494-170">/ИФД/ексиф/{ушорт = 41993}</span><span class="sxs-lookup"><span data-stu-id="e6494-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="e6494-171">2</span><span class="sxs-lookup"><span data-stu-id="e6494-171">2</span></span>     | <span data-ttu-id="e6494-172">/ИФД/КСМП/ексиф: насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e6494-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6494-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6494-174">См. также</span><span class="sxs-lookup"><span data-stu-id="e6494-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6494-175">System. photo. насыщенность</span><span class="sxs-lookup"><span data-stu-id="e6494-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
