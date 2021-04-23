---
description: Политика метаданных фотографии для свойства System. GPS. Высота.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Политика метаданных фото System. GPS. Высота
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712802"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="4ec15-103">Политика метаданных фото System. GPS. Высота</span><span class="sxs-lookup"><span data-stu-id="4ec15-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="4ec15-104">Политика метаданных фотографии для свойства [System. GPS. Высота](../properties/props-system-gps-altitude.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec15-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4ec15-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4ec15-105">PKEY</span></span>

<span data-ttu-id="4ec15-106">По \_ высоте GPS на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="4ec15-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="4ec15-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4ec15-107">Description</span></span>

<span data-ttu-id="4ec15-108">Высота указывается в виде абсолютного значения, на которое ссылается измерительные единицы.</span><span class="sxs-lookup"><span data-stu-id="4ec15-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="4ec15-109">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="4ec15-109">Containers</span></span>

<span data-ttu-id="4ec15-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4ec15-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4ec15-111">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4ec15-111">Read-Only</span></span>

<span data-ttu-id="4ec15-112">Да</span><span class="sxs-lookup"><span data-stu-id="4ec15-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4ec15-113">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="4ec15-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4ec15-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4ec15-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4ec15-115">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="4ec15-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4ec15-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4ec15-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4ec15-117">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="4ec15-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="4ec15-118">Это значение можно записать, записав в System. GPS. Высота. числитель и System. GPS. Высота. знаменатель.</span><span class="sxs-lookup"><span data-stu-id="4ec15-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="4ec15-119">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="4ec15-119">It cannot be written directly.</span></span> <span data-ttu-id="4ec15-120">Пути записи в следующих таблицах указывают, где значение может быть сохранено при его создании, а не когда оно записывается напрямую.</span><span class="sxs-lookup"><span data-stu-id="4ec15-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="4ec15-121">При считывании значения из разных схем выверятся.</span><span class="sxs-lookup"><span data-stu-id="4ec15-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4ec15-122">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="4ec15-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ec15-123">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="4ec15-123">Read Paths</span></span>



| <span data-ttu-id="4ec15-124">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-124">Order</span></span> | <span data-ttu-id="4ec15-125">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-125">Path</span></span>                     | <span data-ttu-id="4ec15-126">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4ec15-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4ec15-127">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-127">1</span></span>     | <span data-ttu-id="4ec15-128">/APP1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="4ec15-129">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-129">2</span></span>     | <span data-ttu-id="4ec15-130">/КСМП/ексиф: Гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="4ec15-131">Пути записи</span><span class="sxs-lookup"><span data-stu-id="4ec15-131">Write Paths</span></span>



| <span data-ttu-id="4ec15-132">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-132">Order</span></span> | <span data-ttu-id="4ec15-133">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-133">Path</span></span>                     | <span data-ttu-id="4ec15-134">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4ec15-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4ec15-135">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-135">1</span></span>     | <span data-ttu-id="4ec15-136">/APP1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="4ec15-137">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-137">2</span></span>     | <span data-ttu-id="4ec15-138">/КСМП/ексиф: Гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4ec15-139">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="4ec15-139">Remove Paths</span></span>



| <span data-ttu-id="4ec15-140">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-140">Order</span></span> | <span data-ttu-id="4ec15-141">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4ec15-142">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-142">1</span></span>     | <span data-ttu-id="4ec15-143">/APP1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="4ec15-144">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-144">2</span></span>     | <span data-ttu-id="4ec15-145">/КСМП/ексиф: гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="4ec15-146">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="4ec15-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ec15-147">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="4ec15-147">Read Paths</span></span>



| <span data-ttu-id="4ec15-148">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-148">Order</span></span> | <span data-ttu-id="4ec15-149">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-149">Path</span></span>                      | <span data-ttu-id="4ec15-150">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4ec15-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4ec15-151">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-151">1</span></span>     | <span data-ttu-id="4ec15-152">/ИФД/ГПС/{ушорт = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="4ec15-153">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-153">2</span></span>     | <span data-ttu-id="4ec15-154">/ИФД/КСМП/ексиф: Гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4ec15-155">Пути записи</span><span class="sxs-lookup"><span data-stu-id="4ec15-155">Write Paths</span></span>



| <span data-ttu-id="4ec15-156">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-156">Order</span></span> | <span data-ttu-id="4ec15-157">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-157">Path</span></span>                      | <span data-ttu-id="4ec15-158">Формат диска</span><span class="sxs-lookup"><span data-stu-id="4ec15-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4ec15-159">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-159">1</span></span>     | <span data-ttu-id="4ec15-160">/ИФД/ГПС/{ушорт = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="4ec15-161">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-161">2</span></span>     | <span data-ttu-id="4ec15-162">/ИФД/КСМП/ексиф: Гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4ec15-163">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="4ec15-163">Remove Paths</span></span>



| <span data-ttu-id="4ec15-164">Заказ</span><span class="sxs-lookup"><span data-stu-id="4ec15-164">Order</span></span> | <span data-ttu-id="4ec15-165">Путь</span><span class="sxs-lookup"><span data-stu-id="4ec15-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="4ec15-166">1</span><span class="sxs-lookup"><span data-stu-id="4ec15-166">1</span></span>     | <span data-ttu-id="4ec15-167">/ИФД/ГПС/{ушорт = 6}</span><span class="sxs-lookup"><span data-stu-id="4ec15-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="4ec15-168">2</span><span class="sxs-lookup"><span data-stu-id="4ec15-168">2</span></span>     | <span data-ttu-id="4ec15-169">/ИФД/КСМП/ексиф: гпсалтитуде</span><span class="sxs-lookup"><span data-stu-id="4ec15-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="4ec15-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ec15-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ec15-171">См. также</span><span class="sxs-lookup"><span data-stu-id="4ec15-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec15-172">System. GPS. Высота</span><span class="sxs-lookup"><span data-stu-id="4ec15-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
