---
description: Политика метаданных фотографии для свойства System. photo. Фнумбер.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Политика метаданных фото для System. photo. Фнумбер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265289"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="9a204-103">Политика метаданных фото для System. photo. Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="9a204-104">Политика метаданных фотографии для свойства [System. photo. фнумбер](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="9a204-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9a204-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9a204-105">PKEY</span></span>

<span data-ttu-id="9a204-106">\_Фнумбер фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="9a204-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="9a204-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="9a204-107">Containers</span></span>

<span data-ttu-id="9a204-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9a204-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9a204-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a204-109">Read-Only</span></span>

<span data-ttu-id="9a204-110">Да</span><span class="sxs-lookup"><span data-stu-id="9a204-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9a204-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="9a204-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9a204-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9a204-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9a204-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="9a204-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9a204-114">Это значение формируется из System. photo. Фнумбернумератор и System. photo. Фнумберденоминатор.</span><span class="sxs-lookup"><span data-stu-id="9a204-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="9a204-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="9a204-115">It cannot be written directly.</span></span> <span data-ttu-id="9a204-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="9a204-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9a204-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="9a204-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a204-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9a204-118">Read Paths</span></span>



| <span data-ttu-id="9a204-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-119">Order</span></span> | <span data-ttu-id="9a204-120">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-120">Path</span></span>                          | <span data-ttu-id="9a204-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a204-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="9a204-122">1</span><span class="sxs-lookup"><span data-stu-id="9a204-122">1</span></span>     | <span data-ttu-id="9a204-123">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="9a204-124">2</span><span class="sxs-lookup"><span data-stu-id="9a204-124">2</span></span>     | <span data-ttu-id="9a204-125">/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="9a204-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9a204-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="9a204-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-127">Order</span></span> | <span data-ttu-id="9a204-128">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-128">Path</span></span>                          | <span data-ttu-id="9a204-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a204-129">Disk Format</span></span> |     |
| <span data-ttu-id="9a204-130">1</span><span class="sxs-lookup"><span data-stu-id="9a204-130">1</span></span>     | <span data-ttu-id="9a204-131">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="9a204-132">2</span><span class="sxs-lookup"><span data-stu-id="9a204-132">2</span></span>     | <span data-ttu-id="9a204-133">/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="9a204-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9a204-134">Remove Paths</span></span>



| <span data-ttu-id="9a204-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-135">Order</span></span> | <span data-ttu-id="9a204-136">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="9a204-137">1</span><span class="sxs-lookup"><span data-stu-id="9a204-137">1</span></span>     | <span data-ttu-id="9a204-138">/APP1/IFD/EXIF/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="9a204-139">2</span><span class="sxs-lookup"><span data-stu-id="9a204-139">2</span></span>     | <span data-ttu-id="9a204-140">/КСМП/ексиф: фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="9a204-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="9a204-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a204-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9a204-142">Read Paths</span></span>



| <span data-ttu-id="9a204-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-143">Order</span></span> | <span data-ttu-id="9a204-144">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-144">Path</span></span>                     | <span data-ttu-id="9a204-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a204-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9a204-146">1</span><span class="sxs-lookup"><span data-stu-id="9a204-146">1</span></span>     | <span data-ttu-id="9a204-147">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="9a204-148">2</span><span class="sxs-lookup"><span data-stu-id="9a204-148">2</span></span>     | <span data-ttu-id="9a204-149">/ИФД/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="9a204-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9a204-150">Write Paths</span></span>



| <span data-ttu-id="9a204-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-151">Order</span></span> | <span data-ttu-id="9a204-152">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-152">Path</span></span>                     | <span data-ttu-id="9a204-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a204-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9a204-154">1</span><span class="sxs-lookup"><span data-stu-id="9a204-154">1</span></span>     | <span data-ttu-id="9a204-155">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="9a204-156">2</span><span class="sxs-lookup"><span data-stu-id="9a204-156">2</span></span>     | <span data-ttu-id="9a204-157">/ИФД/КСМП/ексиф: Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9a204-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9a204-158">Remove Paths</span></span>



| <span data-ttu-id="9a204-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a204-159">Order</span></span> | <span data-ttu-id="9a204-160">Путь</span><span class="sxs-lookup"><span data-stu-id="9a204-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="9a204-161">1</span><span class="sxs-lookup"><span data-stu-id="9a204-161">1</span></span>     | <span data-ttu-id="9a204-162">/ИФД/ексиф/{ушорт = 33437}</span><span class="sxs-lookup"><span data-stu-id="9a204-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="9a204-163">2</span><span class="sxs-lookup"><span data-stu-id="9a204-163">2</span></span>     | <span data-ttu-id="9a204-164">/ИФД/КСМП/ексиф: фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="9a204-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a204-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a204-166">См. также</span><span class="sxs-lookup"><span data-stu-id="9a204-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a204-167">System. photo. Фнумбер</span><span class="sxs-lookup"><span data-stu-id="9a204-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
