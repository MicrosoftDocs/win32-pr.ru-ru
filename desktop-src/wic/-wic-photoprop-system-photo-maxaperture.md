---
description: Политика метаданных фотографии для свойства System. photo. Максапертуре.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Политика метаданных фото для System. photo. Максапертуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674001"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="441c2-103">Политика метаданных фото для System. photo. Максапертуре</span><span class="sxs-lookup"><span data-stu-id="441c2-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="441c2-104">Политика метаданных фотографии для свойства [System. photo. максапертуре](../properties/props-system-photo-maxaperture.md) .</span><span class="sxs-lookup"><span data-stu-id="441c2-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="441c2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="441c2-105">PKEY</span></span>

<span data-ttu-id="441c2-106">\_Максапертуре фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="441c2-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="441c2-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="441c2-107">Containers</span></span>

<span data-ttu-id="441c2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="441c2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="441c2-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="441c2-109">Read-Only</span></span>

<span data-ttu-id="441c2-110">Да</span><span class="sxs-lookup"><span data-stu-id="441c2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="441c2-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="441c2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="441c2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="441c2-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="441c2-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="441c2-113">Input Type</span></span>

<span data-ttu-id="441c2-114">Double</span><span class="sxs-lookup"><span data-stu-id="441c2-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="441c2-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="441c2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="441c2-116">Это значение формируется из System. photo. Максапертуренумератор и System. photo. Максапертуреденоминатор.</span><span class="sxs-lookup"><span data-stu-id="441c2-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="441c2-117">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="441c2-117">It cannot be written directly.</span></span> <span data-ttu-id="441c2-118">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="441c2-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="441c2-119">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="441c2-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="441c2-120">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="441c2-120">Read Paths</span></span>



| <span data-ttu-id="441c2-121">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-121">Order</span></span> | <span data-ttu-id="441c2-122">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-122">Path</span></span>                          | <span data-ttu-id="441c2-123">Формат диска</span><span class="sxs-lookup"><span data-stu-id="441c2-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="441c2-124">1</span><span class="sxs-lookup"><span data-stu-id="441c2-124">1</span></span>     | <span data-ttu-id="441c2-125">/APP1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="441c2-126">2</span><span class="sxs-lookup"><span data-stu-id="441c2-126">2</span></span>     | <span data-ttu-id="441c2-127">/КСМП/ексиф: Максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="441c2-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="441c2-128">Write Paths</span></span>



| <span data-ttu-id="441c2-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-129">Order</span></span> | <span data-ttu-id="441c2-130">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-130">Path</span></span>                          | <span data-ttu-id="441c2-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="441c2-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="441c2-132">1</span><span class="sxs-lookup"><span data-stu-id="441c2-132">1</span></span>     | <span data-ttu-id="441c2-133">/APP1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="441c2-134">2</span><span class="sxs-lookup"><span data-stu-id="441c2-134">2</span></span>     | <span data-ttu-id="441c2-135">/КСМП/ексиф: Максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="441c2-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="441c2-136">Remove Paths</span></span>



| <span data-ttu-id="441c2-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-137">Order</span></span> | <span data-ttu-id="441c2-138">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="441c2-139">1</span><span class="sxs-lookup"><span data-stu-id="441c2-139">1</span></span>     | <span data-ttu-id="441c2-140">/APP1/IFD/EXIF/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="441c2-141">2</span><span class="sxs-lookup"><span data-stu-id="441c2-141">2</span></span>     | <span data-ttu-id="441c2-142">/КСМП/ексиф: максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="441c2-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="441c2-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="441c2-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="441c2-144">Read Paths</span></span>



| <span data-ttu-id="441c2-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-145">Order</span></span> | <span data-ttu-id="441c2-146">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-146">Path</span></span>                           | <span data-ttu-id="441c2-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="441c2-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="441c2-148">1</span><span class="sxs-lookup"><span data-stu-id="441c2-148">1</span></span>     | <span data-ttu-id="441c2-149">/ИФД/ексиф/{ушорт = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="441c2-150">2</span><span class="sxs-lookup"><span data-stu-id="441c2-150">2</span></span>     | <span data-ttu-id="441c2-151">/ИФД/КСМП/ексиф: Максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="441c2-152">Пути записи</span><span class="sxs-lookup"><span data-stu-id="441c2-152">Write Paths</span></span>



| <span data-ttu-id="441c2-153">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-153">Order</span></span> | <span data-ttu-id="441c2-154">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-154">Path</span></span>                           | <span data-ttu-id="441c2-155">Формат диска</span><span class="sxs-lookup"><span data-stu-id="441c2-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="441c2-156">1</span><span class="sxs-lookup"><span data-stu-id="441c2-156">1</span></span>     | <span data-ttu-id="441c2-157">/ИФД/ексиф/{ушорт = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="441c2-158">2</span><span class="sxs-lookup"><span data-stu-id="441c2-158">2</span></span>     | <span data-ttu-id="441c2-159">/ИФД/КСМП/ексиф: Максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="441c2-160">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="441c2-160">Remove Paths</span></span>



| <span data-ttu-id="441c2-161">Заказ</span><span class="sxs-lookup"><span data-stu-id="441c2-161">Order</span></span> | <span data-ttu-id="441c2-162">Путь</span><span class="sxs-lookup"><span data-stu-id="441c2-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="441c2-163">1</span><span class="sxs-lookup"><span data-stu-id="441c2-163">1</span></span>     | <span data-ttu-id="441c2-164">/ИФД/ексиф/{ушорт = 37381}</span><span class="sxs-lookup"><span data-stu-id="441c2-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="441c2-165">2</span><span class="sxs-lookup"><span data-stu-id="441c2-165">2</span></span>     | <span data-ttu-id="441c2-166">/ИФД/КСМП/ексиф: максапертуревалуе</span><span class="sxs-lookup"><span data-stu-id="441c2-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="441c2-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="441c2-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="441c2-168">См. также</span><span class="sxs-lookup"><span data-stu-id="441c2-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="441c2-169">System. photo. Максапертуре</span><span class="sxs-lookup"><span data-stu-id="441c2-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
