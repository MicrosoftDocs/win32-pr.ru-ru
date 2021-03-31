---
description: Политика метаданных фотографии для свойства System. GPS. Траккреф.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Политика метаданных фотографии System. GPS. Траккреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272833"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="15c67-103">Политика метаданных фотографии System. GPS. Траккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="15c67-104">Политика метаданных фотографии для свойства [System. GPS. траккреф](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="15c67-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="15c67-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="15c67-105">PKEY</span></span>

<span data-ttu-id="15c67-106">PKEY \_ GPS \_ траккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="15c67-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="15c67-107">Containers</span></span>

<span data-ttu-id="15c67-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="15c67-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="15c67-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="15c67-109">Read-Only</span></span>

<span data-ttu-id="15c67-110">Нет</span><span class="sxs-lookup"><span data-stu-id="15c67-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="15c67-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="15c67-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="15c67-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="15c67-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="15c67-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="15c67-113">Input Type</span></span>

<span data-ttu-id="15c67-114">Строка</span><span class="sxs-lookup"><span data-stu-id="15c67-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="15c67-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="15c67-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="15c67-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="15c67-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="15c67-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="15c67-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="15c67-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="15c67-118">Read Paths</span></span>



| <span data-ttu-id="15c67-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-119">Order</span></span> | <span data-ttu-id="15c67-120">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-120">Path</span></span>                      | <span data-ttu-id="15c67-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="15c67-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="15c67-122">1</span><span class="sxs-lookup"><span data-stu-id="15c67-122">1</span></span>     | <span data-ttu-id="15c67-123">/APP1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="15c67-124">ascii</span><span class="sxs-lookup"><span data-stu-id="15c67-124">ascii</span></span>       |
| <span data-ttu-id="15c67-125">2</span><span class="sxs-lookup"><span data-stu-id="15c67-125">2</span></span>     | <span data-ttu-id="15c67-126">/КСМП/ексиф: Гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="15c67-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="15c67-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="15c67-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="15c67-128">Write Paths</span></span>



| <span data-ttu-id="15c67-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-129">Order</span></span> | <span data-ttu-id="15c67-130">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-130">Path</span></span>                      | <span data-ttu-id="15c67-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="15c67-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="15c67-132">1</span><span class="sxs-lookup"><span data-stu-id="15c67-132">1</span></span>     | <span data-ttu-id="15c67-133">/APP1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="15c67-134">ascii</span><span class="sxs-lookup"><span data-stu-id="15c67-134">ascii</span></span>       |
| <span data-ttu-id="15c67-135">2</span><span class="sxs-lookup"><span data-stu-id="15c67-135">2</span></span>     | <span data-ttu-id="15c67-136">/КСМП/ексиф: Гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="15c67-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="15c67-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="15c67-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="15c67-138">Remove Paths</span></span>



| <span data-ttu-id="15c67-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-139">Order</span></span> | <span data-ttu-id="15c67-140">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="15c67-141">1</span><span class="sxs-lookup"><span data-stu-id="15c67-141">1</span></span>     | <span data-ttu-id="15c67-142">/APP1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="15c67-143">2</span><span class="sxs-lookup"><span data-stu-id="15c67-143">2</span></span>     | <span data-ttu-id="15c67-144">/КСМП/ексиф: гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="15c67-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="15c67-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="15c67-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="15c67-146">Read Paths</span></span>



| <span data-ttu-id="15c67-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-147">Order</span></span> | <span data-ttu-id="15c67-148">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-148">Path</span></span>                      | <span data-ttu-id="15c67-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="15c67-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="15c67-150">1</span><span class="sxs-lookup"><span data-stu-id="15c67-150">1</span></span>     | <span data-ttu-id="15c67-151">/ИФД/ГПС/{ушорт = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="15c67-152">ascii</span><span class="sxs-lookup"><span data-stu-id="15c67-152">ascii</span></span>       |
| <span data-ttu-id="15c67-153">2</span><span class="sxs-lookup"><span data-stu-id="15c67-153">2</span></span>     | <span data-ttu-id="15c67-154">/ИФД/КСМП/ексиф: Гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="15c67-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="15c67-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="15c67-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="15c67-156">Write Paths</span></span>



| <span data-ttu-id="15c67-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-157">Order</span></span> | <span data-ttu-id="15c67-158">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-158">Path</span></span>                      | <span data-ttu-id="15c67-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="15c67-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="15c67-160">1</span><span class="sxs-lookup"><span data-stu-id="15c67-160">1</span></span>     | <span data-ttu-id="15c67-161">/ИФД/ГПС/{ушорт = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="15c67-162">ascii</span><span class="sxs-lookup"><span data-stu-id="15c67-162">ascii</span></span>       |
| <span data-ttu-id="15c67-163">2</span><span class="sxs-lookup"><span data-stu-id="15c67-163">2</span></span>     | <span data-ttu-id="15c67-164">/ИФД/КСМП/ексиф: Гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="15c67-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="15c67-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="15c67-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="15c67-166">Remove Paths</span></span>



| <span data-ttu-id="15c67-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="15c67-167">Order</span></span> | <span data-ttu-id="15c67-168">Путь</span><span class="sxs-lookup"><span data-stu-id="15c67-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="15c67-169">1</span><span class="sxs-lookup"><span data-stu-id="15c67-169">1</span></span>     | <span data-ttu-id="15c67-170">/ИФД/ГПС/{ушорт = 14}</span><span class="sxs-lookup"><span data-stu-id="15c67-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="15c67-171">2</span><span class="sxs-lookup"><span data-stu-id="15c67-171">2</span></span>     | <span data-ttu-id="15c67-172">/ИФД/КСМП/ексиф: гпстраккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="15c67-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15c67-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="15c67-174">См. также</span><span class="sxs-lookup"><span data-stu-id="15c67-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c67-175">System. GPS. Траккреф</span><span class="sxs-lookup"><span data-stu-id="15c67-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
