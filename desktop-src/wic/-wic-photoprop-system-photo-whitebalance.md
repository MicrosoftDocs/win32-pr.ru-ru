---
description: Политика метаданных фотографии для свойства System. photo. Вхитебаланце.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Политика метаданных фото для System. photo. Вхитебаланце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702741"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="14774-103">Политика метаданных фото для System. photo. Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="14774-104">Политика метаданных фотографии для свойства [System. photo. вхитебаланце](../properties/props-system-photo-whitebalance.md) .</span><span class="sxs-lookup"><span data-stu-id="14774-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="14774-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="14774-105">PKEY</span></span>

<span data-ttu-id="14774-106">\_Вхитебаланце фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="14774-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="14774-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="14774-107">Containers</span></span>

<span data-ttu-id="14774-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="14774-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="14774-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="14774-109">Read-Only</span></span>

<span data-ttu-id="14774-110">Нет</span><span class="sxs-lookup"><span data-stu-id="14774-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="14774-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="14774-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="14774-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="14774-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="14774-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="14774-113">Input Type</span></span>

<span data-ttu-id="14774-114">UShort</span><span class="sxs-lookup"><span data-stu-id="14774-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="14774-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="14774-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="14774-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="14774-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="14774-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="14774-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="14774-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="14774-118">Read Paths</span></span>



| <span data-ttu-id="14774-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-119">Order</span></span> | <span data-ttu-id="14774-120">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-120">Path</span></span>                          | <span data-ttu-id="14774-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14774-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="14774-122">1</span><span class="sxs-lookup"><span data-stu-id="14774-122">1</span></span>     | <span data-ttu-id="14774-123">/APP1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="14774-124">ushort</span><span class="sxs-lookup"><span data-stu-id="14774-124">ushort</span></span>      |
| <span data-ttu-id="14774-125">2</span><span class="sxs-lookup"><span data-stu-id="14774-125">2</span></span>     | <span data-ttu-id="14774-126">/КСМП/ексиф: Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="14774-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="14774-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14774-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="14774-128">Write Paths</span></span>



| <span data-ttu-id="14774-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-129">Order</span></span> | <span data-ttu-id="14774-130">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-130">Path</span></span>                          | <span data-ttu-id="14774-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14774-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="14774-132">1</span><span class="sxs-lookup"><span data-stu-id="14774-132">1</span></span>     | <span data-ttu-id="14774-133">/APP1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="14774-134">ushort</span><span class="sxs-lookup"><span data-stu-id="14774-134">ushort</span></span>      |
| <span data-ttu-id="14774-135">2</span><span class="sxs-lookup"><span data-stu-id="14774-135">2</span></span>     | <span data-ttu-id="14774-136">/КСМП/ексиф: Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="14774-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="14774-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14774-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="14774-138">Remove Paths</span></span>



| <span data-ttu-id="14774-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-139">Order</span></span> | <span data-ttu-id="14774-140">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="14774-141">1</span><span class="sxs-lookup"><span data-stu-id="14774-141">1</span></span>     | <span data-ttu-id="14774-142">/APP1/IFD/EXIF/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="14774-143">2</span><span class="sxs-lookup"><span data-stu-id="14774-143">2</span></span>     | <span data-ttu-id="14774-144">/КСМП/ексиф: вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="14774-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="14774-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="14774-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="14774-146">Read Paths</span></span>



| <span data-ttu-id="14774-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-147">Order</span></span> | <span data-ttu-id="14774-148">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-148">Path</span></span>                       | <span data-ttu-id="14774-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14774-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="14774-150">1</span><span class="sxs-lookup"><span data-stu-id="14774-150">1</span></span>     | <span data-ttu-id="14774-151">/ИФД/ексиф/{ушорт = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="14774-152">ushort</span><span class="sxs-lookup"><span data-stu-id="14774-152">ushort</span></span>      |
| <span data-ttu-id="14774-153">2</span><span class="sxs-lookup"><span data-stu-id="14774-153">2</span></span>     | <span data-ttu-id="14774-154">/ИФД/КСМП/ексиф: Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="14774-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="14774-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="14774-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="14774-156">Write Paths</span></span>



| <span data-ttu-id="14774-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-157">Order</span></span> | <span data-ttu-id="14774-158">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-158">Path</span></span>                       | <span data-ttu-id="14774-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="14774-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="14774-160">1</span><span class="sxs-lookup"><span data-stu-id="14774-160">1</span></span>     | <span data-ttu-id="14774-161">/ИФД/ексиф/{ушорт = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="14774-162">ushort</span><span class="sxs-lookup"><span data-stu-id="14774-162">ushort</span></span>      |
| <span data-ttu-id="14774-163">2</span><span class="sxs-lookup"><span data-stu-id="14774-163">2</span></span>     | <span data-ttu-id="14774-164">/ИФД/КСМП/ексиф: Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="14774-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="14774-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="14774-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="14774-166">Remove Paths</span></span>



| <span data-ttu-id="14774-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="14774-167">Order</span></span> | <span data-ttu-id="14774-168">Путь</span><span class="sxs-lookup"><span data-stu-id="14774-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="14774-169">1</span><span class="sxs-lookup"><span data-stu-id="14774-169">1</span></span>     | <span data-ttu-id="14774-170">/ИФД/ексиф/{ушорт = 41987}</span><span class="sxs-lookup"><span data-stu-id="14774-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="14774-171">2</span><span class="sxs-lookup"><span data-stu-id="14774-171">2</span></span>     | <span data-ttu-id="14774-172">/ИФД/КСМП/ексиф: вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14774-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14774-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="14774-174">См. также</span><span class="sxs-lookup"><span data-stu-id="14774-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14774-175">System. photo. Вхитебаланце</span><span class="sxs-lookup"><span data-stu-id="14774-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
