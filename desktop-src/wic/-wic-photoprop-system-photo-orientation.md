---
description: Политика метаданных фотографии для свойства System. photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Политика метаданных фотографии System. photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081305"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="f50a6-103">Политика метаданных фотографии System. photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="f50a6-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="f50a6-104">Политика метаданных фотографии для свойства [System. photo. Orientation](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="f50a6-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f50a6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f50a6-105">PKEY</span></span>

<span data-ttu-id="f50a6-106">\_Ориентация фотографии \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="f50a6-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="f50a6-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="f50a6-107">Containers</span></span>

<span data-ttu-id="f50a6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f50a6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f50a6-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f50a6-109">Read-Only</span></span>

<span data-ttu-id="f50a6-110">Нет</span><span class="sxs-lookup"><span data-stu-id="f50a6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f50a6-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="f50a6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f50a6-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="f50a6-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="f50a6-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="f50a6-113">Input Type</span></span>

<span data-ttu-id="f50a6-114">UShort</span><span class="sxs-lookup"><span data-stu-id="f50a6-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f50a6-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="f50a6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f50a6-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="f50a6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="f50a6-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="f50a6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="f50a6-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="f50a6-118">Read Paths</span></span>



| <span data-ttu-id="f50a6-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-119">Order</span></span> | <span data-ttu-id="f50a6-120">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-120">Path</span></span>                   | <span data-ttu-id="f50a6-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f50a6-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f50a6-122">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-122">1</span></span>     | <span data-ttu-id="f50a6-123">/APP1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="f50a6-124">ushort</span><span class="sxs-lookup"><span data-stu-id="f50a6-124">ushort</span></span>      |
| <span data-ttu-id="f50a6-125">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-125">2</span></span>     | <span data-ttu-id="f50a6-126">/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="f50a6-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="f50a6-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f50a6-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="f50a6-128">Write Paths</span></span>



| <span data-ttu-id="f50a6-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-129">Order</span></span> | <span data-ttu-id="f50a6-130">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-130">Path</span></span>                   | <span data-ttu-id="f50a6-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f50a6-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="f50a6-132">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-132">1</span></span>     | <span data-ttu-id="f50a6-133">/APP1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="f50a6-134">ushort</span><span class="sxs-lookup"><span data-stu-id="f50a6-134">ushort</span></span>      |
| <span data-ttu-id="f50a6-135">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-135">2</span></span>     | <span data-ttu-id="f50a6-136">/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="f50a6-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="f50a6-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f50a6-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="f50a6-138">Remove Paths</span></span>



| <span data-ttu-id="f50a6-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-139">Order</span></span> | <span data-ttu-id="f50a6-140">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="f50a6-141">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-141">1</span></span>     | <span data-ttu-id="f50a6-142">/APP1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="f50a6-143">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-143">2</span></span>     | <span data-ttu-id="f50a6-144">/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="f50a6-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="f50a6-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f50a6-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="f50a6-146">Read Paths</span></span>



| <span data-ttu-id="f50a6-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-147">Order</span></span> | <span data-ttu-id="f50a6-148">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-148">Path</span></span>                      | <span data-ttu-id="f50a6-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f50a6-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f50a6-150">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-150">1</span></span>     | <span data-ttu-id="f50a6-151">/ИФД/{ушорт = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="f50a6-152">ushort</span><span class="sxs-lookup"><span data-stu-id="f50a6-152">ushort</span></span>      |
| <span data-ttu-id="f50a6-153">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-153">2</span></span>     | <span data-ttu-id="f50a6-154">/ИФД/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="f50a6-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="f50a6-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f50a6-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="f50a6-156">Write Paths</span></span>



| <span data-ttu-id="f50a6-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-157">Order</span></span> | <span data-ttu-id="f50a6-158">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-158">Path</span></span>                      | <span data-ttu-id="f50a6-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f50a6-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f50a6-160">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-160">1</span></span>     | <span data-ttu-id="f50a6-161">/ИФД/{ушорт = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="f50a6-162">ushort</span><span class="sxs-lookup"><span data-stu-id="f50a6-162">ushort</span></span>      |
| <span data-ttu-id="f50a6-163">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-163">2</span></span>     | <span data-ttu-id="f50a6-164">/ИФД/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="f50a6-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="f50a6-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f50a6-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="f50a6-166">Remove Paths</span></span>



| <span data-ttu-id="f50a6-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="f50a6-167">Order</span></span> | <span data-ttu-id="f50a6-168">Путь</span><span class="sxs-lookup"><span data-stu-id="f50a6-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f50a6-169">1</span><span class="sxs-lookup"><span data-stu-id="f50a6-169">1</span></span>     | <span data-ttu-id="f50a6-170">/ИФД/{ушорт = 274}</span><span class="sxs-lookup"><span data-stu-id="f50a6-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="f50a6-171">2</span><span class="sxs-lookup"><span data-stu-id="f50a6-171">2</span></span>     | <span data-ttu-id="f50a6-172">/ИФД/КСМП/Тифф: ориентация</span><span class="sxs-lookup"><span data-stu-id="f50a6-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f50a6-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f50a6-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f50a6-174">См. также</span><span class="sxs-lookup"><span data-stu-id="f50a6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50a6-175">System. фото. Orientation</span><span class="sxs-lookup"><span data-stu-id="f50a6-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
