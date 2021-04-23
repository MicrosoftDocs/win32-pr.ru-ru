---
description: Политика метаданных фотографии для свойства System. photo. Ексифверсион.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Политика метаданных фото для System. photo. Ексифверсион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272092"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="627e7-103">Политика метаданных фото для System. photo. Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="627e7-104">Политика метаданных фотографии для свойства [System. photo. ексифверсион](../properties/props-system-photo-exifversion.md) .</span><span class="sxs-lookup"><span data-stu-id="627e7-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="627e7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="627e7-105">PKEY</span></span>

<span data-ttu-id="627e7-106">\_Ексифверсион фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="627e7-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="627e7-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="627e7-107">Containers</span></span>

<span data-ttu-id="627e7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="627e7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="627e7-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="627e7-109">Read-Only</span></span>

<span data-ttu-id="627e7-110">Нет</span><span class="sxs-lookup"><span data-stu-id="627e7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="627e7-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="627e7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="627e7-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="627e7-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="627e7-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="627e7-113">Input Type</span></span>

<span data-ttu-id="627e7-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="627e7-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="627e7-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="627e7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="627e7-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="627e7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="627e7-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="627e7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="627e7-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="627e7-118">Read Paths</span></span>



| <span data-ttu-id="627e7-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-119">Order</span></span> | <span data-ttu-id="627e7-120">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-120">Path</span></span>                          | <span data-ttu-id="627e7-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="627e7-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="627e7-122">1</span><span class="sxs-lookup"><span data-stu-id="627e7-122">1</span></span>     | <span data-ttu-id="627e7-123">/APP1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="627e7-124">\_версия EXIF</span><span class="sxs-lookup"><span data-stu-id="627e7-124">exif\_version</span></span> |
| <span data-ttu-id="627e7-125">2</span><span class="sxs-lookup"><span data-stu-id="627e7-125">2</span></span>     | <span data-ttu-id="627e7-126">/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="627e7-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="627e7-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="627e7-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="627e7-128">Write Paths</span></span>



| <span data-ttu-id="627e7-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-129">Order</span></span> | <span data-ttu-id="627e7-130">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-130">Path</span></span>                          | <span data-ttu-id="627e7-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="627e7-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="627e7-132">1</span><span class="sxs-lookup"><span data-stu-id="627e7-132">1</span></span>     | <span data-ttu-id="627e7-133">/APP1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="627e7-134">\_версия EXIF</span><span class="sxs-lookup"><span data-stu-id="627e7-134">exif\_version</span></span> |
| <span data-ttu-id="627e7-135">2</span><span class="sxs-lookup"><span data-stu-id="627e7-135">2</span></span>     | <span data-ttu-id="627e7-136">/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="627e7-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="627e7-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="627e7-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="627e7-138">Remove Paths</span></span>



| <span data-ttu-id="627e7-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-139">Order</span></span> | <span data-ttu-id="627e7-140">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="627e7-141">1</span><span class="sxs-lookup"><span data-stu-id="627e7-141">1</span></span>     | <span data-ttu-id="627e7-142">/APP1/IFD/EXIF/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="627e7-143">2</span><span class="sxs-lookup"><span data-stu-id="627e7-143">2</span></span>     | <span data-ttu-id="627e7-144">/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="627e7-145">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="627e7-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="627e7-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="627e7-146">Read Paths</span></span>



| <span data-ttu-id="627e7-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-147">Order</span></span> | <span data-ttu-id="627e7-148">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-148">Path</span></span>                      | <span data-ttu-id="627e7-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="627e7-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="627e7-150">1</span><span class="sxs-lookup"><span data-stu-id="627e7-150">1</span></span>     | <span data-ttu-id="627e7-151">/ИФД/ексиф/{ушорт = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="627e7-152">\_версия EXIF</span><span class="sxs-lookup"><span data-stu-id="627e7-152">exif\_version</span></span> |
| <span data-ttu-id="627e7-153">2</span><span class="sxs-lookup"><span data-stu-id="627e7-153">2</span></span>     | <span data-ttu-id="627e7-154">/ИФД/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="627e7-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="627e7-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="627e7-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="627e7-156">Write Paths</span></span>



| <span data-ttu-id="627e7-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-157">Order</span></span> | <span data-ttu-id="627e7-158">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-158">Path</span></span>                      | <span data-ttu-id="627e7-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="627e7-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="627e7-160">1</span><span class="sxs-lookup"><span data-stu-id="627e7-160">1</span></span>     | <span data-ttu-id="627e7-161">/ИФД/ексиф/{ушорт = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="627e7-162">\_версия EXIF</span><span class="sxs-lookup"><span data-stu-id="627e7-162">exif\_version</span></span> |
| <span data-ttu-id="627e7-163">2</span><span class="sxs-lookup"><span data-stu-id="627e7-163">2</span></span>     | <span data-ttu-id="627e7-164">/ИФД/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="627e7-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="627e7-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="627e7-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="627e7-166">Remove Paths</span></span>



| <span data-ttu-id="627e7-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="627e7-167">Order</span></span> | <span data-ttu-id="627e7-168">Путь</span><span class="sxs-lookup"><span data-stu-id="627e7-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="627e7-169">1</span><span class="sxs-lookup"><span data-stu-id="627e7-169">1</span></span>     | <span data-ttu-id="627e7-170">/ИФД/ексиф/{ушорт = 36864}</span><span class="sxs-lookup"><span data-stu-id="627e7-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="627e7-171">2</span><span class="sxs-lookup"><span data-stu-id="627e7-171">2</span></span>     | <span data-ttu-id="627e7-172">/ИФД/КСМП/ексиф: Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="627e7-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="627e7-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="627e7-174">См. также</span><span class="sxs-lookup"><span data-stu-id="627e7-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="627e7-175">System. photo. Ексифверсион</span><span class="sxs-lookup"><span data-stu-id="627e7-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
