---
description: Политика метаданных фотографии для свойства System. photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Политика метаданных фотографии System. photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674003"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="e83ff-103">Политика метаданных фотографии System. photo. Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="e83ff-104">Политика метаданных фотографии для свойства [System. photo. Flash](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="e83ff-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e83ff-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e83ff-105">PKEY</span></span>

<span data-ttu-id="e83ff-106">\_Фото \_ -ВСПЫШКа PKEY</span><span class="sxs-lookup"><span data-stu-id="e83ff-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="e83ff-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e83ff-107">Containers</span></span>

<span data-ttu-id="e83ff-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e83ff-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e83ff-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e83ff-109">Read-Only</span></span>

<span data-ttu-id="e83ff-110">Нет</span><span class="sxs-lookup"><span data-stu-id="e83ff-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e83ff-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e83ff-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e83ff-112">VT \_ UI1 (если исходная схема — XMP) или VT \_ UI2 (если исходная схема — EXIF)</span><span class="sxs-lookup"><span data-stu-id="e83ff-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="e83ff-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="e83ff-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="e83ff-114">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="e83ff-114">Input Type</span></span>

<span data-ttu-id="e83ff-115">VT \_ UI1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e83ff-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="e83ff-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="e83ff-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e83ff-117">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e83ff-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="e83ff-118">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e83ff-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e83ff-119">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="e83ff-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e83ff-120">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e83ff-120">Read Paths</span></span>



| <span data-ttu-id="e83ff-121">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-121">Order</span></span> | <span data-ttu-id="e83ff-122">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-122">Path</span></span>                             | <span data-ttu-id="e83ff-123">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e83ff-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="e83ff-124">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-124">1</span></span>     | <span data-ttu-id="e83ff-125">/APP1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="e83ff-126">ushort</span><span class="sxs-lookup"><span data-stu-id="e83ff-126">ushort</span></span>      |
| <span data-ttu-id="e83ff-127">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-127">2</span></span>     | <span data-ttu-id="e83ff-128">/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e83ff-129">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e83ff-129">Write Paths</span></span>



| <span data-ttu-id="e83ff-130">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-130">Order</span></span> | <span data-ttu-id="e83ff-131">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-131">Path</span></span>                             | <span data-ttu-id="e83ff-132">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e83ff-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="e83ff-133">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-133">1</span></span>     | <span data-ttu-id="e83ff-134">/APP1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="e83ff-135">ushort</span><span class="sxs-lookup"><span data-stu-id="e83ff-135">ushort</span></span>      |
| <span data-ttu-id="e83ff-136">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-136">2</span></span>     | <span data-ttu-id="e83ff-137">/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e83ff-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e83ff-138">Remove Paths</span></span>



| <span data-ttu-id="e83ff-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-139">Order</span></span> | <span data-ttu-id="e83ff-140">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="e83ff-141">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-141">1</span></span>     | <span data-ttu-id="e83ff-142">/APP1/IFD/EXIF/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="e83ff-143">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-143">2</span></span>     | <span data-ttu-id="e83ff-144">/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="e83ff-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="e83ff-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e83ff-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e83ff-146">Read Paths</span></span>



| <span data-ttu-id="e83ff-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-147">Order</span></span> | <span data-ttu-id="e83ff-148">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-148">Path</span></span>                                 | <span data-ttu-id="e83ff-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e83ff-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="e83ff-150">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-150">1</span></span>     | <span data-ttu-id="e83ff-151">/ИФД/ексиф/{ушорт = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="e83ff-152">ushort</span><span class="sxs-lookup"><span data-stu-id="e83ff-152">ushort</span></span>      |
| <span data-ttu-id="e83ff-153">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-153">2</span></span>     | <span data-ttu-id="e83ff-154">/ИФД/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e83ff-155">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e83ff-155">Write Paths</span></span>



| <span data-ttu-id="e83ff-156">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-156">Order</span></span> | <span data-ttu-id="e83ff-157">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-157">Path</span></span>                                 | <span data-ttu-id="e83ff-158">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e83ff-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="e83ff-159">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-159">1</span></span>     | <span data-ttu-id="e83ff-160">/ИФД/ексиф/{ушорт = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="e83ff-161">ushort</span><span class="sxs-lookup"><span data-stu-id="e83ff-161">ushort</span></span>      |
| <span data-ttu-id="e83ff-162">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-162">2</span></span>     | <span data-ttu-id="e83ff-163">/ИФД/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e83ff-164">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e83ff-164">Remove Paths</span></span>



| <span data-ttu-id="e83ff-165">Заказ</span><span class="sxs-lookup"><span data-stu-id="e83ff-165">Order</span></span> | <span data-ttu-id="e83ff-166">Путь</span><span class="sxs-lookup"><span data-stu-id="e83ff-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="e83ff-167">1</span><span class="sxs-lookup"><span data-stu-id="e83ff-167">1</span></span>     | <span data-ttu-id="e83ff-168">/ИФД/ексиф/{ушорт = 37385}</span><span class="sxs-lookup"><span data-stu-id="e83ff-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="e83ff-169">2</span><span class="sxs-lookup"><span data-stu-id="e83ff-169">2</span></span>     | <span data-ttu-id="e83ff-170">/ИФД/КСМП/ <xmpstruct> EXIF: Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e83ff-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e83ff-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e83ff-172">См. также</span><span class="sxs-lookup"><span data-stu-id="e83ff-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83ff-173">System. photo. Flash</span><span class="sxs-lookup"><span data-stu-id="e83ff-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
