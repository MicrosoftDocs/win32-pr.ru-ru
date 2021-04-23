---
description: Политика метаданных фотографии для свойства System. photo. Шуттерспид.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Политика метаданных фото для System. photo. Шуттерспид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674127"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="b3c94-103">Политика метаданных фото для System. photo. Шуттерспид</span><span class="sxs-lookup"><span data-stu-id="b3c94-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="b3c94-104">Политика метаданных фотографии для свойства [System. photo. шуттерспид](../properties/props-system-photo-shutterspeed.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c94-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b3c94-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b3c94-105">PKEY</span></span>

<span data-ttu-id="b3c94-106">\_Шуттерспид фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="b3c94-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="b3c94-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="b3c94-107">Containers</span></span>

<span data-ttu-id="b3c94-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b3c94-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b3c94-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b3c94-109">Read-Only</span></span>

<span data-ttu-id="b3c94-110">Да</span><span class="sxs-lookup"><span data-stu-id="b3c94-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b3c94-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="b3c94-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b3c94-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="b3c94-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b3c94-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="b3c94-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b3c94-114">Это значение формируется из System. photo. Шуттерспиднумератор и System. photo. Шуттерспидденоминатор.</span><span class="sxs-lookup"><span data-stu-id="b3c94-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="b3c94-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="b3c94-115">It cannot be written directly.</span></span> <span data-ttu-id="b3c94-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="b3c94-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b3c94-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="b3c94-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3c94-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="b3c94-118">Read Paths</span></span>



| <span data-ttu-id="b3c94-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-119">Order</span></span> | <span data-ttu-id="b3c94-120">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-120">Path</span></span>                          | <span data-ttu-id="b3c94-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b3c94-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b3c94-122">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-122">1</span></span>     | <span data-ttu-id="b3c94-123">/APP1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="b3c94-124">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-124">2</span></span>     | <span data-ttu-id="b3c94-125">/КСМП/ексиф: Шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3c94-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="b3c94-126">Write Paths</span></span>



| <span data-ttu-id="b3c94-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-127">Order</span></span> | <span data-ttu-id="b3c94-128">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-128">Path</span></span>                          | <span data-ttu-id="b3c94-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b3c94-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b3c94-130">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-130">1</span></span>     | <span data-ttu-id="b3c94-131">/APP1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="b3c94-132">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-132">2</span></span>     | <span data-ttu-id="b3c94-133">/КСМП/ексиф: Шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3c94-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="b3c94-134">Remove Paths</span></span>



| <span data-ttu-id="b3c94-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-135">Order</span></span> | <span data-ttu-id="b3c94-136">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b3c94-137">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-137">1</span></span>     | <span data-ttu-id="b3c94-138">/APP1/IFD/EXIF/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="b3c94-139">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-139">2</span></span>     | <span data-ttu-id="b3c94-140">/КСМП/ексиф: шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="b3c94-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="b3c94-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3c94-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="b3c94-142">Read Paths</span></span>



| <span data-ttu-id="b3c94-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-143">Order</span></span> | <span data-ttu-id="b3c94-144">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-144">Path</span></span>                            | <span data-ttu-id="b3c94-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b3c94-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b3c94-146">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-146">1</span></span>     | <span data-ttu-id="b3c94-147">/ИФД/ексиф/{ушорт = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="b3c94-148">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-148">2</span></span>     | <span data-ttu-id="b3c94-149">/ИФД/КСМП/ексиф: Шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3c94-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="b3c94-150">Write Paths</span></span>



| <span data-ttu-id="b3c94-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-151">Order</span></span> | <span data-ttu-id="b3c94-152">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-152">Path</span></span>                            | <span data-ttu-id="b3c94-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="b3c94-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="b3c94-154">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-154">1</span></span>     | <span data-ttu-id="b3c94-155">/ИФД/ексиф/{ушорт = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="b3c94-156">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-156">2</span></span>     | <span data-ttu-id="b3c94-157">/ИФД/КСМП/ексиф: Шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3c94-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="b3c94-158">Remove Paths</span></span>



| <span data-ttu-id="b3c94-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="b3c94-159">Order</span></span> | <span data-ttu-id="b3c94-160">Путь</span><span class="sxs-lookup"><span data-stu-id="b3c94-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="b3c94-161">1</span><span class="sxs-lookup"><span data-stu-id="b3c94-161">1</span></span>     | <span data-ttu-id="b3c94-162">/ИФД/ексиф/{ушорт = 37377}</span><span class="sxs-lookup"><span data-stu-id="b3c94-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="b3c94-163">2</span><span class="sxs-lookup"><span data-stu-id="b3c94-163">2</span></span>     | <span data-ttu-id="b3c94-164">/ИФД/КСМП/ексиф: шуттерспидвалуе</span><span class="sxs-lookup"><span data-stu-id="b3c94-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3c94-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3c94-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3c94-166">См. также</span><span class="sxs-lookup"><span data-stu-id="b3c94-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3c94-167">System. photo. Шуттерспид</span><span class="sxs-lookup"><span data-stu-id="b3c94-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
