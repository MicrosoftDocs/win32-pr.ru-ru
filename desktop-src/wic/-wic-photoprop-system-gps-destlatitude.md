---
description: Политика метаданных фотографии для свойства System. GPS. Дестлатитуде.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Политика метаданных фотографии System. GPS. Дестлатитуде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684398"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="ef57b-103">Политика метаданных фотографии System. GPS. Дестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="ef57b-104">Политика метаданных фотографии для свойства [System. GPS. дестлатитуде](../properties/props-system-gps-destlatitude.md) .</span><span class="sxs-lookup"><span data-stu-id="ef57b-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ef57b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ef57b-105">PKEY</span></span>

<span data-ttu-id="ef57b-106">PKEY \_ GPS \_ дестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="ef57b-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="ef57b-107">Containers</span></span>

<span data-ttu-id="ef57b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ef57b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ef57b-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef57b-109">Read-Only</span></span>

<span data-ttu-id="ef57b-110">Да</span><span class="sxs-lookup"><span data-stu-id="ef57b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ef57b-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="ef57b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ef57b-112">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ef57b-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="ef57b-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="ef57b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="ef57b-114">VT \_ вектор \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ef57b-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ef57b-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="ef57b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ef57b-116">Это значение формируется из System. GPS. Дестлатитуденумератор и System. GPS. Дестлатитудеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="ef57b-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="ef57b-117">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="ef57b-117">It cannot be written directly.</span></span> <span data-ttu-id="ef57b-118">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="ef57b-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ef57b-119">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="ef57b-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ef57b-120">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ef57b-120">Read Paths</span></span>



| <span data-ttu-id="ef57b-121">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-121">Order</span></span> | <span data-ttu-id="ef57b-122">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-122">Path</span></span>                      | <span data-ttu-id="ef57b-123">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ef57b-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ef57b-124">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-124">1</span></span>     | <span data-ttu-id="ef57b-125">/APP1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="ef57b-126">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-126">2</span></span>     | <span data-ttu-id="ef57b-127">/КСМП/ексиф: Гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ef57b-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ef57b-128">Write Paths</span></span>



| <span data-ttu-id="ef57b-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-129">Order</span></span> | <span data-ttu-id="ef57b-130">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-130">Path</span></span>                      | <span data-ttu-id="ef57b-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ef57b-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ef57b-132">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-132">1</span></span>     | <span data-ttu-id="ef57b-133">/APP1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="ef57b-134">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-134">2</span></span>     | <span data-ttu-id="ef57b-135">/КСМП/ексиф: Гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ef57b-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ef57b-136">Remove Paths</span></span>



| <span data-ttu-id="ef57b-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-137">Order</span></span> | <span data-ttu-id="ef57b-138">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ef57b-139">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-139">1</span></span>     | <span data-ttu-id="ef57b-140">/APP1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="ef57b-141">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-141">2</span></span>     | <span data-ttu-id="ef57b-142">/КСМП/ексиф: гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ef57b-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="ef57b-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ef57b-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ef57b-144">Read Paths</span></span>



| <span data-ttu-id="ef57b-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-145">Order</span></span> | <span data-ttu-id="ef57b-146">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-146">Path</span></span>                          | <span data-ttu-id="ef57b-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ef57b-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ef57b-148">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-148">1</span></span>     | <span data-ttu-id="ef57b-149">/ИФД/ГПС/{ушорт = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="ef57b-150">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-150">2</span></span>     | <span data-ttu-id="ef57b-151">/ИФД/КСМП/ексиф: Гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ef57b-152">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ef57b-152">Write Paths</span></span>



| <span data-ttu-id="ef57b-153">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-153">Order</span></span> | <span data-ttu-id="ef57b-154">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-154">Path</span></span>                          | <span data-ttu-id="ef57b-155">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ef57b-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ef57b-156">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-156">1</span></span>     | <span data-ttu-id="ef57b-157">/ИФД/ГПС/{ушорт = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="ef57b-158">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-158">2</span></span>     | <span data-ttu-id="ef57b-159">/ИФД/КСМП/ексиф: Гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ef57b-160">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ef57b-160">Remove Paths</span></span>



| <span data-ttu-id="ef57b-161">Заказ</span><span class="sxs-lookup"><span data-stu-id="ef57b-161">Order</span></span> | <span data-ttu-id="ef57b-162">Путь</span><span class="sxs-lookup"><span data-stu-id="ef57b-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ef57b-163">1</span><span class="sxs-lookup"><span data-stu-id="ef57b-163">1</span></span>     | <span data-ttu-id="ef57b-164">/ИФД/ГПС/{ушорт = 20}</span><span class="sxs-lookup"><span data-stu-id="ef57b-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="ef57b-165">2</span><span class="sxs-lookup"><span data-stu-id="ef57b-165">2</span></span>     | <span data-ttu-id="ef57b-166">/ИФД/КСМП/ексиф: гпсдестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ef57b-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef57b-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef57b-168">См. также</span><span class="sxs-lookup"><span data-stu-id="ef57b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef57b-169">System. GPS. Дестлатитуде</span><span class="sxs-lookup"><span data-stu-id="ef57b-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
