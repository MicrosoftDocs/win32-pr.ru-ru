---
description: Политика метаданных фотографии для свойства System. GPS. DIFFERENTIAL.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Политика метаданных фотографии System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348575"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="0126f-103">Политика метаданных фотографии System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="0126f-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="0126f-104">Политика метаданных фотографии для свойства [System. GPS. Differential](../properties/props-system-gps-differential.md) .</span><span class="sxs-lookup"><span data-stu-id="0126f-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0126f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0126f-105">PKEY</span></span>

<span data-ttu-id="0126f-106">\_Разностная копия GPS "PKEY" \_</span><span class="sxs-lookup"><span data-stu-id="0126f-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="0126f-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="0126f-107">Containers</span></span>

<span data-ttu-id="0126f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0126f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0126f-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0126f-109">Read-Only</span></span>

<span data-ttu-id="0126f-110">Нет</span><span class="sxs-lookup"><span data-stu-id="0126f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0126f-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="0126f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0126f-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="0126f-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="0126f-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="0126f-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="0126f-114">\_Все они принимают VT UI1, VT \_ UI2 и VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="0126f-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0126f-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="0126f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0126f-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="0126f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0126f-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="0126f-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0126f-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0126f-118">Read Paths</span></span>



| <span data-ttu-id="0126f-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-119">Order</span></span> | <span data-ttu-id="0126f-120">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-120">Path</span></span>                      | <span data-ttu-id="0126f-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0126f-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0126f-122">1</span><span class="sxs-lookup"><span data-stu-id="0126f-122">1</span></span>     | <span data-ttu-id="0126f-123">/APP1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="0126f-124">ushort</span><span class="sxs-lookup"><span data-stu-id="0126f-124">ushort</span></span>      |
| <span data-ttu-id="0126f-125">2</span><span class="sxs-lookup"><span data-stu-id="0126f-125">2</span></span>     | <span data-ttu-id="0126f-126">/КСМП/ексиф: Гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="0126f-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="0126f-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0126f-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0126f-128">Write Paths</span></span>



| <span data-ttu-id="0126f-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-129">Order</span></span> | <span data-ttu-id="0126f-130">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-130">Path</span></span>                      | <span data-ttu-id="0126f-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0126f-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0126f-132">1</span><span class="sxs-lookup"><span data-stu-id="0126f-132">1</span></span>     | <span data-ttu-id="0126f-133">/APP1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="0126f-134">ushort</span><span class="sxs-lookup"><span data-stu-id="0126f-134">ushort</span></span>      |
| <span data-ttu-id="0126f-135">2</span><span class="sxs-lookup"><span data-stu-id="0126f-135">2</span></span>     | <span data-ttu-id="0126f-136">/КСМП/ексиф: Гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="0126f-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="0126f-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0126f-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0126f-138">Remove Paths</span></span>



| <span data-ttu-id="0126f-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-139">Order</span></span> | <span data-ttu-id="0126f-140">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="0126f-141">1</span><span class="sxs-lookup"><span data-stu-id="0126f-141">1</span></span>     | <span data-ttu-id="0126f-142">/APP1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="0126f-143">2</span><span class="sxs-lookup"><span data-stu-id="0126f-143">2</span></span>     | <span data-ttu-id="0126f-144">/КСМП/ексиф: гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0126f-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="0126f-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0126f-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0126f-146">Read Paths</span></span>



| <span data-ttu-id="0126f-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-147">Order</span></span> | <span data-ttu-id="0126f-148">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-148">Path</span></span>                          | <span data-ttu-id="0126f-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0126f-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0126f-150">1</span><span class="sxs-lookup"><span data-stu-id="0126f-150">1</span></span>     | <span data-ttu-id="0126f-151">/ИФД/ГПС/{ушорт = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="0126f-152">ushort</span><span class="sxs-lookup"><span data-stu-id="0126f-152">ushort</span></span>      |
| <span data-ttu-id="0126f-153">2</span><span class="sxs-lookup"><span data-stu-id="0126f-153">2</span></span>     | <span data-ttu-id="0126f-154">/ИФД/КСМП/ексиф: Гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="0126f-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="0126f-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0126f-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0126f-156">Write Paths</span></span>



| <span data-ttu-id="0126f-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-157">Order</span></span> | <span data-ttu-id="0126f-158">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-158">Path</span></span>                          | <span data-ttu-id="0126f-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0126f-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0126f-160">1</span><span class="sxs-lookup"><span data-stu-id="0126f-160">1</span></span>     | <span data-ttu-id="0126f-161">/ИФД/ГПС/{ушорт = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="0126f-162">ushort</span><span class="sxs-lookup"><span data-stu-id="0126f-162">ushort</span></span>      |
| <span data-ttu-id="0126f-163">2</span><span class="sxs-lookup"><span data-stu-id="0126f-163">2</span></span>     | <span data-ttu-id="0126f-164">/ИФД/КСМП/ексиф: Гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="0126f-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="0126f-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0126f-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0126f-166">Remove Paths</span></span>



| <span data-ttu-id="0126f-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="0126f-167">Order</span></span> | <span data-ttu-id="0126f-168">Путь</span><span class="sxs-lookup"><span data-stu-id="0126f-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0126f-169">1</span><span class="sxs-lookup"><span data-stu-id="0126f-169">1</span></span>     | <span data-ttu-id="0126f-170">/ИФД/ГПС/{ушорт = 30}</span><span class="sxs-lookup"><span data-stu-id="0126f-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="0126f-171">2</span><span class="sxs-lookup"><span data-stu-id="0126f-171">2</span></span>     | <span data-ttu-id="0126f-172">/ИФД/КСМП/ексиф: гпсдифферентиал</span><span class="sxs-lookup"><span data-stu-id="0126f-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0126f-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0126f-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0126f-174">См. также</span><span class="sxs-lookup"><span data-stu-id="0126f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0126f-175">System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="0126f-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
