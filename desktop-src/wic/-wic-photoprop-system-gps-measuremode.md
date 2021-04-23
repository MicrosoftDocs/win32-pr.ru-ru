---
description: Политика метаданных фотографии для свойства System. GPS. Меасуремоде.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Политика метаданных фотографии System. GPS. Меасуремоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998643"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="9a7bf-103">Политика метаданных фотографии System. GPS. Меасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="9a7bf-104">Политика метаданных фотографии для свойства [System. GPS. меасуремоде](../properties/props-system-gps-measuremode.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7bf-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9a7bf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9a7bf-105">PKEY</span></span>

<span data-ttu-id="9a7bf-106">PKEY \_ GPS \_ меасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="9a7bf-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="9a7bf-107">Containers</span></span>

<span data-ttu-id="9a7bf-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9a7bf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9a7bf-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a7bf-109">Read-Only</span></span>

<span data-ttu-id="9a7bf-110">Нет</span><span class="sxs-lookup"><span data-stu-id="9a7bf-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9a7bf-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9a7bf-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9a7bf-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9a7bf-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9a7bf-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9a7bf-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="9a7bf-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9a7bf-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="9a7bf-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="9a7bf-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a7bf-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9a7bf-118">Read Paths</span></span>



| <span data-ttu-id="9a7bf-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-119">Order</span></span> | <span data-ttu-id="9a7bf-120">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-120">Path</span></span>                      | <span data-ttu-id="9a7bf-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a7bf-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a7bf-122">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-122">1</span></span>     | <span data-ttu-id="9a7bf-123">/APP1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="9a7bf-124">ascii</span><span class="sxs-lookup"><span data-stu-id="9a7bf-124">ascii</span></span>       |
| <span data-ttu-id="9a7bf-125">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-125">2</span></span>     | <span data-ttu-id="9a7bf-126">/КСМП/ексиф: Гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="9a7bf-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="9a7bf-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9a7bf-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9a7bf-128">Write Paths</span></span>



| <span data-ttu-id="9a7bf-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-129">Order</span></span> | <span data-ttu-id="9a7bf-130">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-130">Path</span></span>                      | <span data-ttu-id="9a7bf-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a7bf-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9a7bf-132">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-132">1</span></span>     | <span data-ttu-id="9a7bf-133">/APP1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="9a7bf-134">ascii</span><span class="sxs-lookup"><span data-stu-id="9a7bf-134">ascii</span></span>       |
| <span data-ttu-id="9a7bf-135">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-135">2</span></span>     | <span data-ttu-id="9a7bf-136">/КСМП/ексиф: Гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="9a7bf-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="9a7bf-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9a7bf-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9a7bf-138">Remove Paths</span></span>



| <span data-ttu-id="9a7bf-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-139">Order</span></span> | <span data-ttu-id="9a7bf-140">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9a7bf-141">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-141">1</span></span>     | <span data-ttu-id="9a7bf-142">/APP1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="9a7bf-143">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-143">2</span></span>     | <span data-ttu-id="9a7bf-144">/КСМП/ексиф: гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="9a7bf-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="9a7bf-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9a7bf-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="9a7bf-146">Read Paths</span></span>



| <span data-ttu-id="9a7bf-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-147">Order</span></span> | <span data-ttu-id="9a7bf-148">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-148">Path</span></span>                         | <span data-ttu-id="9a7bf-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a7bf-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="9a7bf-150">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-150">1</span></span>     | <span data-ttu-id="9a7bf-151">/ИФД/ГПС/{ушорт = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="9a7bf-152">ascii</span><span class="sxs-lookup"><span data-stu-id="9a7bf-152">ascii</span></span>       |
| <span data-ttu-id="9a7bf-153">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-153">2</span></span>     | <span data-ttu-id="9a7bf-154">/ИФД/КСМП/ексиф: Гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="9a7bf-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="9a7bf-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9a7bf-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="9a7bf-156">Write Paths</span></span>



| <span data-ttu-id="9a7bf-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-157">Order</span></span> | <span data-ttu-id="9a7bf-158">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-158">Path</span></span>                         | <span data-ttu-id="9a7bf-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="9a7bf-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="9a7bf-160">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-160">1</span></span>     | <span data-ttu-id="9a7bf-161">/ИФД/ГПС/{ушорт = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="9a7bf-162">ascii</span><span class="sxs-lookup"><span data-stu-id="9a7bf-162">ascii</span></span>       |
| <span data-ttu-id="9a7bf-163">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-163">2</span></span>     | <span data-ttu-id="9a7bf-164">/ИФД/КСМП/ексиф: Гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="9a7bf-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="9a7bf-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9a7bf-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="9a7bf-166">Remove Paths</span></span>



| <span data-ttu-id="9a7bf-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="9a7bf-167">Order</span></span> | <span data-ttu-id="9a7bf-168">Путь</span><span class="sxs-lookup"><span data-stu-id="9a7bf-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="9a7bf-169">1</span><span class="sxs-lookup"><span data-stu-id="9a7bf-169">1</span></span>     | <span data-ttu-id="9a7bf-170">/ИФД/ГПС/{ушорт = 10}</span><span class="sxs-lookup"><span data-stu-id="9a7bf-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="9a7bf-171">2</span><span class="sxs-lookup"><span data-stu-id="9a7bf-171">2</span></span>     | <span data-ttu-id="9a7bf-172">/ИФД/КСМП/ексиф: гпсмеасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a7bf-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a7bf-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a7bf-174">См. также</span><span class="sxs-lookup"><span data-stu-id="9a7bf-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a7bf-175">System. GPS. Меасуремоде</span><span class="sxs-lookup"><span data-stu-id="9a7bf-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
