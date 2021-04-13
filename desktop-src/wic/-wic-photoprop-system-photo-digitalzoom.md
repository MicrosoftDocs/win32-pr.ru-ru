---
description: Политика метаданных фотографии для свойства System. photo. Дигиталзум.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Политика метаданных фото для System. photo. Дигиталзум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347425"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="8283f-103">Политика метаданных фото для System. photo. Дигиталзум</span><span class="sxs-lookup"><span data-stu-id="8283f-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="8283f-104">Политика метаданных фотографии для свойства [System. photo. дигиталзум](../properties/props-system-photo-digitalzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="8283f-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8283f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8283f-105">PKEY</span></span>

<span data-ttu-id="8283f-106">\_Дигиталзум фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="8283f-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="8283f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="8283f-107">Containers</span></span>

<span data-ttu-id="8283f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8283f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8283f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8283f-109">Read-Only</span></span>

<span data-ttu-id="8283f-110">Да</span><span class="sxs-lookup"><span data-stu-id="8283f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8283f-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="8283f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8283f-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="8283f-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8283f-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="8283f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="8283f-114">Это значение формируется из System. photo. Дигиталзумнумератор и System. photo. Дигиталзумденоминатор.</span><span class="sxs-lookup"><span data-stu-id="8283f-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="8283f-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="8283f-115">It cannot be written directly.</span></span> <span data-ttu-id="8283f-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="8283f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8283f-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="8283f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8283f-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8283f-118">Read Paths</span></span>



| <span data-ttu-id="8283f-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-119">Order</span></span> | <span data-ttu-id="8283f-120">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-120">Path</span></span>                          | <span data-ttu-id="8283f-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8283f-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8283f-122">1</span><span class="sxs-lookup"><span data-stu-id="8283f-122">1</span></span>     | <span data-ttu-id="8283f-123">/APP1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="8283f-124">2</span><span class="sxs-lookup"><span data-stu-id="8283f-124">2</span></span>     | <span data-ttu-id="8283f-125">/КСМП/ексиф: Дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="8283f-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8283f-126">Write Paths</span></span>



| <span data-ttu-id="8283f-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-127">Order</span></span> | <span data-ttu-id="8283f-128">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-128">Path</span></span>                          | <span data-ttu-id="8283f-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8283f-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8283f-130">1</span><span class="sxs-lookup"><span data-stu-id="8283f-130">1</span></span>     | <span data-ttu-id="8283f-131">/APP1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="8283f-132">2</span><span class="sxs-lookup"><span data-stu-id="8283f-132">2</span></span>     | <span data-ttu-id="8283f-133">/КСМП/ексиф: Дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8283f-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8283f-134">Remove Paths</span></span>



| <span data-ttu-id="8283f-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-135">Order</span></span> | <span data-ttu-id="8283f-136">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8283f-137">1</span><span class="sxs-lookup"><span data-stu-id="8283f-137">1</span></span>     | <span data-ttu-id="8283f-138">/APP1/IFD/EXIF/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="8283f-139">2</span><span class="sxs-lookup"><span data-stu-id="8283f-139">2</span></span>     | <span data-ttu-id="8283f-140">/КСМП/ексиф: дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="8283f-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="8283f-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8283f-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8283f-142">Read Paths</span></span>



| <span data-ttu-id="8283f-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-143">Order</span></span> | <span data-ttu-id="8283f-144">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-144">Path</span></span>                           | <span data-ttu-id="8283f-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8283f-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="8283f-146">1</span><span class="sxs-lookup"><span data-stu-id="8283f-146">1</span></span>     | <span data-ttu-id="8283f-147">/ИФД/ексиф/{ушорт = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="8283f-148">2</span><span class="sxs-lookup"><span data-stu-id="8283f-148">2</span></span>     | <span data-ttu-id="8283f-149">/ИФД/КСМП/ексиф: Дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8283f-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8283f-150">Write Paths</span></span>



| <span data-ttu-id="8283f-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-151">Order</span></span> | <span data-ttu-id="8283f-152">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-152">Path</span></span>                           | <span data-ttu-id="8283f-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8283f-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="8283f-154">1</span><span class="sxs-lookup"><span data-stu-id="8283f-154">1</span></span>     | <span data-ttu-id="8283f-155">/ИФД/ексиф/{ушорт = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="8283f-156">2</span><span class="sxs-lookup"><span data-stu-id="8283f-156">2</span></span>     | <span data-ttu-id="8283f-157">/ИФД/КСМП/ексиф: Дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8283f-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8283f-158">Remove Paths</span></span>



| <span data-ttu-id="8283f-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="8283f-159">Order</span></span> | <span data-ttu-id="8283f-160">Путь</span><span class="sxs-lookup"><span data-stu-id="8283f-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="8283f-161">1</span><span class="sxs-lookup"><span data-stu-id="8283f-161">1</span></span>     | <span data-ttu-id="8283f-162">/ИФД/ексиф/{ушорт = 41988}</span><span class="sxs-lookup"><span data-stu-id="8283f-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="8283f-163">2</span><span class="sxs-lookup"><span data-stu-id="8283f-163">2</span></span>     | <span data-ttu-id="8283f-164">/ИФД/КСМП/ексиф: дигиталзумратио</span><span class="sxs-lookup"><span data-stu-id="8283f-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8283f-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8283f-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8283f-166">См. также</span><span class="sxs-lookup"><span data-stu-id="8283f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8283f-167">System. photo. Дигиталзум</span><span class="sxs-lookup"><span data-stu-id="8283f-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
