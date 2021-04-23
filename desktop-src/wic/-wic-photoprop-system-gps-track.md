---
description: Политика метаданных фотографии для свойства System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Политика метаданных фотографии System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703268"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="971bf-103">Политика метаданных фотографии System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="971bf-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="971bf-104">Политика метаданных фотографии для свойства [System. GPS. Track](../properties/props-system-gps-track.md) .</span><span class="sxs-lookup"><span data-stu-id="971bf-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="971bf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="971bf-105">PKEY</span></span>

<span data-ttu-id="971bf-106">Подпрограмма \_ записи GPS "PKEY" \_</span><span class="sxs-lookup"><span data-stu-id="971bf-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="971bf-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="971bf-107">Containers</span></span>

<span data-ttu-id="971bf-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="971bf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="971bf-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="971bf-109">Read-Only</span></span>

<span data-ttu-id="971bf-110">Да</span><span class="sxs-lookup"><span data-stu-id="971bf-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="971bf-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="971bf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="971bf-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="971bf-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="971bf-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="971bf-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="971bf-114">Это значение формируется из System. GPS. Траккнумератор и System. GPS. Траккденоминатор.</span><span class="sxs-lookup"><span data-stu-id="971bf-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="971bf-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="971bf-115">It cannot be written directly.</span></span> <span data-ttu-id="971bf-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="971bf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="971bf-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="971bf-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="971bf-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="971bf-118">Read Paths</span></span>



| <span data-ttu-id="971bf-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-119">Order</span></span> | <span data-ttu-id="971bf-120">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-120">Path</span></span>                      | <span data-ttu-id="971bf-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="971bf-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="971bf-122">1</span><span class="sxs-lookup"><span data-stu-id="971bf-122">1</span></span>     | <span data-ttu-id="971bf-123">/APP1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="971bf-124">2</span><span class="sxs-lookup"><span data-stu-id="971bf-124">2</span></span>     | <span data-ttu-id="971bf-125">/КСМП/ексиф: Гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="971bf-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="971bf-126">Write Paths</span></span>



| <span data-ttu-id="971bf-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-127">Order</span></span> | <span data-ttu-id="971bf-128">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-128">Path</span></span>                      | <span data-ttu-id="971bf-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="971bf-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="971bf-130">1</span><span class="sxs-lookup"><span data-stu-id="971bf-130">1</span></span>     | <span data-ttu-id="971bf-131">/APP1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="971bf-132">2</span><span class="sxs-lookup"><span data-stu-id="971bf-132">2</span></span>     | <span data-ttu-id="971bf-133">/КСМП/ексиф: Гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="971bf-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="971bf-134">Remove Paths</span></span>



| <span data-ttu-id="971bf-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-135">Order</span></span> | <span data-ttu-id="971bf-136">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="971bf-137">1</span><span class="sxs-lookup"><span data-stu-id="971bf-137">1</span></span>     | <span data-ttu-id="971bf-138">/APP1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="971bf-139">2</span><span class="sxs-lookup"><span data-stu-id="971bf-139">2</span></span>     | <span data-ttu-id="971bf-140">/КСМП/ексиф: гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="971bf-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="971bf-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="971bf-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="971bf-142">Read Paths</span></span>



| <span data-ttu-id="971bf-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-143">Order</span></span> | <span data-ttu-id="971bf-144">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-144">Path</span></span>                   | <span data-ttu-id="971bf-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="971bf-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="971bf-146">1</span><span class="sxs-lookup"><span data-stu-id="971bf-146">1</span></span>     | <span data-ttu-id="971bf-147">/ИФД/ГПС/{ушорт = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="971bf-148">2</span><span class="sxs-lookup"><span data-stu-id="971bf-148">2</span></span>     | <span data-ttu-id="971bf-149">/ИФД/КСМП/ексиф: Гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="971bf-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="971bf-150">Write Paths</span></span>



| <span data-ttu-id="971bf-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-151">Order</span></span> | <span data-ttu-id="971bf-152">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-152">Path</span></span>                   | <span data-ttu-id="971bf-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="971bf-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="971bf-154">1</span><span class="sxs-lookup"><span data-stu-id="971bf-154">1</span></span>     | <span data-ttu-id="971bf-155">/ИФД/ГПС/{ушорт = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="971bf-156">2</span><span class="sxs-lookup"><span data-stu-id="971bf-156">2</span></span>     | <span data-ttu-id="971bf-157">/ИФД/КСМП/ексиф: Гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="971bf-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="971bf-158">Remove Paths</span></span>



| <span data-ttu-id="971bf-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="971bf-159">Order</span></span> | <span data-ttu-id="971bf-160">Путь</span><span class="sxs-lookup"><span data-stu-id="971bf-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="971bf-161">1</span><span class="sxs-lookup"><span data-stu-id="971bf-161">1</span></span>     | <span data-ttu-id="971bf-162">/ИФД/ГПС/{ушорт = 15}</span><span class="sxs-lookup"><span data-stu-id="971bf-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="971bf-163">2</span><span class="sxs-lookup"><span data-stu-id="971bf-163">2</span></span>     | <span data-ttu-id="971bf-164">/ИФД/КСМП/ексиф: гпстракк</span><span class="sxs-lookup"><span data-stu-id="971bf-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="971bf-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="971bf-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="971bf-166">См. также</span><span class="sxs-lookup"><span data-stu-id="971bf-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="971bf-167">System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="971bf-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
