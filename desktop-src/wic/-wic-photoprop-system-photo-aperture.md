---
description: Политика метаданных фотографии для свойства System. photo. апертуры.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Политика метаданных фотографии System. photo. апертуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684292"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="56d7d-103">Политика метаданных фотографии System. photo. апертуры</span><span class="sxs-lookup"><span data-stu-id="56d7d-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="56d7d-104">Политика метаданных фотографии для свойства [System. photo. апертуры](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="56d7d-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="56d7d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="56d7d-105">PKEY</span></span>

<span data-ttu-id="56d7d-106">\_ \_ Фотоапертура PKEY</span><span class="sxs-lookup"><span data-stu-id="56d7d-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="56d7d-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="56d7d-107">Containers</span></span>

<span data-ttu-id="56d7d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="56d7d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="56d7d-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="56d7d-109">Read-Only</span></span>

<span data-ttu-id="56d7d-110">Да</span><span class="sxs-lookup"><span data-stu-id="56d7d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="56d7d-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="56d7d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="56d7d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="56d7d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="56d7d-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="56d7d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="56d7d-114">Это значение формируется из System. photo. Апертуренумератор и System. photo. Апертуреденоминатор.</span><span class="sxs-lookup"><span data-stu-id="56d7d-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="56d7d-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="56d7d-115">It cannot be written directly.</span></span> <span data-ttu-id="56d7d-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="56d7d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="56d7d-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="56d7d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="56d7d-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="56d7d-118">Read Paths</span></span>



| <span data-ttu-id="56d7d-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-119">Order</span></span> | <span data-ttu-id="56d7d-120">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-120">Path</span></span>                          | <span data-ttu-id="56d7d-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="56d7d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="56d7d-122">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-122">1</span></span>     | <span data-ttu-id="56d7d-123">/APP1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="56d7d-124">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-124">2</span></span>     | <span data-ttu-id="56d7d-125">/КСМП/ексиф: Апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="56d7d-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="56d7d-126">Write Paths</span></span>



| <span data-ttu-id="56d7d-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-127">Order</span></span> | <span data-ttu-id="56d7d-128">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-128">Path</span></span>                          | <span data-ttu-id="56d7d-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="56d7d-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="56d7d-130">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-130">1</span></span>     | <span data-ttu-id="56d7d-131">/APP1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="56d7d-132">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-132">2</span></span>     | <span data-ttu-id="56d7d-133">/КСМП/ексиф: Апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="56d7d-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="56d7d-134">Remove Paths</span></span>



| <span data-ttu-id="56d7d-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-135">Order</span></span> | <span data-ttu-id="56d7d-136">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="56d7d-137">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-137">1</span></span>     | <span data-ttu-id="56d7d-138">/APP1/IFD/EXIF/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="56d7d-139">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-139">2</span></span>     | <span data-ttu-id="56d7d-140">/КСМП/ексиф: апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="56d7d-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="56d7d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="56d7d-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="56d7d-142">Read Paths</span></span>



| <span data-ttu-id="56d7d-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-143">Order</span></span> | <span data-ttu-id="56d7d-144">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-144">Path</span></span>                        | <span data-ttu-id="56d7d-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="56d7d-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="56d7d-146">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-146">1</span></span>     | <span data-ttu-id="56d7d-147">/ИФД/ексиф/{ушорт = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="56d7d-148">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-148">2</span></span>     | <span data-ttu-id="56d7d-149">/ИФД/КСМП/ексиф: Апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="56d7d-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="56d7d-150">Write Paths</span></span>



| <span data-ttu-id="56d7d-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-151">Order</span></span> | <span data-ttu-id="56d7d-152">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-152">Path</span></span>                        | <span data-ttu-id="56d7d-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="56d7d-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="56d7d-154">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-154">1</span></span>     | <span data-ttu-id="56d7d-155">/ИФД/ексиф/{ушорт = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="56d7d-156">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-156">2</span></span>     | <span data-ttu-id="56d7d-157">/ИФД/КСМП/ексиф: Апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="56d7d-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="56d7d-158">Remove Paths</span></span>



| <span data-ttu-id="56d7d-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="56d7d-159">Order</span></span> | <span data-ttu-id="56d7d-160">Путь</span><span class="sxs-lookup"><span data-stu-id="56d7d-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="56d7d-161">1</span><span class="sxs-lookup"><span data-stu-id="56d7d-161">1</span></span>     | <span data-ttu-id="56d7d-162">/ИФД/ексиф/{ушорт = 37378}</span><span class="sxs-lookup"><span data-stu-id="56d7d-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="56d7d-163">2</span><span class="sxs-lookup"><span data-stu-id="56d7d-163">2</span></span>     | <span data-ttu-id="56d7d-164">/ИФД/КСМП/ексиф: апертуревалуе</span><span class="sxs-lookup"><span data-stu-id="56d7d-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="56d7d-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56d7d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="56d7d-166">См. также</span><span class="sxs-lookup"><span data-stu-id="56d7d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d7d-167">System. photo. Апертура</span><span class="sxs-lookup"><span data-stu-id="56d7d-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
