---
description: Политика метаданных фотографии для свойства System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Политика метаданных фотографии System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683570"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="8de1d-103">Политика метаданных фотографии System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="8de1d-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="8de1d-104">Политика метаданных фотографии для свойства [System. GPS. status](../properties/props-system-gps-status.md) .</span><span class="sxs-lookup"><span data-stu-id="8de1d-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8de1d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8de1d-105">PKEY</span></span>

<span data-ttu-id="8de1d-106">\_Состояние состояния GPS "PKEY" \_</span><span class="sxs-lookup"><span data-stu-id="8de1d-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="8de1d-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="8de1d-107">Containers</span></span>

<span data-ttu-id="8de1d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8de1d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8de1d-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8de1d-109">Read-Only</span></span>

<span data-ttu-id="8de1d-110">Нет</span><span class="sxs-lookup"><span data-stu-id="8de1d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8de1d-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="8de1d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8de1d-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="8de1d-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8de1d-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="8de1d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8de1d-114">VT \_ LPWSTR является предпочтительным, но \_ также принимается VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="8de1d-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8de1d-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="8de1d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8de1d-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="8de1d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="8de1d-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="8de1d-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8de1d-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8de1d-118">Read Paths</span></span>



| <span data-ttu-id="8de1d-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-119">Order</span></span> | <span data-ttu-id="8de1d-120">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-120">Path</span></span>                     | <span data-ttu-id="8de1d-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8de1d-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8de1d-122">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-122">1</span></span>     | <span data-ttu-id="8de1d-123">/APP1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="8de1d-124">ascii</span><span class="sxs-lookup"><span data-stu-id="8de1d-124">ascii</span></span>       |
| <span data-ttu-id="8de1d-125">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-125">2</span></span>     | <span data-ttu-id="8de1d-126">/КСМП/ексиф: Гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="8de1d-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="8de1d-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8de1d-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8de1d-128">Write Paths</span></span>



| <span data-ttu-id="8de1d-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-129">Order</span></span> | <span data-ttu-id="8de1d-130">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-130">Path</span></span>                     | <span data-ttu-id="8de1d-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8de1d-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="8de1d-132">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-132">1</span></span>     | <span data-ttu-id="8de1d-133">/APP1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="8de1d-134">ascii</span><span class="sxs-lookup"><span data-stu-id="8de1d-134">ascii</span></span>       |
| <span data-ttu-id="8de1d-135">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-135">2</span></span>     | <span data-ttu-id="8de1d-136">/КСМП/ексиф: Гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="8de1d-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="8de1d-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8de1d-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8de1d-138">Remove Paths</span></span>



| <span data-ttu-id="8de1d-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-139">Order</span></span> | <span data-ttu-id="8de1d-140">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="8de1d-141">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-141">1</span></span>     | <span data-ttu-id="8de1d-142">/APP1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="8de1d-143">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-143">2</span></span>     | <span data-ttu-id="8de1d-144">/КСМП/ексиф: гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="8de1d-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="8de1d-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8de1d-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="8de1d-146">Read Paths</span></span>



| <span data-ttu-id="8de1d-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-147">Order</span></span> | <span data-ttu-id="8de1d-148">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-148">Path</span></span>                    | <span data-ttu-id="8de1d-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8de1d-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="8de1d-150">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-150">1</span></span>     | <span data-ttu-id="8de1d-151">/ИФД/ГПС/{ушорт = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="8de1d-152">ascii</span><span class="sxs-lookup"><span data-stu-id="8de1d-152">ascii</span></span>       |
| <span data-ttu-id="8de1d-153">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-153">2</span></span>     | <span data-ttu-id="8de1d-154">/ИФД/КСМП/ексиф: Гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="8de1d-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="8de1d-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8de1d-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="8de1d-156">Write Paths</span></span>



| <span data-ttu-id="8de1d-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-157">Order</span></span> | <span data-ttu-id="8de1d-158">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-158">Path</span></span>                    | <span data-ttu-id="8de1d-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="8de1d-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="8de1d-160">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-160">1</span></span>     | <span data-ttu-id="8de1d-161">/ИФД/ГПС/{ушорт = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="8de1d-162">ascii</span><span class="sxs-lookup"><span data-stu-id="8de1d-162">ascii</span></span>       |
| <span data-ttu-id="8de1d-163">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-163">2</span></span>     | <span data-ttu-id="8de1d-164">/ИФД/КСМП/ексиф: Гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="8de1d-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="8de1d-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8de1d-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="8de1d-166">Remove Paths</span></span>



| <span data-ttu-id="8de1d-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="8de1d-167">Order</span></span> | <span data-ttu-id="8de1d-168">Путь</span><span class="sxs-lookup"><span data-stu-id="8de1d-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="8de1d-169">1</span><span class="sxs-lookup"><span data-stu-id="8de1d-169">1</span></span>     | <span data-ttu-id="8de1d-170">/ИФД/ГПС/{ушорт = 9}</span><span class="sxs-lookup"><span data-stu-id="8de1d-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="8de1d-171">2</span><span class="sxs-lookup"><span data-stu-id="8de1d-171">2</span></span>     | <span data-ttu-id="8de1d-172">/ИФД/КСМП/ексиф: гпсстатус</span><span class="sxs-lookup"><span data-stu-id="8de1d-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8de1d-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8de1d-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de1d-174">См. также</span><span class="sxs-lookup"><span data-stu-id="8de1d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de1d-175">System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="8de1d-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
