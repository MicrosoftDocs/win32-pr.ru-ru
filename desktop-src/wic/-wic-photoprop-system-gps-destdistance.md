---
description: Политика метаданных фотографии для свойства System. GPS. Дестдистанце.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Политика метаданных фотографии System. GPS. Дестдистанце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683780"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="11079-103">Политика метаданных фотографии System. GPS. Дестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="11079-104">Политика метаданных фотографии для свойства [System. GPS. дестдистанце](../properties/props-system-gps-destdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="11079-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="11079-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="11079-105">PKEY</span></span>

<span data-ttu-id="11079-106">PKEY \_ GPS \_ дестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="11079-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="11079-107">Containers</span></span>

<span data-ttu-id="11079-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="11079-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="11079-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="11079-109">Read-Only</span></span>

<span data-ttu-id="11079-110">Да</span><span class="sxs-lookup"><span data-stu-id="11079-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="11079-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="11079-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="11079-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="11079-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="11079-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="11079-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="11079-114">Это значение формируется из System. GPS. Дестдистанценумератор и System. GPS. Дестдистанцеденоминатор.</span><span class="sxs-lookup"><span data-stu-id="11079-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="11079-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="11079-115">It cannot be written directly.</span></span> <span data-ttu-id="11079-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="11079-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="11079-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="11079-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="11079-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="11079-118">Read Paths</span></span>



| <span data-ttu-id="11079-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-119">Order</span></span> | <span data-ttu-id="11079-120">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-120">Path</span></span>                      | <span data-ttu-id="11079-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="11079-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="11079-122">1</span><span class="sxs-lookup"><span data-stu-id="11079-122">1</span></span>     | <span data-ttu-id="11079-123">/APP1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="11079-124">2</span><span class="sxs-lookup"><span data-stu-id="11079-124">2</span></span>     | <span data-ttu-id="11079-125">/КСМП/ексиф: Гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="11079-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="11079-126">Write Paths</span></span>



| <span data-ttu-id="11079-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-127">Order</span></span> | <span data-ttu-id="11079-128">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-128">Path</span></span>                      | <span data-ttu-id="11079-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="11079-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="11079-130">1</span><span class="sxs-lookup"><span data-stu-id="11079-130">1</span></span>     | <span data-ttu-id="11079-131">/APP1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="11079-132">2</span><span class="sxs-lookup"><span data-stu-id="11079-132">2</span></span>     | <span data-ttu-id="11079-133">/КСМП/ексиф: Гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="11079-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="11079-134">Remove Paths</span></span>



| <span data-ttu-id="11079-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-135">Order</span></span> | <span data-ttu-id="11079-136">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="11079-137">1</span><span class="sxs-lookup"><span data-stu-id="11079-137">1</span></span>     | <span data-ttu-id="11079-138">/APP1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="11079-139">2</span><span class="sxs-lookup"><span data-stu-id="11079-139">2</span></span>     | <span data-ttu-id="11079-140">/КСМП/ексиф: гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="11079-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="11079-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="11079-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="11079-142">Read Paths</span></span>



| <span data-ttu-id="11079-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-143">Order</span></span> | <span data-ttu-id="11079-144">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-144">Path</span></span>                          | <span data-ttu-id="11079-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="11079-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="11079-146">1</span><span class="sxs-lookup"><span data-stu-id="11079-146">1</span></span>     | <span data-ttu-id="11079-147">/ИФД/ГПС/{ушорт = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="11079-148">2</span><span class="sxs-lookup"><span data-stu-id="11079-148">2</span></span>     | <span data-ttu-id="11079-149">/ИФД/КСМП/ексиф: Гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="11079-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="11079-150">Write Paths</span></span>



| <span data-ttu-id="11079-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-151">Order</span></span> | <span data-ttu-id="11079-152">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-152">Path</span></span>                          | <span data-ttu-id="11079-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="11079-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="11079-154">1</span><span class="sxs-lookup"><span data-stu-id="11079-154">1</span></span>     | <span data-ttu-id="11079-155">/ИФД/ГПС/{ушорт = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="11079-156">2</span><span class="sxs-lookup"><span data-stu-id="11079-156">2</span></span>     | <span data-ttu-id="11079-157">/ИФД/КСМП/ексиф: Гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="11079-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="11079-158">Remove Paths</span></span>



| <span data-ttu-id="11079-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="11079-159">Order</span></span> | <span data-ttu-id="11079-160">Путь</span><span class="sxs-lookup"><span data-stu-id="11079-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="11079-161">1</span><span class="sxs-lookup"><span data-stu-id="11079-161">1</span></span>     | <span data-ttu-id="11079-162">/ИФД/ГПС/{ушорт = 26}</span><span class="sxs-lookup"><span data-stu-id="11079-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="11079-163">2</span><span class="sxs-lookup"><span data-stu-id="11079-163">2</span></span>     | <span data-ttu-id="11079-164">/ИФД/КСМП/ексиф: гпсдестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11079-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11079-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="11079-166">См. также</span><span class="sxs-lookup"><span data-stu-id="11079-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11079-167">System. GPS. Дестдистанце</span><span class="sxs-lookup"><span data-stu-id="11079-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
