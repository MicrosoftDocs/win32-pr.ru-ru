---
description: Политика метаданных фотографии для свойства System. photo. Транскодедфорсинк.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Политика метаданных фото для System. photo. Транскодедфорсинк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911944"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="a3d2f-103">Политика метаданных фото для System. photo. Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="a3d2f-104">Политика метаданных фотографии для свойства [System. photo. транскодедфорсинк](../properties/props-system-photo-transcodedforsync.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d2f-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a3d2f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a3d2f-105">PKEY</span></span>

<span data-ttu-id="a3d2f-106">\_Транскодедфорсинк фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="a3d2f-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="a3d2f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="a3d2f-107">Containers</span></span>

<span data-ttu-id="a3d2f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a3d2f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a3d2f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3d2f-109">Read-Only</span></span>

<span data-ttu-id="a3d2f-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a3d2f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a3d2f-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a3d2f-112">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="a3d2f-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="a3d2f-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="a3d2f-113">Input Type</span></span>

<span data-ttu-id="a3d2f-114">Логическое.</span><span class="sxs-lookup"><span data-stu-id="a3d2f-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a3d2f-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="a3d2f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a3d2f-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="a3d2f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a3d2f-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="a3d2f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3d2f-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a3d2f-118">Read Paths</span></span>



| <span data-ttu-id="a3d2f-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-119">Order</span></span> | <span data-ttu-id="a3d2f-120">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-120">Path</span></span>                                  | <span data-ttu-id="a3d2f-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a3d2f-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="a3d2f-122">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-122">1</span></span>     | <span data-ttu-id="a3d2f-123">/APP1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="a3d2f-124">bool, \_ UShort</span><span class="sxs-lookup"><span data-stu-id="a3d2f-124">bool\_ushort</span></span> |
| <span data-ttu-id="a3d2f-125">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-125">2</span></span>     | <span data-ttu-id="a3d2f-126">/КСМП/микрософтфото: Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="a3d2f-127">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a3d2f-127">Write Paths</span></span>



| <span data-ttu-id="a3d2f-128">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-128">Order</span></span> | <span data-ttu-id="a3d2f-129">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-129">Path</span></span>                                  | <span data-ttu-id="a3d2f-130">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a3d2f-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="a3d2f-131">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-131">1</span></span>     | <span data-ttu-id="a3d2f-132">/APP1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="a3d2f-133">bool, \_ UShort</span><span class="sxs-lookup"><span data-stu-id="a3d2f-133">bool\_ushort</span></span> |
| <span data-ttu-id="a3d2f-134">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-134">2</span></span>     | <span data-ttu-id="a3d2f-135">/КСМП/микрософтфото: Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="a3d2f-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a3d2f-136">Remove Paths</span></span>



| <span data-ttu-id="a3d2f-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-137">Order</span></span> | <span data-ttu-id="a3d2f-138">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="a3d2f-139">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-139">1</span></span>     | <span data-ttu-id="a3d2f-140">/APP1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="a3d2f-141">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-141">2</span></span>     | <span data-ttu-id="a3d2f-142">/КСМП/микрософтфото: транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a3d2f-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="a3d2f-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a3d2f-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a3d2f-144">Read Paths</span></span>



| <span data-ttu-id="a3d2f-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-145">Order</span></span> | <span data-ttu-id="a3d2f-146">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-146">Path</span></span>                                      | <span data-ttu-id="a3d2f-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a3d2f-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="a3d2f-148">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-148">1</span></span>     | <span data-ttu-id="a3d2f-149">/ИФД/{ушорт = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="a3d2f-150">bool, \_ UShort</span><span class="sxs-lookup"><span data-stu-id="a3d2f-150">bool\_ushort</span></span> |
| <span data-ttu-id="a3d2f-151">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-151">2</span></span>     | <span data-ttu-id="a3d2f-152">/ИФД/КСМП/микрософтфото: Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="a3d2f-153">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a3d2f-153">Write Paths</span></span>



| <span data-ttu-id="a3d2f-154">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-154">Order</span></span> | <span data-ttu-id="a3d2f-155">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-155">Path</span></span>                                      | <span data-ttu-id="a3d2f-156">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a3d2f-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="a3d2f-157">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-157">1</span></span>     | <span data-ttu-id="a3d2f-158">/ИФД/{ушорт = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="a3d2f-159">bool, \_ UShort</span><span class="sxs-lookup"><span data-stu-id="a3d2f-159">bool\_ushort</span></span> |
| <span data-ttu-id="a3d2f-160">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-160">2</span></span>     | <span data-ttu-id="a3d2f-161">/ИФД/КСМП/микрософтфото: Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="a3d2f-162">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a3d2f-162">Remove Paths</span></span>



| <span data-ttu-id="a3d2f-163">Заказ</span><span class="sxs-lookup"><span data-stu-id="a3d2f-163">Order</span></span> | <span data-ttu-id="a3d2f-164">Путь</span><span class="sxs-lookup"><span data-stu-id="a3d2f-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="a3d2f-165">1</span><span class="sxs-lookup"><span data-stu-id="a3d2f-165">1</span></span>     | <span data-ttu-id="a3d2f-166">/ИФД/{ушорт = 18248}</span><span class="sxs-lookup"><span data-stu-id="a3d2f-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="a3d2f-167">2</span><span class="sxs-lookup"><span data-stu-id="a3d2f-167">2</span></span>     | <span data-ttu-id="a3d2f-168">/ИФД/КСМП/микрософтфото: транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a3d2f-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3d2f-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3d2f-170">См. также</span><span class="sxs-lookup"><span data-stu-id="a3d2f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3d2f-171">System. photo. Транскодедфорсинк</span><span class="sxs-lookup"><span data-stu-id="a3d2f-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
