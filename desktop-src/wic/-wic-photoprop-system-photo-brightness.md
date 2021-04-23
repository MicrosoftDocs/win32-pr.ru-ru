---
description: Политика метаданных фотографии для свойства System. photo. яркость.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Политика метаданных фотографии System. photo. яркость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999340"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="746c1-103">Политика метаданных фотографии System. photo. яркость</span><span class="sxs-lookup"><span data-stu-id="746c1-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="746c1-104">Политика метаданных фотографии для свойства [System. photo. яркость](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="746c1-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="746c1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="746c1-105">PKEY</span></span>

<span data-ttu-id="746c1-106">\_Яркость фотографии \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="746c1-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="746c1-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="746c1-107">Containers</span></span>

<span data-ttu-id="746c1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="746c1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="746c1-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="746c1-109">Read-Only</span></span>

<span data-ttu-id="746c1-110">Да</span><span class="sxs-lookup"><span data-stu-id="746c1-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="746c1-111">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="746c1-111">Input Type</span></span>

<span data-ttu-id="746c1-112">Double</span><span class="sxs-lookup"><span data-stu-id="746c1-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="746c1-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="746c1-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="746c1-114">Это значение формируется из System. photo. Апертуренумератор и System. photo. Апертуреденоминатор.</span><span class="sxs-lookup"><span data-stu-id="746c1-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="746c1-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="746c1-115">It cannot be written directly.</span></span> <span data-ttu-id="746c1-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="746c1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="746c1-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="746c1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="746c1-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="746c1-118">Read Paths</span></span>



| <span data-ttu-id="746c1-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-119">Order</span></span> | <span data-ttu-id="746c1-120">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-120">Path</span></span>                          | <span data-ttu-id="746c1-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="746c1-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="746c1-122">1</span><span class="sxs-lookup"><span data-stu-id="746c1-122">1</span></span>     | <span data-ttu-id="746c1-123">/APP1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="746c1-124">2</span><span class="sxs-lookup"><span data-stu-id="746c1-124">2</span></span>     | <span data-ttu-id="746c1-125">/КСМП/ексиф: Бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="746c1-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="746c1-126">Write Paths</span></span>



| <span data-ttu-id="746c1-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-127">Order</span></span> | <span data-ttu-id="746c1-128">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-128">Path</span></span>                          | <span data-ttu-id="746c1-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="746c1-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="746c1-130">1</span><span class="sxs-lookup"><span data-stu-id="746c1-130">1</span></span>     | <span data-ttu-id="746c1-131">/APP1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="746c1-132">2</span><span class="sxs-lookup"><span data-stu-id="746c1-132">2</span></span>     | <span data-ttu-id="746c1-133">/КСМП/ексиф: Бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="746c1-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="746c1-134">Remove Paths</span></span>



| <span data-ttu-id="746c1-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-135">Order</span></span> | <span data-ttu-id="746c1-136">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="746c1-137">1</span><span class="sxs-lookup"><span data-stu-id="746c1-137">1</span></span>     | <span data-ttu-id="746c1-138">/APP1/IFD/EXIF/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="746c1-139">2</span><span class="sxs-lookup"><span data-stu-id="746c1-139">2</span></span>     | <span data-ttu-id="746c1-140">/КСМП/ексиф: бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="746c1-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="746c1-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="746c1-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="746c1-142">Read Paths</span></span>



| <span data-ttu-id="746c1-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-143">Order</span></span> | <span data-ttu-id="746c1-144">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-144">Path</span></span>                          | <span data-ttu-id="746c1-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="746c1-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="746c1-146">1</span><span class="sxs-lookup"><span data-stu-id="746c1-146">1</span></span>     | <span data-ttu-id="746c1-147">/ИФД/ексиф/{ушорт = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="746c1-148">2</span><span class="sxs-lookup"><span data-stu-id="746c1-148">2</span></span>     | <span data-ttu-id="746c1-149">/ИФД/КСМП/ексиф: Бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="746c1-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="746c1-150">Write Paths</span></span>



| <span data-ttu-id="746c1-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-151">Order</span></span> | <span data-ttu-id="746c1-152">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-152">Path</span></span>                          | <span data-ttu-id="746c1-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="746c1-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="746c1-154">1</span><span class="sxs-lookup"><span data-stu-id="746c1-154">1</span></span>     | <span data-ttu-id="746c1-155">/ИФД/ексиф/{ушорт = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="746c1-156">2</span><span class="sxs-lookup"><span data-stu-id="746c1-156">2</span></span>     | <span data-ttu-id="746c1-157">/ИФД/КСМП/ексиф: Бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="746c1-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="746c1-158">Remove Paths</span></span>



| <span data-ttu-id="746c1-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="746c1-159">Order</span></span> | <span data-ttu-id="746c1-160">Путь</span><span class="sxs-lookup"><span data-stu-id="746c1-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="746c1-161">1</span><span class="sxs-lookup"><span data-stu-id="746c1-161">1</span></span>     | <span data-ttu-id="746c1-162">/ИФД/ексиф/{ушорт = 37379}</span><span class="sxs-lookup"><span data-stu-id="746c1-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="746c1-163">2</span><span class="sxs-lookup"><span data-stu-id="746c1-163">2</span></span>     | <span data-ttu-id="746c1-164">/ИФД/КСМП/ексиф: бригхтнессвалуе</span><span class="sxs-lookup"><span data-stu-id="746c1-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="746c1-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="746c1-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="746c1-166">См. также</span><span class="sxs-lookup"><span data-stu-id="746c1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="746c1-167">System. photo. яркость</span><span class="sxs-lookup"><span data-stu-id="746c1-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
