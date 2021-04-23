---
description: Политика метаданных фотографии для свойства System. GPS. Дестлонгитуде.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Политика метаданных фотографии System. GPS. Дестлонгитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081310"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="3eb78-103">Политика метаданных фотографии System. GPS. Дестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="3eb78-104">Политика метаданных фотографии для свойства [System. GPS. дестлонгитуде](../properties/props-system-gps-destlongitude.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb78-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3eb78-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3eb78-105">PKEY</span></span>

<span data-ttu-id="3eb78-106">PKEY \_ GPS \_ дестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="3eb78-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="3eb78-107">Containers</span></span>

<span data-ttu-id="3eb78-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3eb78-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3eb78-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3eb78-109">Read-Only</span></span>

<span data-ttu-id="3eb78-110">Да</span><span class="sxs-lookup"><span data-stu-id="3eb78-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3eb78-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="3eb78-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3eb78-112">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="3eb78-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="3eb78-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="3eb78-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="3eb78-114">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="3eb78-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3eb78-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="3eb78-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3eb78-116">Это значение формируется из System. GPS. Дестлонгитуденумератор и System. GPS. Дестлонгитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="3eb78-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="3eb78-117">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="3eb78-117">It cannot be written directly.</span></span> <span data-ttu-id="3eb78-118">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="3eb78-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3eb78-119">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="3eb78-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3eb78-120">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="3eb78-120">Read Paths</span></span>



| <span data-ttu-id="3eb78-121">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-121">Order</span></span> | <span data-ttu-id="3eb78-122">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-122">Path</span></span>                       | <span data-ttu-id="3eb78-123">Формат диска</span><span class="sxs-lookup"><span data-stu-id="3eb78-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3eb78-124">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-124">1</span></span>     | <span data-ttu-id="3eb78-125">/APP1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="3eb78-126">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-126">2</span></span>     | <span data-ttu-id="3eb78-127">/КСМП/ексиф: Гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3eb78-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="3eb78-128">Write Paths</span></span>



| <span data-ttu-id="3eb78-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-129">Order</span></span> | <span data-ttu-id="3eb78-130">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-130">Path</span></span>                       | <span data-ttu-id="3eb78-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="3eb78-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3eb78-132">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-132">1</span></span>     | <span data-ttu-id="3eb78-133">/APP1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="3eb78-134">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-134">2</span></span>     | <span data-ttu-id="3eb78-135">/КСМП/ексиф: Гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3eb78-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="3eb78-136">Remove Paths</span></span>



| <span data-ttu-id="3eb78-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-137">Order</span></span> | <span data-ttu-id="3eb78-138">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="3eb78-139">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-139">1</span></span>     | <span data-ttu-id="3eb78-140">/APP1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="3eb78-141">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-141">2</span></span>     | <span data-ttu-id="3eb78-142">/КСМП/ексиф: гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="3eb78-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="3eb78-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3eb78-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="3eb78-144">Read Paths</span></span>



| <span data-ttu-id="3eb78-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-145">Order</span></span> | <span data-ttu-id="3eb78-146">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-146">Path</span></span>                           | <span data-ttu-id="3eb78-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="3eb78-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="3eb78-148">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-148">1</span></span>     | <span data-ttu-id="3eb78-149">/ИФД/ГПС/{ушорт = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="3eb78-150">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-150">2</span></span>     | <span data-ttu-id="3eb78-151">/ИФД/КСМП/ексиф: Гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="3eb78-152">Пути записи</span><span class="sxs-lookup"><span data-stu-id="3eb78-152">Write Paths</span></span>



| <span data-ttu-id="3eb78-153">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-153">Order</span></span> | <span data-ttu-id="3eb78-154">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-154">Path</span></span>                           | <span data-ttu-id="3eb78-155">Формат диска</span><span class="sxs-lookup"><span data-stu-id="3eb78-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="3eb78-156">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-156">1</span></span>     | <span data-ttu-id="3eb78-157">/ИФД/ГПС/{ушорт = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="3eb78-158">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-158">2</span></span>     | <span data-ttu-id="3eb78-159">/ИФД/КСМП/ексиф: Гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="3eb78-160">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="3eb78-160">Remove Paths</span></span>



| <span data-ttu-id="3eb78-161">Заказ</span><span class="sxs-lookup"><span data-stu-id="3eb78-161">Order</span></span> | <span data-ttu-id="3eb78-162">Путь</span><span class="sxs-lookup"><span data-stu-id="3eb78-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="3eb78-163">1</span><span class="sxs-lookup"><span data-stu-id="3eb78-163">1</span></span>     | <span data-ttu-id="3eb78-164">/ИФД/ГПС/{ушорт = 22}</span><span class="sxs-lookup"><span data-stu-id="3eb78-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="3eb78-165">2</span><span class="sxs-lookup"><span data-stu-id="3eb78-165">2</span></span>     | <span data-ttu-id="3eb78-166">/ИФД/КСМП/ексиф: гпсдестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3eb78-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3eb78-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3eb78-168">См. также</span><span class="sxs-lookup"><span data-stu-id="3eb78-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eb78-169">System. GPS. Дестлонгитуде</span><span class="sxs-lookup"><span data-stu-id="3eb78-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
