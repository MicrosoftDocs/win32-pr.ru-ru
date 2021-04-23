---
description: Политика метаданных фотографии для свойства System. photo. Експосуретиме.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Политика метаданных фото для System. photo. Експосуретиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674004"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="e89d4-103">Политика метаданных фото для System. photo. Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="e89d4-104">Политика метаданных фотографии для свойства [System. photo. експосуретиме](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="e89d4-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e89d4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e89d4-105">PKEY</span></span>

<span data-ttu-id="e89d4-106">\_Експосуретиме фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="e89d4-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="e89d4-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e89d4-107">Containers</span></span>

<span data-ttu-id="e89d4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e89d4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e89d4-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e89d4-109">Read-Only</span></span>

<span data-ttu-id="e89d4-110">Да</span><span class="sxs-lookup"><span data-stu-id="e89d4-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e89d4-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e89d4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e89d4-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e89d4-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e89d4-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e89d4-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e89d4-114">Это значение формируется из System. photo. Експосуретименумератор и System. photo. Експосуретимеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="e89d4-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="e89d4-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="e89d4-115">It cannot be written directly.</span></span> <span data-ttu-id="e89d4-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e89d4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e89d4-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="e89d4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e89d4-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e89d4-118">Read Paths</span></span>



| <span data-ttu-id="e89d4-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-119">Order</span></span> | <span data-ttu-id="e89d4-120">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-120">Path</span></span>                          | <span data-ttu-id="e89d4-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e89d4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e89d4-122">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-122">1</span></span>     | <span data-ttu-id="e89d4-123">/APP1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="e89d4-124">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-124">2</span></span>     | <span data-ttu-id="e89d4-125">/КСМП/ексиф: Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="e89d4-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e89d4-126">Write Paths</span></span>



| <span data-ttu-id="e89d4-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-127">Order</span></span> | <span data-ttu-id="e89d4-128">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-128">Path</span></span>                          | <span data-ttu-id="e89d4-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e89d4-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e89d4-130">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-130">1</span></span>     | <span data-ttu-id="e89d4-131">/APP1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="e89d4-132">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-132">2</span></span>     | <span data-ttu-id="e89d4-133">/КСМП/ексиф: Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e89d4-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e89d4-134">Remove Paths</span></span>



| <span data-ttu-id="e89d4-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-135">Order</span></span> | <span data-ttu-id="e89d4-136">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e89d4-137">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-137">1</span></span>     | <span data-ttu-id="e89d4-138">/APP1/IFD/EXIF/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="e89d4-139">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-139">2</span></span>     | <span data-ttu-id="e89d4-140">/КСМП/ексиф: експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="e89d4-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="e89d4-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e89d4-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e89d4-142">Read Paths</span></span>



| <span data-ttu-id="e89d4-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-143">Order</span></span> | <span data-ttu-id="e89d4-144">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-144">Path</span></span>                       | <span data-ttu-id="e89d4-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e89d4-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e89d4-146">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-146">1</span></span>     | <span data-ttu-id="e89d4-147">/ИФД/ексиф/{ушорт = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="e89d4-148">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-148">2</span></span>     | <span data-ttu-id="e89d4-149">/ИФД/КСМП/ексиф: Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e89d4-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e89d4-150">Write Paths</span></span>



| <span data-ttu-id="e89d4-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-151">Order</span></span> | <span data-ttu-id="e89d4-152">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-152">Path</span></span>                       | <span data-ttu-id="e89d4-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e89d4-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="e89d4-154">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-154">1</span></span>     | <span data-ttu-id="e89d4-155">/ИФД/ексиф/{ушорт = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="e89d4-156">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-156">2</span></span>     | <span data-ttu-id="e89d4-157">/ИФД/КСМП/ексиф: Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e89d4-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e89d4-158">Remove Paths</span></span>



| <span data-ttu-id="e89d4-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="e89d4-159">Order</span></span> | <span data-ttu-id="e89d4-160">Путь</span><span class="sxs-lookup"><span data-stu-id="e89d4-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="e89d4-161">1</span><span class="sxs-lookup"><span data-stu-id="e89d4-161">1</span></span>     | <span data-ttu-id="e89d4-162">/ИФД/ексиф/{ушорт = 33434}</span><span class="sxs-lookup"><span data-stu-id="e89d4-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="e89d4-163">2</span><span class="sxs-lookup"><span data-stu-id="e89d4-163">2</span></span>     | <span data-ttu-id="e89d4-164">/ИФД/КСМП/ексиф: експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e89d4-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e89d4-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e89d4-166">См. также</span><span class="sxs-lookup"><span data-stu-id="e89d4-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e89d4-167">System. photo. Експосуретиме</span><span class="sxs-lookup"><span data-stu-id="e89d4-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
