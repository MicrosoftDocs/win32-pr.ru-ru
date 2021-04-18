---
description: Политика метаданных фотографии для свойства System. GPS. Спидреф.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Политика метаданных фотографии System. GPS. Спидреф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693398"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="f3c3a-103">Политика метаданных фотографии System. GPS. Спидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="f3c3a-104">Политика метаданных фотографии для свойства [System. GPS. спидреф](../properties/props-system-gps-speedref.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c3a-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f3c3a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f3c3a-105">PKEY</span></span>

<span data-ttu-id="f3c3a-106">PKEY \_ GPS \_ спидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="f3c3a-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="f3c3a-107">Containers</span></span>

<span data-ttu-id="f3c3a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3c3a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f3c3a-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3c3a-109">Read-Only</span></span>

<span data-ttu-id="f3c3a-110">Нет</span><span class="sxs-lookup"><span data-stu-id="f3c3a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f3c3a-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f3c3a-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f3c3a-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="f3c3a-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="f3c3a-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="f3c3a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f3c3a-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="f3c3a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f3c3a-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="f3c3a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="f3c3a-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="f3c3a-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f3c3a-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="f3c3a-118">Read Paths</span></span>



| <span data-ttu-id="f3c3a-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-119">Order</span></span> | <span data-ttu-id="f3c3a-120">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-120">Path</span></span>                      | <span data-ttu-id="f3c3a-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f3c3a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f3c3a-122">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-122">1</span></span>     | <span data-ttu-id="f3c3a-123">/APP1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="f3c3a-124">ascii</span><span class="sxs-lookup"><span data-stu-id="f3c3a-124">ascii</span></span>       |
| <span data-ttu-id="f3c3a-125">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-125">2</span></span>     | <span data-ttu-id="f3c3a-126">/КСМП/ексиф: Гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="f3c3a-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="f3c3a-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f3c3a-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="f3c3a-128">Write Paths</span></span>



| <span data-ttu-id="f3c3a-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-129">Order</span></span> | <span data-ttu-id="f3c3a-130">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-130">Path</span></span>                      | <span data-ttu-id="f3c3a-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f3c3a-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f3c3a-132">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-132">1</span></span>     | <span data-ttu-id="f3c3a-133">/APP1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="f3c3a-134">ascii</span><span class="sxs-lookup"><span data-stu-id="f3c3a-134">ascii</span></span>       |
| <span data-ttu-id="f3c3a-135">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-135">2</span></span>     | <span data-ttu-id="f3c3a-136">/КСМП/ексиф: Гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="f3c3a-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="f3c3a-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f3c3a-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="f3c3a-138">Remove Paths</span></span>



| <span data-ttu-id="f3c3a-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-139">Order</span></span> | <span data-ttu-id="f3c3a-140">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-140">Path</span></span>                      | <span data-ttu-id="f3c3a-141">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f3c3a-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f3c3a-142">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-142">1</span></span>     | <span data-ttu-id="f3c3a-143">/APP1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="f3c3a-144">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-144">2</span></span>     | <span data-ttu-id="f3c3a-145">/КСМП/ексиф: гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="f3c3a-146">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="f3c3a-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f3c3a-147">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="f3c3a-147">Read Paths</span></span>



| <span data-ttu-id="f3c3a-148">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-148">Order</span></span> | <span data-ttu-id="f3c3a-149">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="f3c3a-150">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-150">1</span></span>     | <span data-ttu-id="f3c3a-151">/ИФД/ГПС/{ушорт = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="f3c3a-152">ascii</span><span class="sxs-lookup"><span data-stu-id="f3c3a-152">ascii</span></span>   |
| <span data-ttu-id="f3c3a-153">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-153">2</span></span>     | <span data-ttu-id="f3c3a-154">/ИФД/КСМП/ексиф: Гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="f3c3a-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="f3c3a-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="f3c3a-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="f3c3a-156">Write Paths</span></span>



| <span data-ttu-id="f3c3a-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-157">Order</span></span> | <span data-ttu-id="f3c3a-158">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-158">Path</span></span>                      | <span data-ttu-id="f3c3a-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="f3c3a-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f3c3a-160">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-160">1</span></span>     | <span data-ttu-id="f3c3a-161">/ИФД/ГПС/{ушорт = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="f3c3a-162">ascii</span><span class="sxs-lookup"><span data-stu-id="f3c3a-162">ascii</span></span>       |
| <span data-ttu-id="f3c3a-163">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-163">2</span></span>     | <span data-ttu-id="f3c3a-164">/ИФД/КСМП/ексиф: Гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="f3c3a-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="f3c3a-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f3c3a-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="f3c3a-166">Remove Paths</span></span>



| <span data-ttu-id="f3c3a-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="f3c3a-167">Order</span></span> | <span data-ttu-id="f3c3a-168">Путь</span><span class="sxs-lookup"><span data-stu-id="f3c3a-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f3c3a-169">1</span><span class="sxs-lookup"><span data-stu-id="f3c3a-169">1</span></span>     | <span data-ttu-id="f3c3a-170">/ИФД/ГПС/{ушорт = 12}</span><span class="sxs-lookup"><span data-stu-id="f3c3a-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="f3c3a-171">2</span><span class="sxs-lookup"><span data-stu-id="f3c3a-171">2</span></span>     | <span data-ttu-id="f3c3a-172">/ИФД/КСМП/ексиф: гпсспидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f3c3a-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3c3a-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3c3a-174">См. также</span><span class="sxs-lookup"><span data-stu-id="f3c3a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c3a-175">System. GPS. Спидреф</span><span class="sxs-lookup"><span data-stu-id="f3c3a-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
