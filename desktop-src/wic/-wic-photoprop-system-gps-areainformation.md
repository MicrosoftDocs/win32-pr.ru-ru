---
description: Политика метаданных фотографии для свойства System. GPS. Ареаинформатион.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Политика метаданных фотографии System. GPS. Ареаинформатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346415"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="0f8b2-103">Политика метаданных фотографии System. GPS. Ареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="0f8b2-104">Политика метаданных фотографии для свойства [System. GPS. ареаинформатион](../properties/props-system-gps-areainformation.md) .</span><span class="sxs-lookup"><span data-stu-id="0f8b2-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0f8b2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0f8b2-105">PKEY</span></span>

<span data-ttu-id="0f8b2-106">PKEY \_ GPS \_ ареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="0f8b2-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="0f8b2-107">Containers</span></span>

<span data-ttu-id="0f8b2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0f8b2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0f8b2-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f8b2-109">Read-Only</span></span>

<span data-ttu-id="0f8b2-110">Нет</span><span class="sxs-lookup"><span data-stu-id="0f8b2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0f8b2-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0f8b2-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="0f8b2-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="0f8b2-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="0f8b2-113">Input Type</span></span>

<span data-ttu-id="0f8b2-114">Строка.</span><span class="sxs-lookup"><span data-stu-id="0f8b2-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0f8b2-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="0f8b2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0f8b2-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="0f8b2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0f8b2-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="0f8b2-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0f8b2-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0f8b2-118">Read Paths</span></span>



| <span data-ttu-id="0f8b2-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-119">Order</span></span> | <span data-ttu-id="0f8b2-120">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-120">Path</span></span>                         | <span data-ttu-id="0f8b2-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0f8b2-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0f8b2-122">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-122">1</span></span>     | <span data-ttu-id="0f8b2-123">/APP1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="0f8b2-124">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-124">2</span></span>     | <span data-ttu-id="0f8b2-125">/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="0f8b2-126">Юникод</span><span class="sxs-lookup"><span data-stu-id="0f8b2-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0f8b2-127">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0f8b2-127">Write Paths</span></span>



| <span data-ttu-id="0f8b2-128">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-128">Order</span></span> | <span data-ttu-id="0f8b2-129">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-129">Path</span></span>                         | <span data-ttu-id="0f8b2-130">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0f8b2-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="0f8b2-131">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-131">1</span></span>     | <span data-ttu-id="0f8b2-132">/APP1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="0f8b2-133">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-133">2</span></span>     | <span data-ttu-id="0f8b2-134">/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="0f8b2-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="0f8b2-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0f8b2-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0f8b2-136">Remove Paths</span></span>



| <span data-ttu-id="0f8b2-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-137">Order</span></span> | <span data-ttu-id="0f8b2-138">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="0f8b2-139">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-139">1</span></span>     | <span data-ttu-id="0f8b2-140">/APP1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="0f8b2-141">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-141">2</span></span>     | <span data-ttu-id="0f8b2-142">/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="0f8b2-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="0f8b2-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0f8b2-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="0f8b2-144">Read Paths</span></span>



| <span data-ttu-id="0f8b2-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-145">Order</span></span> | <span data-ttu-id="0f8b2-146">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-146">Path</span></span>                             | <span data-ttu-id="0f8b2-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0f8b2-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0f8b2-148">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-148">1</span></span>     | <span data-ttu-id="0f8b2-149">/ИФД/ГПС/{ушорт = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="0f8b2-150">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-150">2</span></span>     | <span data-ttu-id="0f8b2-151">/ИФД/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="0f8b2-152">Юникод</span><span class="sxs-lookup"><span data-stu-id="0f8b2-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0f8b2-153">Пути записи</span><span class="sxs-lookup"><span data-stu-id="0f8b2-153">Write Paths</span></span>



| <span data-ttu-id="0f8b2-154">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-154">Order</span></span> | <span data-ttu-id="0f8b2-155">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-155">Path</span></span>                             | <span data-ttu-id="0f8b2-156">Формат диска</span><span class="sxs-lookup"><span data-stu-id="0f8b2-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="0f8b2-157">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-157">1</span></span>     | <span data-ttu-id="0f8b2-158">/ИФД/ГПС/{ушорт = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="0f8b2-159">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-159">2</span></span>     | <span data-ttu-id="0f8b2-160">/ИФД/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="0f8b2-161">Юникод</span><span class="sxs-lookup"><span data-stu-id="0f8b2-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0f8b2-162">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="0f8b2-162">Remove Paths</span></span>



| <span data-ttu-id="0f8b2-163">Заказ</span><span class="sxs-lookup"><span data-stu-id="0f8b2-163">Order</span></span> | <span data-ttu-id="0f8b2-164">Путь</span><span class="sxs-lookup"><span data-stu-id="0f8b2-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="0f8b2-165">1</span><span class="sxs-lookup"><span data-stu-id="0f8b2-165">1</span></span>     | <span data-ttu-id="0f8b2-166">/ИФД/ГПС/{ушорт = 28}</span><span class="sxs-lookup"><span data-stu-id="0f8b2-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="0f8b2-167">2</span><span class="sxs-lookup"><span data-stu-id="0f8b2-167">2</span></span>     | <span data-ttu-id="0f8b2-168">/ИФД/КСМП/ексиф: Гпсареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0f8b2-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f8b2-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f8b2-170">См. также</span><span class="sxs-lookup"><span data-stu-id="0f8b2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f8b2-171">System. GPS. Ареаинформатион</span><span class="sxs-lookup"><span data-stu-id="0f8b2-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
