---
description: Политика метаданных фотографии для свойства System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Политика метаданных фотографии System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272297"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="c6764-103">Политика метаданных фотографии System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="c6764-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="c6764-104">Политика метаданных фотографии для свойства [System. GPS. Date](../properties/props-system-gps-date.md) .</span><span class="sxs-lookup"><span data-stu-id="c6764-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c6764-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c6764-105">PKEY</span></span>

<span data-ttu-id="c6764-106">Дата и время \_ GPS \_</span><span class="sxs-lookup"><span data-stu-id="c6764-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="c6764-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="c6764-107">Containers</span></span>

<span data-ttu-id="c6764-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6764-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c6764-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c6764-109">Read-Only</span></span>

<span data-ttu-id="c6764-110">Нет</span><span class="sxs-lookup"><span data-stu-id="c6764-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="c6764-111">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="c6764-111">Input Type</span></span>

<span data-ttu-id="c6764-112">Строка.</span><span class="sxs-lookup"><span data-stu-id="c6764-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c6764-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="c6764-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c6764-114">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="c6764-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c6764-115">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="c6764-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c6764-116">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c6764-116">Read Paths</span></span>



| <span data-ttu-id="c6764-117">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-117">Order</span></span> | <span data-ttu-id="c6764-118">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-118">Path</span></span>                      | <span data-ttu-id="c6764-119">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c6764-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c6764-120">1</span><span class="sxs-lookup"><span data-stu-id="c6764-120">1</span></span>     | <span data-ttu-id="c6764-121">/APP1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="c6764-122">ascii</span><span class="sxs-lookup"><span data-stu-id="c6764-122">ascii</span></span>       |
| <span data-ttu-id="c6764-123">2</span><span class="sxs-lookup"><span data-stu-id="c6764-123">2</span></span>     | <span data-ttu-id="c6764-124">/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="c6764-125">Юникод</span><span class="sxs-lookup"><span data-stu-id="c6764-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c6764-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c6764-126">Write Paths</span></span>



| <span data-ttu-id="c6764-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-127">Order</span></span> | <span data-ttu-id="c6764-128">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-128">Path</span></span>                      | <span data-ttu-id="c6764-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c6764-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c6764-130">1</span><span class="sxs-lookup"><span data-stu-id="c6764-130">1</span></span>     | <span data-ttu-id="c6764-131">/APP1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="c6764-132">ascii</span><span class="sxs-lookup"><span data-stu-id="c6764-132">ascii</span></span>       |
| <span data-ttu-id="c6764-133">2</span><span class="sxs-lookup"><span data-stu-id="c6764-133">2</span></span>     | <span data-ttu-id="c6764-134">/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="c6764-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="c6764-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c6764-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c6764-136">Remove Paths</span></span>



| <span data-ttu-id="c6764-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-137">Order</span></span> | <span data-ttu-id="c6764-138">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c6764-139">1</span><span class="sxs-lookup"><span data-stu-id="c6764-139">1</span></span>     | <span data-ttu-id="c6764-140">/APP1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="c6764-141">2</span><span class="sxs-lookup"><span data-stu-id="c6764-141">2</span></span>     | <span data-ttu-id="c6764-142">/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="c6764-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="c6764-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c6764-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="c6764-144">Read Paths</span></span>



| <span data-ttu-id="c6764-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-145">Order</span></span> | <span data-ttu-id="c6764-146">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-146">Path</span></span>                       | <span data-ttu-id="c6764-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c6764-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c6764-148">1</span><span class="sxs-lookup"><span data-stu-id="c6764-148">1</span></span>     | <span data-ttu-id="c6764-149">/ИФД/ГПС/{ушорт = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="c6764-150">ascii</span><span class="sxs-lookup"><span data-stu-id="c6764-150">ascii</span></span>       |
| <span data-ttu-id="c6764-151">2</span><span class="sxs-lookup"><span data-stu-id="c6764-151">2</span></span>     | <span data-ttu-id="c6764-152">/ИФД/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="c6764-153">Юникод</span><span class="sxs-lookup"><span data-stu-id="c6764-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c6764-154">Пути записи</span><span class="sxs-lookup"><span data-stu-id="c6764-154">Write Paths</span></span>



| <span data-ttu-id="c6764-155">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-155">Order</span></span> | <span data-ttu-id="c6764-156">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-156">Path</span></span>                       | <span data-ttu-id="c6764-157">Формат диска</span><span class="sxs-lookup"><span data-stu-id="c6764-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c6764-158">1</span><span class="sxs-lookup"><span data-stu-id="c6764-158">1</span></span>     | <span data-ttu-id="c6764-159">/ИФД/ГПС/{ушорт = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="c6764-160">ascii</span><span class="sxs-lookup"><span data-stu-id="c6764-160">ascii</span></span>       |
| <span data-ttu-id="c6764-161">2</span><span class="sxs-lookup"><span data-stu-id="c6764-161">2</span></span>     | <span data-ttu-id="c6764-162">/ИФД/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="c6764-163">Юникод</span><span class="sxs-lookup"><span data-stu-id="c6764-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c6764-164">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="c6764-164">Remove Paths</span></span>



| <span data-ttu-id="c6764-165">Заказ</span><span class="sxs-lookup"><span data-stu-id="c6764-165">Order</span></span> | <span data-ttu-id="c6764-166">Путь</span><span class="sxs-lookup"><span data-stu-id="c6764-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="c6764-167">1</span><span class="sxs-lookup"><span data-stu-id="c6764-167">1</span></span>     | <span data-ttu-id="c6764-168">/ИФД/ГПС/{ушорт = 29}</span><span class="sxs-lookup"><span data-stu-id="c6764-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="c6764-169">2</span><span class="sxs-lookup"><span data-stu-id="c6764-169">2</span></span>     | <span data-ttu-id="c6764-170">/ИФД/КСМП/ексиф: Гпстиместамп</span><span class="sxs-lookup"><span data-stu-id="c6764-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6764-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6764-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6764-172">См. также</span><span class="sxs-lookup"><span data-stu-id="c6764-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6764-173">System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="c6764-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
