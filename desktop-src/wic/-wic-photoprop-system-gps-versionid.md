---
description: Политика метаданных фотографии для свойства System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Политика метаданных фотографии System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702313"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="a9943-103">Политика метаданных фотографии System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="a9943-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="a9943-104">Политика метаданных фотографии для свойства [System. GPS. VersionID](../properties/props-system-gps-versionid.md) .</span><span class="sxs-lookup"><span data-stu-id="a9943-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a9943-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a9943-105">PKEY</span></span>

<span data-ttu-id="a9943-106">PKEY \_ GPS \_ VersionID</span><span class="sxs-lookup"><span data-stu-id="a9943-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="a9943-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="a9943-107">Containers</span></span>

<span data-ttu-id="a9943-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a9943-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a9943-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9943-109">Read-Only</span></span>

<span data-ttu-id="a9943-110">Нет</span><span class="sxs-lookup"><span data-stu-id="a9943-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a9943-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="a9943-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a9943-112">\_ \| Пользовательский интерфейс VT ВЕКТОРа VT \_</span><span class="sxs-lookup"><span data-stu-id="a9943-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="a9943-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="a9943-113">Input Type</span></span>

<span data-ttu-id="a9943-114">Буфер</span><span class="sxs-lookup"><span data-stu-id="a9943-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a9943-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="a9943-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a9943-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="a9943-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="a9943-117">Политики JPEG</span><span class="sxs-lookup"><span data-stu-id="a9943-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a9943-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a9943-118">Read Paths</span></span>



| <span data-ttu-id="a9943-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-119">Order</span></span> | <span data-ttu-id="a9943-120">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-120">Path</span></span>                     | <span data-ttu-id="a9943-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a9943-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a9943-122">1</span><span class="sxs-lookup"><span data-stu-id="a9943-122">1</span></span>     | <span data-ttu-id="a9943-123">/APP1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="a9943-124">2</span><span class="sxs-lookup"><span data-stu-id="a9943-124">2</span></span>     | <span data-ttu-id="a9943-125">/КСМП/ексиф: Гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="a9943-126">Юникод</span><span class="sxs-lookup"><span data-stu-id="a9943-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a9943-127">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a9943-127">Write Paths</span></span>



| <span data-ttu-id="a9943-128">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-128">Order</span></span> | <span data-ttu-id="a9943-129">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-129">Path</span></span>                     | <span data-ttu-id="a9943-130">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a9943-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a9943-131">1</span><span class="sxs-lookup"><span data-stu-id="a9943-131">1</span></span>     | <span data-ttu-id="a9943-132">/APP1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="a9943-133">2</span><span class="sxs-lookup"><span data-stu-id="a9943-133">2</span></span>     | <span data-ttu-id="a9943-134">/КСМП/ексиф: Гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="a9943-135">Юникод</span><span class="sxs-lookup"><span data-stu-id="a9943-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a9943-136">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a9943-136">Remove Paths</span></span>



| <span data-ttu-id="a9943-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-137">Order</span></span> | <span data-ttu-id="a9943-138">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="a9943-139">1</span><span class="sxs-lookup"><span data-stu-id="a9943-139">1</span></span>     | <span data-ttu-id="a9943-140">/APP1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="a9943-141">2</span><span class="sxs-lookup"><span data-stu-id="a9943-141">2</span></span>     | <span data-ttu-id="a9943-142">/КСМП/ексиф: гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="a9943-143">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="a9943-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a9943-144">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="a9943-144">Read Paths</span></span>



| <span data-ttu-id="a9943-145">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-145">Order</span></span> | <span data-ttu-id="a9943-146">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-146">Path</span></span>                       | <span data-ttu-id="a9943-147">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a9943-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="a9943-148">1</span><span class="sxs-lookup"><span data-stu-id="a9943-148">1</span></span>     | <span data-ttu-id="a9943-149">/ИФД/ГПС/{ушорт = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="a9943-150">2</span><span class="sxs-lookup"><span data-stu-id="a9943-150">2</span></span>     | <span data-ttu-id="a9943-151">/ИФД/КСМП/ексиф: Гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="a9943-152">Юникод</span><span class="sxs-lookup"><span data-stu-id="a9943-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a9943-153">Пути записи</span><span class="sxs-lookup"><span data-stu-id="a9943-153">Write Paths</span></span>



| <span data-ttu-id="a9943-154">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-154">Order</span></span> | <span data-ttu-id="a9943-155">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-155">Path</span></span>                       | <span data-ttu-id="a9943-156">Формат диска</span><span class="sxs-lookup"><span data-stu-id="a9943-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="a9943-157">1</span><span class="sxs-lookup"><span data-stu-id="a9943-157">1</span></span>     | <span data-ttu-id="a9943-158">/ИФД/ГПС/{ушорт = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="a9943-159">2</span><span class="sxs-lookup"><span data-stu-id="a9943-159">2</span></span>     | <span data-ttu-id="a9943-160">/ИФД/КСМП/ексиф: Гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="a9943-161">Юникод</span><span class="sxs-lookup"><span data-stu-id="a9943-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a9943-162">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="a9943-162">Remove Paths</span></span>



| <span data-ttu-id="a9943-163">Заказ</span><span class="sxs-lookup"><span data-stu-id="a9943-163">Order</span></span> | <span data-ttu-id="a9943-164">Путь</span><span class="sxs-lookup"><span data-stu-id="a9943-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="a9943-165">1</span><span class="sxs-lookup"><span data-stu-id="a9943-165">1</span></span>     | <span data-ttu-id="a9943-166">/ИФД/ГПС/{ушорт = 0}</span><span class="sxs-lookup"><span data-stu-id="a9943-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="a9943-167">2</span><span class="sxs-lookup"><span data-stu-id="a9943-167">2</span></span>     | <span data-ttu-id="a9943-168">/ИФД/КСМП/ексиф: гпсверсионид</span><span class="sxs-lookup"><span data-stu-id="a9943-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a9943-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9943-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9943-170">См. также</span><span class="sxs-lookup"><span data-stu-id="a9943-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9943-171">System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="a9943-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
