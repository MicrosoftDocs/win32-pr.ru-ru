---
description: Политика метаданных фотографии для свойства System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Политика метаданных фотографии System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683568"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="7298a-103">Политика метаданных фотографии System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="7298a-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="7298a-104">Политика метаданных фотографии для свойства [System. Image. Compression](../properties/props-system-image-compression.md) .</span><span class="sxs-lookup"><span data-stu-id="7298a-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7298a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7298a-105">PKEY</span></span>

<span data-ttu-id="7298a-106">\_Сжатие образа \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="7298a-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="7298a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="7298a-107">Containers</span></span>

<span data-ttu-id="7298a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7298a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7298a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7298a-109">Read-Only</span></span>

<span data-ttu-id="7298a-110">Да</span><span class="sxs-lookup"><span data-stu-id="7298a-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7298a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="7298a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7298a-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="7298a-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="7298a-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="7298a-113">Input Type</span></span>

<span data-ttu-id="7298a-114">UShort</span><span class="sxs-lookup"><span data-stu-id="7298a-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7298a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="7298a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7298a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="7298a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7298a-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="7298a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7298a-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="7298a-118">Read Paths</span></span>



| <span data-ttu-id="7298a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-119">Order</span></span> | <span data-ttu-id="7298a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-120">Path</span></span>                   | <span data-ttu-id="7298a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7298a-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7298a-122">1</span><span class="sxs-lookup"><span data-stu-id="7298a-122">1</span></span>     | <span data-ttu-id="7298a-123">/APP1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="7298a-124">ushort</span><span class="sxs-lookup"><span data-stu-id="7298a-124">ushort</span></span>      |
| <span data-ttu-id="7298a-125">2</span><span class="sxs-lookup"><span data-stu-id="7298a-125">2</span></span>     | <span data-ttu-id="7298a-126">/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="7298a-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="7298a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7298a-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="7298a-128">Write Paths</span></span>



| <span data-ttu-id="7298a-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-129">Order</span></span> | <span data-ttu-id="7298a-130">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-130">Path</span></span>                   | <span data-ttu-id="7298a-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7298a-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7298a-132">1</span><span class="sxs-lookup"><span data-stu-id="7298a-132">1</span></span>     | <span data-ttu-id="7298a-133">/APP1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="7298a-134">ushort</span><span class="sxs-lookup"><span data-stu-id="7298a-134">ushort</span></span>      |
| <span data-ttu-id="7298a-135">2</span><span class="sxs-lookup"><span data-stu-id="7298a-135">2</span></span>     | <span data-ttu-id="7298a-136">/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="7298a-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="7298a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7298a-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="7298a-138">Remove Paths</span></span>



| <span data-ttu-id="7298a-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-139">Order</span></span> | <span data-ttu-id="7298a-140">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="7298a-141">1</span><span class="sxs-lookup"><span data-stu-id="7298a-141">1</span></span>     | <span data-ttu-id="7298a-142">/APP1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="7298a-143">2</span><span class="sxs-lookup"><span data-stu-id="7298a-143">2</span></span>     | <span data-ttu-id="7298a-144">/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="7298a-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="7298a-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7298a-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="7298a-146">Read Paths</span></span>



| <span data-ttu-id="7298a-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-147">Order</span></span> | <span data-ttu-id="7298a-148">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-148">Path</span></span>                      | <span data-ttu-id="7298a-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7298a-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7298a-150">1</span><span class="sxs-lookup"><span data-stu-id="7298a-150">1</span></span>     | <span data-ttu-id="7298a-151">/ИФД/{ушорт = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="7298a-152">ushort</span><span class="sxs-lookup"><span data-stu-id="7298a-152">ushort</span></span>      |
| <span data-ttu-id="7298a-153">2</span><span class="sxs-lookup"><span data-stu-id="7298a-153">2</span></span>     | <span data-ttu-id="7298a-154">/ИФД/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="7298a-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="7298a-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7298a-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="7298a-156">Write Paths</span></span>



| <span data-ttu-id="7298a-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-157">Order</span></span> | <span data-ttu-id="7298a-158">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-158">Path</span></span>                      | <span data-ttu-id="7298a-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="7298a-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7298a-160">1</span><span class="sxs-lookup"><span data-stu-id="7298a-160">1</span></span>     | <span data-ttu-id="7298a-161">/ИФД/{ушорт = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="7298a-162">ushort</span><span class="sxs-lookup"><span data-stu-id="7298a-162">ushort</span></span>      |
| <span data-ttu-id="7298a-163">2</span><span class="sxs-lookup"><span data-stu-id="7298a-163">2</span></span>     | <span data-ttu-id="7298a-164">/ИФД/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="7298a-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="7298a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7298a-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="7298a-166">Remove Paths</span></span>



| <span data-ttu-id="7298a-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="7298a-167">Order</span></span> | <span data-ttu-id="7298a-168">Путь</span><span class="sxs-lookup"><span data-stu-id="7298a-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="7298a-169">1</span><span class="sxs-lookup"><span data-stu-id="7298a-169">1</span></span>     | <span data-ttu-id="7298a-170">/ИФД/{ушорт = 259}</span><span class="sxs-lookup"><span data-stu-id="7298a-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="7298a-171">2</span><span class="sxs-lookup"><span data-stu-id="7298a-171">2</span></span>     | <span data-ttu-id="7298a-172">/ИФД/КСМП/Тифф: сжатие</span><span class="sxs-lookup"><span data-stu-id="7298a-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7298a-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7298a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7298a-174">См. также</span><span class="sxs-lookup"><span data-stu-id="7298a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7298a-175">System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="7298a-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
