---
description: Политика метаданных фотографии для свойства System. photo. Программоде.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Политика метаданных фото для System. photo. Программоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999124"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="0262a-103">Политика метаданных фото для System. photo. Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="0262a-104">Политика метаданных фотографии для свойства [System. photo. программоде](../properties/props-system-photo-programmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0262a-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0262a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0262a-105">PKEY</span></span>

<span data-ttu-id="0262a-106">\_Программоде фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="0262a-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="0262a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="0262a-107">Containers</span></span>

<span data-ttu-id="0262a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0262a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0262a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0262a-109">Read-Only</span></span>

<span data-ttu-id="0262a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="0262a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0262a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="0262a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0262a-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="0262a-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="0262a-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="0262a-113">Input Type</span></span>

<span data-ttu-id="0262a-114">UShort</span><span class="sxs-lookup"><span data-stu-id="0262a-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0262a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="0262a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0262a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="0262a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0262a-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="0262a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0262a-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0262a-118">Read Paths</span></span>



| <span data-ttu-id="0262a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-119">Order</span></span> | <span data-ttu-id="0262a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-120">Path</span></span>                          | <span data-ttu-id="0262a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0262a-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0262a-122">1</span><span class="sxs-lookup"><span data-stu-id="0262a-122">1</span></span>     | <span data-ttu-id="0262a-123">/APP1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="0262a-124">ushort</span><span class="sxs-lookup"><span data-stu-id="0262a-124">ushort</span></span>      |
| <span data-ttu-id="0262a-125">2</span><span class="sxs-lookup"><span data-stu-id="0262a-125">2</span></span>     | <span data-ttu-id="0262a-126">/КСМП/ексиф: Експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="0262a-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-127">unicode</span></span>     |
| <span data-ttu-id="0262a-128">3</span><span class="sxs-lookup"><span data-stu-id="0262a-128">3</span></span>     | <span data-ttu-id="0262a-129">/КСМП/ексиф: Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="0262a-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0262a-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0262a-131">Write Paths</span></span>



| <span data-ttu-id="0262a-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-132">Order</span></span> | <span data-ttu-id="0262a-133">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-133">Path</span></span>                          | <span data-ttu-id="0262a-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0262a-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0262a-135">1</span><span class="sxs-lookup"><span data-stu-id="0262a-135">1</span></span>     | <span data-ttu-id="0262a-136">/APP1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="0262a-137">ushort</span><span class="sxs-lookup"><span data-stu-id="0262a-137">ushort</span></span>      |
| <span data-ttu-id="0262a-138">2</span><span class="sxs-lookup"><span data-stu-id="0262a-138">2</span></span>     | <span data-ttu-id="0262a-139">/КСМП/ексиф: Експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="0262a-140">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-140">unicode</span></span>     |
| <span data-ttu-id="0262a-141">3</span><span class="sxs-lookup"><span data-stu-id="0262a-141">3</span></span>     | <span data-ttu-id="0262a-142">/КСМП/ексиф: Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="0262a-143">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0262a-144">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0262a-144">Remove Paths</span></span>



| <span data-ttu-id="0262a-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-145">Order</span></span> | <span data-ttu-id="0262a-146">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0262a-147">1</span><span class="sxs-lookup"><span data-stu-id="0262a-147">1</span></span>     | <span data-ttu-id="0262a-148">/APP1/IFD/EXIF/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="0262a-149">2</span><span class="sxs-lookup"><span data-stu-id="0262a-149">2</span></span>     | <span data-ttu-id="0262a-150">/КСМП/ексиф: експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="0262a-151">3</span><span class="sxs-lookup"><span data-stu-id="0262a-151">3</span></span>     | <span data-ttu-id="0262a-152">/КСМП/ексиф: программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="0262a-153">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="0262a-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0262a-154">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0262a-154">Read Paths</span></span>



| <span data-ttu-id="0262a-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-155">Order</span></span> | <span data-ttu-id="0262a-156">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-156">Path</span></span>                          | <span data-ttu-id="0262a-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0262a-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0262a-158">1</span><span class="sxs-lookup"><span data-stu-id="0262a-158">1</span></span>     | <span data-ttu-id="0262a-159">/ИФД/ексиф/{ушорт = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="0262a-160">ushort</span><span class="sxs-lookup"><span data-stu-id="0262a-160">ushort</span></span>      |
| <span data-ttu-id="0262a-161">2</span><span class="sxs-lookup"><span data-stu-id="0262a-161">2</span></span>     | <span data-ttu-id="0262a-162">/ИФД/КСМП/ексиф: Експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="0262a-163">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-163">unicode</span></span>     |
| <span data-ttu-id="0262a-164">3</span><span class="sxs-lookup"><span data-stu-id="0262a-164">3</span></span>     | <span data-ttu-id="0262a-165">/ИФД/КСМП/ексиф: Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="0262a-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0262a-167">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0262a-167">Write Paths</span></span>



| <span data-ttu-id="0262a-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-168">Order</span></span> | <span data-ttu-id="0262a-169">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-169">Path</span></span>                          | <span data-ttu-id="0262a-170">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0262a-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0262a-171">1</span><span class="sxs-lookup"><span data-stu-id="0262a-171">1</span></span>     | <span data-ttu-id="0262a-172">/ИФД/ексиф/{ушорт = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="0262a-173">ushort</span><span class="sxs-lookup"><span data-stu-id="0262a-173">ushort</span></span>      |
| <span data-ttu-id="0262a-174">2</span><span class="sxs-lookup"><span data-stu-id="0262a-174">2</span></span>     | <span data-ttu-id="0262a-175">/ИФД/КСМП/ексиф: Експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="0262a-176">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-176">unicode</span></span>     |
| <span data-ttu-id="0262a-177">3</span><span class="sxs-lookup"><span data-stu-id="0262a-177">3</span></span>     | <span data-ttu-id="0262a-178">/ИФД/КСМП/ексиф: Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="0262a-179">Юникод</span><span class="sxs-lookup"><span data-stu-id="0262a-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0262a-180">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0262a-180">Remove Paths</span></span>



| <span data-ttu-id="0262a-181">Заказ</span><span class="sxs-lookup"><span data-stu-id="0262a-181">Order</span></span> | <span data-ttu-id="0262a-182">Путь</span><span class="sxs-lookup"><span data-stu-id="0262a-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0262a-183">1</span><span class="sxs-lookup"><span data-stu-id="0262a-183">1</span></span>     | <span data-ttu-id="0262a-184">/ИФД/ексиф/{ушорт = 34850}</span><span class="sxs-lookup"><span data-stu-id="0262a-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="0262a-185">2</span><span class="sxs-lookup"><span data-stu-id="0262a-185">2</span></span>     | <span data-ttu-id="0262a-186">/ИФД/КСМП/ексиф: експосурепрограм</span><span class="sxs-lookup"><span data-stu-id="0262a-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="0262a-187">3</span><span class="sxs-lookup"><span data-stu-id="0262a-187">3</span></span>     | <span data-ttu-id="0262a-188">/ИФД/КСМП/ексиф: программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="0262a-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0262a-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0262a-190">См. также</span><span class="sxs-lookup"><span data-stu-id="0262a-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0262a-191">System. photo. Программоде</span><span class="sxs-lookup"><span data-stu-id="0262a-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
