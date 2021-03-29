---
description: Политика метаданных фотографии для свойства System. photo. Субжектдистанце.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Политика метаданных фото для System. photo. Субжектдистанце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911947"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="a1cb7-103">Политика метаданных фото для System. photo. Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="a1cb7-104">Политика метаданных фотографии для свойства [System. photo. субжектдистанце](../properties/props-system-photo-subjectdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="a1cb7-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a1cb7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a1cb7-105">PKEY</span></span>

<span data-ttu-id="a1cb7-106">\_Субжектдистанце фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="a1cb7-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="a1cb7-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="a1cb7-107">Containers</span></span>

<span data-ttu-id="a1cb7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a1cb7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a1cb7-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1cb7-109">Read-Only</span></span>

<span data-ttu-id="a1cb7-110">Да</span><span class="sxs-lookup"><span data-stu-id="a1cb7-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a1cb7-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a1cb7-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="a1cb7-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a1cb7-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="a1cb7-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a1cb7-114">Это значение формируется из System. photo. Субжектдистанценумератор и System. photo. Субжектдистанцеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="a1cb7-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="a1cb7-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="a1cb7-115">It cannot be written directly.</span></span> <span data-ttu-id="a1cb7-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="a1cb7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a1cb7-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="a1cb7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a1cb7-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a1cb7-118">Read Paths</span></span>



| <span data-ttu-id="a1cb7-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-119">Order</span></span> | <span data-ttu-id="a1cb7-120">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-120">Path</span></span>                          | <span data-ttu-id="a1cb7-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a1cb7-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a1cb7-122">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-122">1</span></span>     | <span data-ttu-id="a1cb7-123">/APP1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="a1cb7-124">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-124">2</span></span>     | <span data-ttu-id="a1cb7-125">/КСМП/ексиф: Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="a1cb7-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a1cb7-126">Write Paths</span></span>



| <span data-ttu-id="a1cb7-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-127">Order</span></span> | <span data-ttu-id="a1cb7-128">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-128">Path</span></span>                          | <span data-ttu-id="a1cb7-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a1cb7-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a1cb7-130">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-130">1</span></span>     | <span data-ttu-id="a1cb7-131">/APP1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="a1cb7-132">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-132">2</span></span>     | <span data-ttu-id="a1cb7-133">/КСМП/ексиф: Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a1cb7-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a1cb7-134">Remove Paths</span></span>



| <span data-ttu-id="a1cb7-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-135">Order</span></span> | <span data-ttu-id="a1cb7-136">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a1cb7-137">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-137">1</span></span>     | <span data-ttu-id="a1cb7-138">/APP1/IFD/EXIF/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="a1cb7-139">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-139">2</span></span>     | <span data-ttu-id="a1cb7-140">/КСМП/ексиф: субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="a1cb7-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="a1cb7-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a1cb7-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a1cb7-142">Read Paths</span></span>



| <span data-ttu-id="a1cb7-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-143">Order</span></span> | <span data-ttu-id="a1cb7-144">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-144">Path</span></span>                          | <span data-ttu-id="a1cb7-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a1cb7-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a1cb7-146">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-146">1</span></span>     | <span data-ttu-id="a1cb7-147">/ИФД/ексиф/{ушорт = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="a1cb7-148">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-148">2</span></span>     | <span data-ttu-id="a1cb7-149">/ИФД/КСМП/ексиф: Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a1cb7-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a1cb7-150">Write Paths</span></span>



| <span data-ttu-id="a1cb7-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-151">Order</span></span> | <span data-ttu-id="a1cb7-152">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-152">Path</span></span>                          | <span data-ttu-id="a1cb7-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a1cb7-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a1cb7-154">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-154">1</span></span>     | <span data-ttu-id="a1cb7-155">/ИФД/ексиф/{ушорт = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="a1cb7-156">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-156">2</span></span>     | <span data-ttu-id="a1cb7-157">/ИФД/КСМП/ексиф: Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a1cb7-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a1cb7-158">Remove Paths</span></span>



| <span data-ttu-id="a1cb7-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="a1cb7-159">Order</span></span> | <span data-ttu-id="a1cb7-160">Путь</span><span class="sxs-lookup"><span data-stu-id="a1cb7-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a1cb7-161">1</span><span class="sxs-lookup"><span data-stu-id="a1cb7-161">1</span></span>     | <span data-ttu-id="a1cb7-162">/ИФД/ексиф/{ушорт = 37382}</span><span class="sxs-lookup"><span data-stu-id="a1cb7-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="a1cb7-163">2</span><span class="sxs-lookup"><span data-stu-id="a1cb7-163">2</span></span>     | <span data-ttu-id="a1cb7-164">/ИФД/КСМП/ексиф: субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a1cb7-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1cb7-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1cb7-166">См. также</span><span class="sxs-lookup"><span data-stu-id="a1cb7-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1cb7-167">System. photo. Субжектдистанце</span><span class="sxs-lookup"><span data-stu-id="a1cb7-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
