---
description: Политика метаданных фотографии для свойства System. GPS. Имгдиректион.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Политика метаданных фотографии System. GPS. Имгдиректион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712795"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="62560-103">Политика метаданных фотографии System. GPS. Имгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="62560-104">Политика метаданных фотографии для свойства [System. GPS. имгдиректион](../properties/props-system-gps-imgdirection.md) .</span><span class="sxs-lookup"><span data-stu-id="62560-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="62560-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="62560-105">PKEY</span></span>

<span data-ttu-id="62560-106">PKEY \_ GPS \_ имгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="62560-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="62560-107">Containers</span></span>

<span data-ttu-id="62560-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="62560-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="62560-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="62560-109">Read-Only</span></span>

<span data-ttu-id="62560-110">Да</span><span class="sxs-lookup"><span data-stu-id="62560-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="62560-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="62560-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="62560-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="62560-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="62560-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="62560-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="62560-114">Это значение можно записать с помощью записи в System. GPS. Имгдиректионнумератор и System. GPS. Имгдиректионденоминатор.</span><span class="sxs-lookup"><span data-stu-id="62560-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="62560-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="62560-115">It cannot be written directly.</span></span> <span data-ttu-id="62560-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="62560-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="62560-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="62560-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="62560-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="62560-118">Read Paths</span></span>



| <span data-ttu-id="62560-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-119">Order</span></span> | <span data-ttu-id="62560-120">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-120">Path</span></span>                      | <span data-ttu-id="62560-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62560-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="62560-122">1</span><span class="sxs-lookup"><span data-stu-id="62560-122">1</span></span>     | <span data-ttu-id="62560-123">/APP1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="62560-124">2</span><span class="sxs-lookup"><span data-stu-id="62560-124">2</span></span>     | <span data-ttu-id="62560-125">/КСМП/ексиф: Гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="62560-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="62560-126">Write Paths</span></span>



| <span data-ttu-id="62560-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-127">Order</span></span> | <span data-ttu-id="62560-128">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-128">Path</span></span>                      | <span data-ttu-id="62560-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62560-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="62560-130">1</span><span class="sxs-lookup"><span data-stu-id="62560-130">1</span></span>     | <span data-ttu-id="62560-131">/APP1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="62560-132">2</span><span class="sxs-lookup"><span data-stu-id="62560-132">2</span></span>     | <span data-ttu-id="62560-133">/КСМП/ексиф: Гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62560-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="62560-134">Remove Paths</span></span>



| <span data-ttu-id="62560-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-135">Order</span></span> | <span data-ttu-id="62560-136">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="62560-137">1</span><span class="sxs-lookup"><span data-stu-id="62560-137">1</span></span>     | <span data-ttu-id="62560-138">/APP1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="62560-139">2</span><span class="sxs-lookup"><span data-stu-id="62560-139">2</span></span>     | <span data-ttu-id="62560-140">/КСМП/ексиф: гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="62560-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="62560-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="62560-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="62560-142">Read Paths</span></span>



| <span data-ttu-id="62560-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-143">Order</span></span> | <span data-ttu-id="62560-144">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-144">Path</span></span>                          | <span data-ttu-id="62560-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62560-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="62560-146">1</span><span class="sxs-lookup"><span data-stu-id="62560-146">1</span></span>     | <span data-ttu-id="62560-147">/ИФД/ГПС/{ушорт = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="62560-148">2</span><span class="sxs-lookup"><span data-stu-id="62560-148">2</span></span>     | <span data-ttu-id="62560-149">/ИФД/КСМП/ексиф: Гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="62560-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="62560-150">Write Paths</span></span>



| <span data-ttu-id="62560-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-151">Order</span></span> | <span data-ttu-id="62560-152">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-152">Path</span></span>                          | <span data-ttu-id="62560-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="62560-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="62560-154">1</span><span class="sxs-lookup"><span data-stu-id="62560-154">1</span></span>     | <span data-ttu-id="62560-155">/ИФД/ГПС/{ушорт = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="62560-156">2</span><span class="sxs-lookup"><span data-stu-id="62560-156">2</span></span>     | <span data-ttu-id="62560-157">/ИФД/КСМП/ексиф: Гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="62560-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="62560-158">Remove Paths</span></span>



| <span data-ttu-id="62560-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="62560-159">Order</span></span> | <span data-ttu-id="62560-160">Путь</span><span class="sxs-lookup"><span data-stu-id="62560-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="62560-161">1</span><span class="sxs-lookup"><span data-stu-id="62560-161">1</span></span>     | <span data-ttu-id="62560-162">/ИФД/ГПС/{ушорт = 17}</span><span class="sxs-lookup"><span data-stu-id="62560-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="62560-163">2</span><span class="sxs-lookup"><span data-stu-id="62560-163">2</span></span>     | <span data-ttu-id="62560-164">/ИФД/КСМП/ексиф: гпсимгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="62560-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62560-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="62560-166">См. также</span><span class="sxs-lookup"><span data-stu-id="62560-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62560-167">System. GPS. Имгдиректион</span><span class="sxs-lookup"><span data-stu-id="62560-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
