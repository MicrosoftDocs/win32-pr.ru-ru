---
description: Политика метаданных фотографии для свойства System. photo. Фокалленгс.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Политика метаданных фото для System. photo. Фокалленгс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712351"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="17ac2-103">Политика метаданных фото для System. photo. Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="17ac2-104">Политика метаданных фотографии для свойства [System. photo. фокалленгс](../properties/props-system-photo-focallength.md) .</span><span class="sxs-lookup"><span data-stu-id="17ac2-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="17ac2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="17ac2-105">PKEY</span></span>

<span data-ttu-id="17ac2-106">\_Фокалленгс фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="17ac2-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="17ac2-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="17ac2-107">Containers</span></span>

<span data-ttu-id="17ac2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="17ac2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="17ac2-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="17ac2-109">Read-Only</span></span>

<span data-ttu-id="17ac2-110">Да</span><span class="sxs-lookup"><span data-stu-id="17ac2-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="17ac2-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="17ac2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="17ac2-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="17ac2-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="17ac2-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="17ac2-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="17ac2-114">Это значение формируется из System. photo. Фокалленгснумератор и System. photo. Фокалленгсденоминатор.</span><span class="sxs-lookup"><span data-stu-id="17ac2-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="17ac2-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="17ac2-115">It cannot be written directly.</span></span> <span data-ttu-id="17ac2-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="17ac2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="17ac2-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="17ac2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="17ac2-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="17ac2-118">Read Paths</span></span>



| <span data-ttu-id="17ac2-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-119">Order</span></span> | <span data-ttu-id="17ac2-120">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-120">Path</span></span>                          | <span data-ttu-id="17ac2-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="17ac2-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="17ac2-122">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-122">1</span></span>     | <span data-ttu-id="17ac2-123">/APP1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="17ac2-124">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-124">2</span></span>     | <span data-ttu-id="17ac2-125">/КСМП/ексиф: Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="17ac2-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="17ac2-126">Write Paths</span></span>



| <span data-ttu-id="17ac2-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-127">Order</span></span> | <span data-ttu-id="17ac2-128">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-128">Path</span></span>                          | <span data-ttu-id="17ac2-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="17ac2-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="17ac2-130">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-130">1</span></span>     | <span data-ttu-id="17ac2-131">/APP1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="17ac2-132">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-132">2</span></span>     | <span data-ttu-id="17ac2-133">/КСМП/ексиф: Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="17ac2-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="17ac2-134">Remove Paths</span></span>



| <span data-ttu-id="17ac2-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-135">Order</span></span> | <span data-ttu-id="17ac2-136">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="17ac2-137">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-137">1</span></span>     | <span data-ttu-id="17ac2-138">/APP1/IFD/EXIF/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="17ac2-139">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-139">2</span></span>     | <span data-ttu-id="17ac2-140">/КСМП/ексиф: фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="17ac2-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="17ac2-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="17ac2-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="17ac2-142">Read Paths</span></span>



| <span data-ttu-id="17ac2-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-143">Order</span></span> | <span data-ttu-id="17ac2-144">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-144">Path</span></span>                      | <span data-ttu-id="17ac2-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="17ac2-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="17ac2-146">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-146">1</span></span>     | <span data-ttu-id="17ac2-147">/ИФД/ексиф/{ушорт = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="17ac2-148">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-148">2</span></span>     | <span data-ttu-id="17ac2-149">/ИФД/КСМП/ексиф: Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="17ac2-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="17ac2-150">Write Paths</span></span>



| <span data-ttu-id="17ac2-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-151">Order</span></span> | <span data-ttu-id="17ac2-152">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-152">Path</span></span>                      | <span data-ttu-id="17ac2-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="17ac2-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="17ac2-154">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-154">1</span></span>     | <span data-ttu-id="17ac2-155">/ИФД/ексиф/{ушорт = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="17ac2-156">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-156">2</span></span>     | <span data-ttu-id="17ac2-157">/ИФД/КСМП/ексиф: Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="17ac2-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="17ac2-158">Remove Paths</span></span>



| <span data-ttu-id="17ac2-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="17ac2-159">Order</span></span> | <span data-ttu-id="17ac2-160">Путь</span><span class="sxs-lookup"><span data-stu-id="17ac2-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="17ac2-161">1</span><span class="sxs-lookup"><span data-stu-id="17ac2-161">1</span></span>     | <span data-ttu-id="17ac2-162">/ИФД/ексиф/{ушорт = 37386}</span><span class="sxs-lookup"><span data-stu-id="17ac2-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="17ac2-163">2</span><span class="sxs-lookup"><span data-stu-id="17ac2-163">2</span></span>     | <span data-ttu-id="17ac2-164">/ИФД/КСМП/ексиф: фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="17ac2-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17ac2-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ac2-166">См. также</span><span class="sxs-lookup"><span data-stu-id="17ac2-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ac2-167">System. photo. Фокалленгс</span><span class="sxs-lookup"><span data-stu-id="17ac2-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
