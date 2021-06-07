---
description: Политика метаданных фотографии для свойства System. photo. Фнумбер.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Политика метаданных фото для System. photo. Фнумбер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443625"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="050ff-103">Политика метаданных фото для System. photo. Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="050ff-104">Политика метаданных фотографии для свойства [System. photo. фнумбер](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="050ff-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="050ff-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="050ff-105">PKEY</span></span>

<span data-ttu-id="050ff-106">\_Фнумбер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="050ff-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="050ff-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="050ff-107">Containers</span></span>

<span data-ttu-id="050ff-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="050ff-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="050ff-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="050ff-109">Read-Only</span></span>

<span data-ttu-id="050ff-110">Да</span><span class="sxs-lookup"><span data-stu-id="050ff-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="050ff-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="050ff-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="050ff-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="050ff-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="050ff-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="050ff-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="050ff-114">Это значение формируется из System. photo. Фнумбернумератор и System. photo. Фнумберденоминатор.</span><span class="sxs-lookup"><span data-stu-id="050ff-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="050ff-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="050ff-115">It cannot be written directly.</span></span> <span data-ttu-id="050ff-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="050ff-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="050ff-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="050ff-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="050ff-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="050ff-118">Read Paths</span></span>



| <span data-ttu-id="050ff-119">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-119">Order</span></span> | <span data-ttu-id="050ff-120">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-120">Path</span></span>                          | <span data-ttu-id="050ff-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="050ff-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="050ff-122">1</span><span class="sxs-lookup"><span data-stu-id="050ff-122">1</span></span>     | <span data-ttu-id="050ff-123">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="050ff-124">2</span><span class="sxs-lookup"><span data-stu-id="050ff-124">2</span></span>     | <span data-ttu-id="050ff-125">/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="050ff-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="050ff-126">Write Paths</span></span>



| <span data-ttu-id="050ff-127">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-127">Order</span></span> | <span data-ttu-id="050ff-128">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-128">Path</span></span>                          | <span data-ttu-id="050ff-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="050ff-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="050ff-130">1</span><span class="sxs-lookup"><span data-stu-id="050ff-130">1</span></span>     | <span data-ttu-id="050ff-131">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="050ff-132">2</span><span class="sxs-lookup"><span data-stu-id="050ff-132">2</span></span>     | <span data-ttu-id="050ff-133">/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="050ff-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="050ff-134">Remove Paths</span></span>



| <span data-ttu-id="050ff-135">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-135">Order</span></span> | <span data-ttu-id="050ff-136">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="050ff-137">1</span><span class="sxs-lookup"><span data-stu-id="050ff-137">1</span></span>     | <span data-ttu-id="050ff-138">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="050ff-139">2</span><span class="sxs-lookup"><span data-stu-id="050ff-139">2</span></span>     | <span data-ttu-id="050ff-140">/КСМП/ексиф: фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="050ff-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="050ff-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="050ff-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="050ff-142">Read Paths</span></span>



| <span data-ttu-id="050ff-143">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-143">Order</span></span> | <span data-ttu-id="050ff-144">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-144">Path</span></span>                     | <span data-ttu-id="050ff-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="050ff-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="050ff-146">1</span><span class="sxs-lookup"><span data-stu-id="050ff-146">1</span></span>     | <span data-ttu-id="050ff-147">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="050ff-148">2</span><span class="sxs-lookup"><span data-stu-id="050ff-148">2</span></span>     | <span data-ttu-id="050ff-149">/ИФД/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="050ff-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="050ff-150">Write Paths</span></span>



| <span data-ttu-id="050ff-151">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-151">Order</span></span> | <span data-ttu-id="050ff-152">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-152">Path</span></span>                     | <span data-ttu-id="050ff-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="050ff-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="050ff-154">1</span><span class="sxs-lookup"><span data-stu-id="050ff-154">1</span></span>     | <span data-ttu-id="050ff-155">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="050ff-156">2</span><span class="sxs-lookup"><span data-stu-id="050ff-156">2</span></span>     | <span data-ttu-id="050ff-157">/ИФД/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="050ff-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="050ff-158">Remove Paths</span></span>



| <span data-ttu-id="050ff-159">Номер</span><span class="sxs-lookup"><span data-stu-id="050ff-159">Order</span></span> | <span data-ttu-id="050ff-160">Путь</span><span class="sxs-lookup"><span data-stu-id="050ff-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="050ff-161">1</span><span class="sxs-lookup"><span data-stu-id="050ff-161">1</span></span>     | <span data-ttu-id="050ff-162">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="050ff-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="050ff-163">2</span><span class="sxs-lookup"><span data-stu-id="050ff-163">2</span></span>     | <span data-ttu-id="050ff-164">/ИФД/КСМП/ексиф: фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="050ff-165">Remarks</span><span class="sxs-lookup"><span data-stu-id="050ff-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="050ff-166">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="050ff-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="050ff-167">System. photo. Фнумбер</span><span class="sxs-lookup"><span data-stu-id="050ff-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
