---
description: Политика метаданных фотографии для свойства System. Image. Имажеид.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Политика метаданных фотографии System. Image. Имажеид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545719"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="8fc6a-103">Политика метаданных фотографии System. Image. Имажеид</span><span class="sxs-lookup"><span data-stu-id="8fc6a-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="8fc6a-104">Политика метаданных фотографии для свойства [System. Image. имажеид](../properties/props-system-image-imageid.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc6a-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8fc6a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8fc6a-105">PKEY</span></span>

<span data-ttu-id="8fc6a-106">\_Имажеид образа \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="8fc6a-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="8fc6a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="8fc6a-107">Containers</span></span>

<span data-ttu-id="8fc6a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8fc6a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8fc6a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8fc6a-109">Read-Only</span></span>

<span data-ttu-id="8fc6a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="8fc6a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8fc6a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8fc6a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8fc6a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="8fc6a-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="8fc6a-113">Input Type</span></span>

<span data-ttu-id="8fc6a-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="8fc6a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8fc6a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="8fc6a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8fc6a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="8fc6a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8fc6a-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="8fc6a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8fc6a-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8fc6a-118">Read Paths</span></span>



| <span data-ttu-id="8fc6a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-119">Order</span></span> | <span data-ttu-id="8fc6a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-120">Path</span></span>                          | <span data-ttu-id="8fc6a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8fc6a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8fc6a-122">1</span><span class="sxs-lookup"><span data-stu-id="8fc6a-122">1</span></span>     | <span data-ttu-id="8fc6a-123">/APP1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="8fc6a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="8fc6a-124">ascii</span></span>       |
| <span data-ttu-id="8fc6a-125">2</span><span class="sxs-lookup"><span data-stu-id="8fc6a-125">2</span></span>     | <span data-ttu-id="8fc6a-126">/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="8fc6a-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="8fc6a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8fc6a-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8fc6a-128">Write Paths</span></span>



| <span data-ttu-id="8fc6a-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-129">Order</span></span> | <span data-ttu-id="8fc6a-130">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-130">Path</span></span>                          | <span data-ttu-id="8fc6a-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8fc6a-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8fc6a-132">1</span><span class="sxs-lookup"><span data-stu-id="8fc6a-132">1</span></span>     | <span data-ttu-id="8fc6a-133">/APP1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="8fc6a-134">ascii</span><span class="sxs-lookup"><span data-stu-id="8fc6a-134">ascii</span></span>       |
| <span data-ttu-id="8fc6a-135">2</span><span class="sxs-lookup"><span data-stu-id="8fc6a-135">2</span></span>     | <span data-ttu-id="8fc6a-136">/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="8fc6a-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="8fc6a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8fc6a-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8fc6a-138">Remove Paths</span></span>



| <span data-ttu-id="8fc6a-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-139">Order</span></span> | <span data-ttu-id="8fc6a-140">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8fc6a-141">1</span><span class="sxs-lookup"><span data-stu-id="8fc6a-141">1</span></span>     | <span data-ttu-id="8fc6a-142">/APP1/IFD/EXIF/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="8fc6a-143">2</span><span class="sxs-lookup"><span data-stu-id="8fc6a-143">2</span></span>     | <span data-ttu-id="8fc6a-144">/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="8fc6a-145">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="8fc6a-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8fc6a-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8fc6a-146">Read Paths</span></span>



| <span data-ttu-id="8fc6a-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-147">Order</span></span> | <span data-ttu-id="8fc6a-148">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-148">Path</span></span>                        | <span data-ttu-id="8fc6a-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8fc6a-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="8fc6a-150">/ИФД/ексиф/{ушорт = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="8fc6a-151">ascii</span><span class="sxs-lookup"><span data-stu-id="8fc6a-151">ascii</span></span>       |
|       | <span data-ttu-id="8fc6a-152">/ИФД/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="8fc6a-153">Юникод</span><span class="sxs-lookup"><span data-stu-id="8fc6a-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8fc6a-154">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8fc6a-154">Write Paths</span></span>



| <span data-ttu-id="8fc6a-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-155">Order</span></span> | <span data-ttu-id="8fc6a-156">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-156">Path</span></span>                        | <span data-ttu-id="8fc6a-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8fc6a-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="8fc6a-158">/ИФД/ексиф/{ушорт = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="8fc6a-159">ascii</span><span class="sxs-lookup"><span data-stu-id="8fc6a-159">ascii</span></span>       |
|       | <span data-ttu-id="8fc6a-160">/ИФД/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="8fc6a-161">Юникод</span><span class="sxs-lookup"><span data-stu-id="8fc6a-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8fc6a-162">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8fc6a-162">Remove Paths</span></span>



| <span data-ttu-id="8fc6a-163">Заказ</span><span class="sxs-lookup"><span data-stu-id="8fc6a-163">Order</span></span> | <span data-ttu-id="8fc6a-164">Путь</span><span class="sxs-lookup"><span data-stu-id="8fc6a-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="8fc6a-165">/ИФД/ексиф/{ушорт = 42016}</span><span class="sxs-lookup"><span data-stu-id="8fc6a-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="8fc6a-166">/ИФД/КСМП/ексиф: Imageuniqueid)</span><span class="sxs-lookup"><span data-stu-id="8fc6a-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8fc6a-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fc6a-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fc6a-168">См. также</span><span class="sxs-lookup"><span data-stu-id="8fc6a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc6a-169">System. Image. Имажеид</span><span class="sxs-lookup"><span data-stu-id="8fc6a-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
