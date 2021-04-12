---
description: Политика метаданных фотографии для свойства System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Политика метаданных фотографии System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348595"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="5710b-103">Политика метаданных фотографии System. Comment</span><span class="sxs-lookup"><span data-stu-id="5710b-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="5710b-104">Политика метаданных фотографии для свойства [System. Comment](../properties/props-system-comment.md) .</span><span class="sxs-lookup"><span data-stu-id="5710b-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5710b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5710b-105">PKEY</span></span>

<span data-ttu-id="5710b-106">\_Комментарий PKEY</span><span class="sxs-lookup"><span data-stu-id="5710b-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="5710b-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="5710b-107">Containers</span></span>

<span data-ttu-id="5710b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5710b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5710b-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5710b-109">Read-Only</span></span>

<span data-ttu-id="5710b-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5710b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5710b-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5710b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5710b-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5710b-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="5710b-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5710b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="5710b-114">VT \_ LPWSTR или VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5710b-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5710b-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="5710b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5710b-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="5710b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5710b-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="5710b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5710b-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="5710b-118">Read Paths</span></span>



| <span data-ttu-id="5710b-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-119">Order</span></span> | <span data-ttu-id="5710b-120">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-120">Path</span></span>                                | <span data-ttu-id="5710b-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5710b-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="5710b-122">1</span><span class="sxs-lookup"><span data-stu-id="5710b-122">1</span></span>     | <span data-ttu-id="5710b-123">/APP1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="5710b-124">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="5710b-124">unicode\_bytes</span></span> |
| <span data-ttu-id="5710b-125">2</span><span class="sxs-lookup"><span data-stu-id="5710b-125">2</span></span>     | <span data-ttu-id="5710b-126">/APP1/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="5710b-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="5710b-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="5710b-127">unicode</span></span>        |
| <span data-ttu-id="5710b-128">3</span><span class="sxs-lookup"><span data-stu-id="5710b-128">3</span></span>     | <span data-ttu-id="5710b-129">/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="5710b-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="5710b-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="5710b-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="5710b-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="5710b-131">Write Paths</span></span>



| <span data-ttu-id="5710b-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-132">Order</span></span> | <span data-ttu-id="5710b-133">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-133">Path</span></span>                     | <span data-ttu-id="5710b-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5710b-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="5710b-135">1</span><span class="sxs-lookup"><span data-stu-id="5710b-135">1</span></span>     | <span data-ttu-id="5710b-136">/APP1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="5710b-137">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="5710b-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="5710b-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="5710b-138">Remove Paths</span></span>



| <span data-ttu-id="5710b-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-139">Order</span></span> | <span data-ttu-id="5710b-140">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5710b-141">1</span><span class="sxs-lookup"><span data-stu-id="5710b-141">1</span></span>     | <span data-ttu-id="5710b-142">/APP1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="5710b-143">2</span><span class="sxs-lookup"><span data-stu-id="5710b-143">2</span></span>     | <span data-ttu-id="5710b-144">/APP1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="5710b-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="5710b-145">3</span><span class="sxs-lookup"><span data-stu-id="5710b-145">3</span></span>     | <span data-ttu-id="5710b-146">/КСМП/ексиф: Усеркоммент</span><span class="sxs-lookup"><span data-stu-id="5710b-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="5710b-147">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="5710b-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5710b-148">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="5710b-148">Read Paths</span></span>



| <span data-ttu-id="5710b-149">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-149">Order</span></span> | <span data-ttu-id="5710b-150">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-150">Path</span></span>                                    | <span data-ttu-id="5710b-151">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5710b-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="5710b-152">1</span><span class="sxs-lookup"><span data-stu-id="5710b-152">1</span></span>     | <span data-ttu-id="5710b-153">/ИФД/{ушорт = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="5710b-154">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="5710b-154">unicode\_bytes</span></span> |
| <span data-ttu-id="5710b-155">2</span><span class="sxs-lookup"><span data-stu-id="5710b-155">2</span></span>     | <span data-ttu-id="5710b-156">/ИФД/{ушорт = 37510}</span><span class="sxs-lookup"><span data-stu-id="5710b-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="5710b-157">Юникод</span><span class="sxs-lookup"><span data-stu-id="5710b-157">unicode</span></span>        |
| <span data-ttu-id="5710b-158">3</span><span class="sxs-lookup"><span data-stu-id="5710b-158">3</span></span>     | <span data-ttu-id="5710b-159">/ИФД/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="5710b-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="5710b-160">Юникод</span><span class="sxs-lookup"><span data-stu-id="5710b-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="5710b-161">Пути записи</span><span class="sxs-lookup"><span data-stu-id="5710b-161">Write Paths</span></span>



| <span data-ttu-id="5710b-162">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-162">Order</span></span> | <span data-ttu-id="5710b-163">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-163">Path</span></span>                | <span data-ttu-id="5710b-164">Формат диска</span><span class="sxs-lookup"><span data-stu-id="5710b-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="5710b-165">1</span><span class="sxs-lookup"><span data-stu-id="5710b-165">1</span></span>     | <span data-ttu-id="5710b-166">/ИФД/{ушорт = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="5710b-167">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="5710b-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="5710b-168">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="5710b-168">Remove Paths</span></span>



| <span data-ttu-id="5710b-169">Заказ</span><span class="sxs-lookup"><span data-stu-id="5710b-169">Order</span></span> | <span data-ttu-id="5710b-170">Путь</span><span class="sxs-lookup"><span data-stu-id="5710b-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="5710b-171">1</span><span class="sxs-lookup"><span data-stu-id="5710b-171">1</span></span>     | <span data-ttu-id="5710b-172">/ИФД/{ушорт = 40092}</span><span class="sxs-lookup"><span data-stu-id="5710b-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="5710b-173">2</span><span class="sxs-lookup"><span data-stu-id="5710b-173">2</span></span>     | <span data-ttu-id="5710b-174">/ИФД/{ушорт = 37510}</span><span class="sxs-lookup"><span data-stu-id="5710b-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="5710b-175">3</span><span class="sxs-lookup"><span data-stu-id="5710b-175">3</span></span>     | <span data-ttu-id="5710b-176">/ИФД/КСМП/ексиф: Усеркоммент</span><span class="sxs-lookup"><span data-stu-id="5710b-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5710b-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5710b-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5710b-178">См. также</span><span class="sxs-lookup"><span data-stu-id="5710b-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5710b-179">System. комментарий</span><span class="sxs-lookup"><span data-stu-id="5710b-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
