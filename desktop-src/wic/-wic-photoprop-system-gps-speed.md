---
description: Политика метаданных фотографии для свойства System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Политика метаданных фотографии System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693399"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="33b64-103">Политика метаданных фотографии System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="33b64-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="33b64-104">Политика метаданных фотографии для свойства [System. GPS. Speed](../properties/props-system-gps-speed.md) .</span><span class="sxs-lookup"><span data-stu-id="33b64-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="33b64-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="33b64-105">PKEY</span></span>

<span data-ttu-id="33b64-106">" \_ Высокая скорость" для GPS \_</span><span class="sxs-lookup"><span data-stu-id="33b64-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="33b64-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="33b64-107">Containers</span></span>

<span data-ttu-id="33b64-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="33b64-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="33b64-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="33b64-109">Read-Only</span></span>

<span data-ttu-id="33b64-110">Да</span><span class="sxs-lookup"><span data-stu-id="33b64-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="33b64-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="33b64-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="33b64-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="33b64-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="33b64-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="33b64-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="33b64-114">Это значение формируется из System. GPS. Спиднумератор и System. GPS. Спидденоминатор.</span><span class="sxs-lookup"><span data-stu-id="33b64-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="33b64-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="33b64-115">It cannot be written directly.</span></span> <span data-ttu-id="33b64-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="33b64-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="33b64-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="33b64-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="33b64-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="33b64-118">Read Paths</span></span>



| <span data-ttu-id="33b64-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-119">Order</span></span> | <span data-ttu-id="33b64-120">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-120">Path</span></span>                      | <span data-ttu-id="33b64-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="33b64-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="33b64-122">1</span><span class="sxs-lookup"><span data-stu-id="33b64-122">1</span></span>     | <span data-ttu-id="33b64-123">/APP1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="33b64-124">2</span><span class="sxs-lookup"><span data-stu-id="33b64-124">2</span></span>     | <span data-ttu-id="33b64-125">/КСМП/ексиф: Гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="33b64-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="33b64-126">Write Paths</span></span>



| <span data-ttu-id="33b64-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-127">Order</span></span> | <span data-ttu-id="33b64-128">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-128">Path</span></span>                      | <span data-ttu-id="33b64-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="33b64-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="33b64-130">1</span><span class="sxs-lookup"><span data-stu-id="33b64-130">1</span></span>     | <span data-ttu-id="33b64-131">/APP1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="33b64-132">2</span><span class="sxs-lookup"><span data-stu-id="33b64-132">2</span></span>     | <span data-ttu-id="33b64-133">/КСМП/ексиф: Гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="33b64-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="33b64-134">Remove Paths</span></span>



| <span data-ttu-id="33b64-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-135">Order</span></span> | <span data-ttu-id="33b64-136">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="33b64-137">1</span><span class="sxs-lookup"><span data-stu-id="33b64-137">1</span></span>     | <span data-ttu-id="33b64-138">/APP1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="33b64-139">2</span><span class="sxs-lookup"><span data-stu-id="33b64-139">2</span></span>     | <span data-ttu-id="33b64-140">/КСМП/ексиф: гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="33b64-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="33b64-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="33b64-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="33b64-142">Read Paths</span></span>



| <span data-ttu-id="33b64-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-143">Order</span></span> | <span data-ttu-id="33b64-144">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-144">Path</span></span>                   | <span data-ttu-id="33b64-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="33b64-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="33b64-146">1</span><span class="sxs-lookup"><span data-stu-id="33b64-146">1</span></span>     | <span data-ttu-id="33b64-147">/ИФД/ГПС/{ушорт = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="33b64-148">2</span><span class="sxs-lookup"><span data-stu-id="33b64-148">2</span></span>     | <span data-ttu-id="33b64-149">/ИФД/КСМП/ексиф: Гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="33b64-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="33b64-150">Write Paths</span></span>



| <span data-ttu-id="33b64-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-151">Order</span></span> | <span data-ttu-id="33b64-152">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-152">Path</span></span>                   | <span data-ttu-id="33b64-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="33b64-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="33b64-154">1</span><span class="sxs-lookup"><span data-stu-id="33b64-154">1</span></span>     | <span data-ttu-id="33b64-155">/ИФД/ГПС/{ушорт = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="33b64-156">2</span><span class="sxs-lookup"><span data-stu-id="33b64-156">2</span></span>     | <span data-ttu-id="33b64-157">/ИФД/КСМП/ексиф: Гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="33b64-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="33b64-158">Remove Paths</span></span>



| <span data-ttu-id="33b64-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="33b64-159">Order</span></span> | <span data-ttu-id="33b64-160">Путь</span><span class="sxs-lookup"><span data-stu-id="33b64-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="33b64-161">1</span><span class="sxs-lookup"><span data-stu-id="33b64-161">1</span></span>     | <span data-ttu-id="33b64-162">/ИФД/ГПС/{ушорт = 13}</span><span class="sxs-lookup"><span data-stu-id="33b64-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="33b64-163">2</span><span class="sxs-lookup"><span data-stu-id="33b64-163">2</span></span>     | <span data-ttu-id="33b64-164">/ИФД/КСМП/ексиф: гпсспид</span><span class="sxs-lookup"><span data-stu-id="33b64-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="33b64-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33b64-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="33b64-166">См. также</span><span class="sxs-lookup"><span data-stu-id="33b64-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33b64-167">System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="33b64-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
