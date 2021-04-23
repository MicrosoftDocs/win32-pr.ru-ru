---
description: Политика метаданных фотографии для свойства System. photo. Флашенерги.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Политика метаданных фото для System. photo. Флашенерги
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081446"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="4266f-103">Политика метаданных фото для System. photo. Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="4266f-104">Политика метаданных фотографии для свойства [System. photo. флашенерги](../properties/props-system-photo-flashenergy.md) .</span><span class="sxs-lookup"><span data-stu-id="4266f-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4266f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4266f-105">PKEY</span></span>

<span data-ttu-id="4266f-106">\_Флашенерги фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="4266f-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="4266f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="4266f-107">Containers</span></span>

<span data-ttu-id="4266f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4266f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4266f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4266f-109">Read-Only</span></span>

<span data-ttu-id="4266f-110">Да</span><span class="sxs-lookup"><span data-stu-id="4266f-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="4266f-111">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="4266f-111">Input Type</span></span>

<span data-ttu-id="4266f-112">Double</span><span class="sxs-lookup"><span data-stu-id="4266f-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4266f-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="4266f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="4266f-114">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="4266f-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4266f-115">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="4266f-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4266f-116">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="4266f-116">Read Paths</span></span>



| <span data-ttu-id="4266f-117">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-117">Order</span></span> | <span data-ttu-id="4266f-118">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-118">Path</span></span>                          | <span data-ttu-id="4266f-119">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4266f-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4266f-120">1</span><span class="sxs-lookup"><span data-stu-id="4266f-120">1</span></span>     | <span data-ttu-id="4266f-121">/APP1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="4266f-122">2</span><span class="sxs-lookup"><span data-stu-id="4266f-122">2</span></span>     | <span data-ttu-id="4266f-123">/КСМП/ексиф: Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="4266f-124">Пути записи</span><span class="sxs-lookup"><span data-stu-id="4266f-124">Write Paths</span></span>



| <span data-ttu-id="4266f-125">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-125">Order</span></span> | <span data-ttu-id="4266f-126">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-126">Path</span></span>                          | <span data-ttu-id="4266f-127">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4266f-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4266f-128">1</span><span class="sxs-lookup"><span data-stu-id="4266f-128">1</span></span>     | <span data-ttu-id="4266f-129">/APP1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="4266f-130">2</span><span class="sxs-lookup"><span data-stu-id="4266f-130">2</span></span>     | <span data-ttu-id="4266f-131">/КСМП/ексиф: Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4266f-132">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="4266f-132">Remove Paths</span></span>



| <span data-ttu-id="4266f-133">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-133">Order</span></span> | <span data-ttu-id="4266f-134">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="4266f-135">1</span><span class="sxs-lookup"><span data-stu-id="4266f-135">1</span></span>     | <span data-ttu-id="4266f-136">/APP1/IFD/EXIF/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="4266f-137">2</span><span class="sxs-lookup"><span data-stu-id="4266f-137">2</span></span>     | <span data-ttu-id="4266f-138">/КСМП/ексиф: флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="4266f-139">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="4266f-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4266f-140">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="4266f-140">Read Paths</span></span>



| <span data-ttu-id="4266f-141">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-141">Order</span></span> | <span data-ttu-id="4266f-142">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-142">Path</span></span>                      | <span data-ttu-id="4266f-143">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4266f-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4266f-144">1</span><span class="sxs-lookup"><span data-stu-id="4266f-144">1</span></span>     | <span data-ttu-id="4266f-145">/ИФД/ексиф/{ушорт = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="4266f-146">2</span><span class="sxs-lookup"><span data-stu-id="4266f-146">2</span></span>     | <span data-ttu-id="4266f-147">/ИФД/КСМП/ексиф: Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4266f-148">Пути записи</span><span class="sxs-lookup"><span data-stu-id="4266f-148">Write Paths</span></span>



| <span data-ttu-id="4266f-149">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-149">Order</span></span> | <span data-ttu-id="4266f-150">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-150">Path</span></span>                      | <span data-ttu-id="4266f-151">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4266f-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4266f-152">1</span><span class="sxs-lookup"><span data-stu-id="4266f-152">1</span></span>     | <span data-ttu-id="4266f-153">/ИФД/ексиф/{ушорт = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="4266f-154">2</span><span class="sxs-lookup"><span data-stu-id="4266f-154">2</span></span>     | <span data-ttu-id="4266f-155">/ИФД/КСМП/ексиф: Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4266f-156">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="4266f-156">Remove Paths</span></span>



| <span data-ttu-id="4266f-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="4266f-157">Order</span></span> | <span data-ttu-id="4266f-158">Путь</span><span class="sxs-lookup"><span data-stu-id="4266f-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4266f-159">1</span><span class="sxs-lookup"><span data-stu-id="4266f-159">1</span></span>     | <span data-ttu-id="4266f-160">/ИФД/ексиф/{ушорт = 41483}</span><span class="sxs-lookup"><span data-stu-id="4266f-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="4266f-161">2</span><span class="sxs-lookup"><span data-stu-id="4266f-161">2</span></span>     | <span data-ttu-id="4266f-162">/ИФД/КСМП/ексиф: флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4266f-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4266f-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4266f-164">См. также</span><span class="sxs-lookup"><span data-stu-id="4266f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4266f-165">System. photo. Флашенерги</span><span class="sxs-lookup"><span data-stu-id="4266f-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
