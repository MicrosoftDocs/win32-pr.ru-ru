---
description: Политика метаданных фотографии для свойства System. photo. контраста.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Политика метаданных фотографии System. photo. контраста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547042"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="005c9-103">Политика метаданных фотографии System. photo. контраста</span><span class="sxs-lookup"><span data-stu-id="005c9-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="005c9-104">Политика метаданных фотографии для свойства [System. photo. контраста](../properties/props-system-photo-contrast.md) .</span><span class="sxs-lookup"><span data-stu-id="005c9-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="005c9-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="005c9-105">PKEY</span></span>

<span data-ttu-id="005c9-106">\_Контрастность фото в PKEY \_</span><span class="sxs-lookup"><span data-stu-id="005c9-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="005c9-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="005c9-107">Containers</span></span>

<span data-ttu-id="005c9-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="005c9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="005c9-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="005c9-109">Read-Only</span></span>

<span data-ttu-id="005c9-110">Нет</span><span class="sxs-lookup"><span data-stu-id="005c9-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="005c9-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="005c9-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="005c9-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="005c9-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="005c9-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="005c9-113">Input Type</span></span>

<span data-ttu-id="005c9-114">UShort</span><span class="sxs-lookup"><span data-stu-id="005c9-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="005c9-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="005c9-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="005c9-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="005c9-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="005c9-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="005c9-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="005c9-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="005c9-118">Read Paths</span></span>



| <span data-ttu-id="005c9-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-119">Order</span></span> | <span data-ttu-id="005c9-120">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-120">Path</span></span>                          | <span data-ttu-id="005c9-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="005c9-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="005c9-122">1</span><span class="sxs-lookup"><span data-stu-id="005c9-122">1</span></span>     | <span data-ttu-id="005c9-123">/APP1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="005c9-124">ushort</span><span class="sxs-lookup"><span data-stu-id="005c9-124">ushort</span></span>      |
| <span data-ttu-id="005c9-125">2</span><span class="sxs-lookup"><span data-stu-id="005c9-125">2</span></span>     | <span data-ttu-id="005c9-126">/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="005c9-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="005c9-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="005c9-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="005c9-128">Write Paths</span></span>



| <span data-ttu-id="005c9-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-129">Order</span></span> | <span data-ttu-id="005c9-130">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-130">Path</span></span>                          | <span data-ttu-id="005c9-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="005c9-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="005c9-132">1</span><span class="sxs-lookup"><span data-stu-id="005c9-132">1</span></span>     | <span data-ttu-id="005c9-133">/APP1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="005c9-134">ushort</span><span class="sxs-lookup"><span data-stu-id="005c9-134">ushort</span></span>      |
| <span data-ttu-id="005c9-135">2</span><span class="sxs-lookup"><span data-stu-id="005c9-135">2</span></span>     | <span data-ttu-id="005c9-136">/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="005c9-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="005c9-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="005c9-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="005c9-138">Remove Paths</span></span>



| <span data-ttu-id="005c9-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-139">Order</span></span> | <span data-ttu-id="005c9-140">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="005c9-141">1</span><span class="sxs-lookup"><span data-stu-id="005c9-141">1</span></span>     | <span data-ttu-id="005c9-142">/APP1/IFD/EXIF/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="005c9-143">2</span><span class="sxs-lookup"><span data-stu-id="005c9-143">2</span></span>     | <span data-ttu-id="005c9-144">/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="005c9-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="005c9-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="005c9-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="005c9-146">Read Paths</span></span>



| <span data-ttu-id="005c9-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-147">Order</span></span> | <span data-ttu-id="005c9-148">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-148">Path</span></span>                     | <span data-ttu-id="005c9-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="005c9-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="005c9-150">1</span><span class="sxs-lookup"><span data-stu-id="005c9-150">1</span></span>     | <span data-ttu-id="005c9-151">/ИФД/ексиф/{ушорт = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="005c9-152">ushort</span><span class="sxs-lookup"><span data-stu-id="005c9-152">ushort</span></span>      |
| <span data-ttu-id="005c9-153">2</span><span class="sxs-lookup"><span data-stu-id="005c9-153">2</span></span>     | <span data-ttu-id="005c9-154">/ИФД/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="005c9-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="005c9-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="005c9-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="005c9-156">Write Paths</span></span>



| <span data-ttu-id="005c9-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-157">Order</span></span> | <span data-ttu-id="005c9-158">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-158">Path</span></span>                     | <span data-ttu-id="005c9-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="005c9-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="005c9-160">1</span><span class="sxs-lookup"><span data-stu-id="005c9-160">1</span></span>     | <span data-ttu-id="005c9-161">/ИФД/ексиф/{ушорт = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="005c9-162">ushort</span><span class="sxs-lookup"><span data-stu-id="005c9-162">ushort</span></span>      |
| <span data-ttu-id="005c9-163">2</span><span class="sxs-lookup"><span data-stu-id="005c9-163">2</span></span>     | <span data-ttu-id="005c9-164">/ИФД/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="005c9-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="005c9-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="005c9-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="005c9-166">Remove Paths</span></span>



| <span data-ttu-id="005c9-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="005c9-167">Order</span></span> | <span data-ttu-id="005c9-168">Путь</span><span class="sxs-lookup"><span data-stu-id="005c9-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="005c9-169">1</span><span class="sxs-lookup"><span data-stu-id="005c9-169">1</span></span>     | <span data-ttu-id="005c9-170">/ИФД/ексиф/{ушорт = 41992}</span><span class="sxs-lookup"><span data-stu-id="005c9-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="005c9-171">2</span><span class="sxs-lookup"><span data-stu-id="005c9-171">2</span></span>     | <span data-ttu-id="005c9-172">/ИФД/КСМП/ексиф: контрастность</span><span class="sxs-lookup"><span data-stu-id="005c9-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="005c9-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="005c9-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="005c9-174">См. также</span><span class="sxs-lookup"><span data-stu-id="005c9-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="005c9-175">System. photo. контраст</span><span class="sxs-lookup"><span data-stu-id="005c9-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
