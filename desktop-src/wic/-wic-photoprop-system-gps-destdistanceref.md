---
description: Политика метаданных фотографии для свойства System. GPS. Дестдистанцереф.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Политика метаданных фотографии System. GPS. Дестдистанцереф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684399"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="2e166-103">Политика метаданных фотографии System. GPS. Дестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="2e166-104">Политика метаданных фотографии для свойства [System. GPS. дестдистанцереф](../properties/props-system-gps-destdistanceref.md) .</span><span class="sxs-lookup"><span data-stu-id="2e166-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2e166-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2e166-105">PKEY</span></span>

<span data-ttu-id="2e166-106">PKEY \_ дестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="2e166-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="2e166-107">Containers</span></span>

<span data-ttu-id="2e166-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2e166-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2e166-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e166-109">Read-Only</span></span>

<span data-ttu-id="2e166-110">Нет</span><span class="sxs-lookup"><span data-stu-id="2e166-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2e166-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="2e166-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2e166-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="2e166-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="2e166-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="2e166-113">Input Type</span></span>

<span data-ttu-id="2e166-114">\_Принимаются VT LPWSTR или VT \_ LPSTR.</span><span class="sxs-lookup"><span data-stu-id="2e166-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2e166-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="2e166-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2e166-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="2e166-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="2e166-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="2e166-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2e166-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="2e166-118">Read Paths</span></span>



| <span data-ttu-id="2e166-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-119">Order</span></span> | <span data-ttu-id="2e166-120">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-120">Path</span></span>                         | <span data-ttu-id="2e166-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2e166-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2e166-122">1</span><span class="sxs-lookup"><span data-stu-id="2e166-122">1</span></span>     | <span data-ttu-id="2e166-123">/APP1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="2e166-124">ascii</span><span class="sxs-lookup"><span data-stu-id="2e166-124">ascii</span></span>       |
| <span data-ttu-id="2e166-125">2</span><span class="sxs-lookup"><span data-stu-id="2e166-125">2</span></span>     | <span data-ttu-id="2e166-126">/КСМП/ексиф: Гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="2e166-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="2e166-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2e166-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="2e166-128">Write Paths</span></span>



| <span data-ttu-id="2e166-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-129">Order</span></span> | <span data-ttu-id="2e166-130">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-130">Path</span></span>                         | <span data-ttu-id="2e166-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2e166-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2e166-132">1</span><span class="sxs-lookup"><span data-stu-id="2e166-132">1</span></span>     | <span data-ttu-id="2e166-133">/APP1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="2e166-134">ascii</span><span class="sxs-lookup"><span data-stu-id="2e166-134">ascii</span></span>       |
| <span data-ttu-id="2e166-135">2</span><span class="sxs-lookup"><span data-stu-id="2e166-135">2</span></span>     | <span data-ttu-id="2e166-136">/КСМП/ексиф: Гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="2e166-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="2e166-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2e166-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="2e166-138">Remove Paths</span></span>



| <span data-ttu-id="2e166-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-139">Order</span></span> | <span data-ttu-id="2e166-140">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="2e166-141">1</span><span class="sxs-lookup"><span data-stu-id="2e166-141">1</span></span>     | <span data-ttu-id="2e166-142">/APP1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="2e166-143">2</span><span class="sxs-lookup"><span data-stu-id="2e166-143">2</span></span>     | <span data-ttu-id="2e166-144">/КСМП/ексиф: гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="2e166-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="2e166-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2e166-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="2e166-146">Read Paths</span></span>



| <span data-ttu-id="2e166-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-147">Order</span></span> | <span data-ttu-id="2e166-148">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-148">Path</span></span>                             | <span data-ttu-id="2e166-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2e166-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="2e166-150">1</span><span class="sxs-lookup"><span data-stu-id="2e166-150">1</span></span>     | <span data-ttu-id="2e166-151">/ИФД/ГПС/{ушорт = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="2e166-152">ascii</span><span class="sxs-lookup"><span data-stu-id="2e166-152">ascii</span></span>       |
| <span data-ttu-id="2e166-153">2</span><span class="sxs-lookup"><span data-stu-id="2e166-153">2</span></span>     | <span data-ttu-id="2e166-154">/ИФД/КСМП/ексиф: Гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="2e166-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="2e166-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2e166-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="2e166-156">Write Paths</span></span>



| <span data-ttu-id="2e166-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-157">Order</span></span> | <span data-ttu-id="2e166-158">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-158">Path</span></span>                             | <span data-ttu-id="2e166-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="2e166-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="2e166-160">1</span><span class="sxs-lookup"><span data-stu-id="2e166-160">1</span></span>     | <span data-ttu-id="2e166-161">/ИФД/ГПС/{ушорт = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="2e166-162">ascii</span><span class="sxs-lookup"><span data-stu-id="2e166-162">ascii</span></span>       |
| <span data-ttu-id="2e166-163">2</span><span class="sxs-lookup"><span data-stu-id="2e166-163">2</span></span>     | <span data-ttu-id="2e166-164">/ИФД/КСМП/ексиф: Гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="2e166-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="2e166-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2e166-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="2e166-166">Remove Paths</span></span>



| <span data-ttu-id="2e166-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="2e166-167">Order</span></span> | <span data-ttu-id="2e166-168">Путь</span><span class="sxs-lookup"><span data-stu-id="2e166-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="2e166-169">1</span><span class="sxs-lookup"><span data-stu-id="2e166-169">1</span></span>     | <span data-ttu-id="2e166-170">/ИФД/ГПС/{ушорт = 25}</span><span class="sxs-lookup"><span data-stu-id="2e166-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="2e166-171">2</span><span class="sxs-lookup"><span data-stu-id="2e166-171">2</span></span>     | <span data-ttu-id="2e166-172">/ИФД/КСМП/ексиф: гпсдестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2e166-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e166-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e166-174">См. также</span><span class="sxs-lookup"><span data-stu-id="2e166-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e166-175">System. GPS. Дестдистанцереф</span><span class="sxs-lookup"><span data-stu-id="2e166-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
