---
description: Политика метаданных фотографии для свойства System. photo. ФотометриЦинтерпретатион.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Политика метаданных фото для System. photo. ФотометриЦинтерпретатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674130"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="ed598-103">Политика метаданных фото для System. photo. ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="ed598-104">Политика метаданных фотографии для свойства [System. photo. фотометриЦинтерпретатион](../properties/props-system-photo-photometricinterpretation.md) .</span><span class="sxs-lookup"><span data-stu-id="ed598-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed598-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ed598-105">PKEY</span></span>

<span data-ttu-id="ed598-106">\_ФотометриЦинтерпретатион фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="ed598-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="ed598-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="ed598-107">Containers</span></span>

<span data-ttu-id="ed598-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ed598-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed598-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed598-109">Read-Only</span></span>

<span data-ttu-id="ed598-110">Да</span><span class="sxs-lookup"><span data-stu-id="ed598-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed598-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="ed598-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed598-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="ed598-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="ed598-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="ed598-113">Input Type</span></span>

<span data-ttu-id="ed598-114">UShort</span><span class="sxs-lookup"><span data-stu-id="ed598-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed598-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="ed598-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed598-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="ed598-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed598-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="ed598-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed598-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ed598-118">Read Paths</span></span>



| <span data-ttu-id="ed598-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-119">Order</span></span> | <span data-ttu-id="ed598-120">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-120">Path</span></span>                                | <span data-ttu-id="ed598-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ed598-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="ed598-122">1</span><span class="sxs-lookup"><span data-stu-id="ed598-122">1</span></span>     | <span data-ttu-id="ed598-123">/APP1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="ed598-124">ushort</span><span class="sxs-lookup"><span data-stu-id="ed598-124">ushort</span></span>      |
| <span data-ttu-id="ed598-125">2</span><span class="sxs-lookup"><span data-stu-id="ed598-125">2</span></span>     | <span data-ttu-id="ed598-126">/КСМП/Тифф: ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="ed598-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="ed598-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed598-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ed598-128">Write Paths</span></span>



| <span data-ttu-id="ed598-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-129">Order</span></span> | <span data-ttu-id="ed598-130">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-130">Path</span></span>                                | <span data-ttu-id="ed598-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ed598-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="ed598-132">1</span><span class="sxs-lookup"><span data-stu-id="ed598-132">1</span></span>     | <span data-ttu-id="ed598-133">/APP1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="ed598-134">ushort</span><span class="sxs-lookup"><span data-stu-id="ed598-134">ushort</span></span>      |
| <span data-ttu-id="ed598-135">2</span><span class="sxs-lookup"><span data-stu-id="ed598-135">2</span></span>     | <span data-ttu-id="ed598-136">/КСМП/Тифф: ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="ed598-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="ed598-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed598-138">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ed598-138">Remove Paths</span></span>



| <span data-ttu-id="ed598-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-139">Order</span></span> | <span data-ttu-id="ed598-140">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="ed598-141">1</span><span class="sxs-lookup"><span data-stu-id="ed598-141">1</span></span>     | <span data-ttu-id="ed598-142">/APP1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="ed598-143">2</span><span class="sxs-lookup"><span data-stu-id="ed598-143">2</span></span>     | <span data-ttu-id="ed598-144">/КСМП/Тифф: фотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ed598-145">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="ed598-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed598-146">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ed598-146">Read Paths</span></span>



| <span data-ttu-id="ed598-147">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-147">Order</span></span> | <span data-ttu-id="ed598-148">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-148">Path</span></span>                                    | <span data-ttu-id="ed598-149">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ed598-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="ed598-150">1</span><span class="sxs-lookup"><span data-stu-id="ed598-150">1</span></span>     | <span data-ttu-id="ed598-151">/ИФД/{ушорт = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="ed598-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ed598-152">ushort</span></span>      |
| <span data-ttu-id="ed598-153">2</span><span class="sxs-lookup"><span data-stu-id="ed598-153">2</span></span>     | <span data-ttu-id="ed598-154">/ИФД/КСМП/Тифф: ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="ed598-155">Юникод</span><span class="sxs-lookup"><span data-stu-id="ed598-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed598-156">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ed598-156">Write Paths</span></span>



| <span data-ttu-id="ed598-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-157">Order</span></span> | <span data-ttu-id="ed598-158">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-158">Path</span></span>                                    | <span data-ttu-id="ed598-159">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ed598-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="ed598-160">1</span><span class="sxs-lookup"><span data-stu-id="ed598-160">1</span></span>     | <span data-ttu-id="ed598-161">/ИФД/{ушорт = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="ed598-162">ushort</span><span class="sxs-lookup"><span data-stu-id="ed598-162">ushort</span></span>      |
| <span data-ttu-id="ed598-163">2</span><span class="sxs-lookup"><span data-stu-id="ed598-163">2</span></span>     | <span data-ttu-id="ed598-164">/ИФД/КСМП/Тифф: ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="ed598-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="ed598-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed598-166">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ed598-166">Remove Paths</span></span>



| <span data-ttu-id="ed598-167">Заказ</span><span class="sxs-lookup"><span data-stu-id="ed598-167">Order</span></span> | <span data-ttu-id="ed598-168">Путь</span><span class="sxs-lookup"><span data-stu-id="ed598-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="ed598-169">1</span><span class="sxs-lookup"><span data-stu-id="ed598-169">1</span></span>     | <span data-ttu-id="ed598-170">/ИФД/{ушорт = 262}</span><span class="sxs-lookup"><span data-stu-id="ed598-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="ed598-171">2</span><span class="sxs-lookup"><span data-stu-id="ed598-171">2</span></span>     | <span data-ttu-id="ed598-172">/ИФД/КСМП/Тифф: фотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed598-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed598-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed598-174">См. также</span><span class="sxs-lookup"><span data-stu-id="ed598-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed598-175">System. photo. ФотометриЦинтерпретатион</span><span class="sxs-lookup"><span data-stu-id="ed598-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
