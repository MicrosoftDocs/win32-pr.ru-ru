---
description: Политика метаданных фотографии для свойства System. photo. Макерноте.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Политика метаданных фото для System. photo. Макерноте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673873"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a><span data-ttu-id="31e48-103">Политика метаданных фото для System. photo. Макерноте</span><span class="sxs-lookup"><span data-stu-id="31e48-103">System.Photo.MakerNote Photo Metadata Policy</span></span>

<span data-ttu-id="31e48-104">Политика метаданных фотографии для свойства [System. photo. макерноте](../properties/props-system-photo-makernote.md) .</span><span class="sxs-lookup"><span data-stu-id="31e48-104">The photo metadata policy for the [System.Photo.MakerNote](../properties/props-system-photo-makernote.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="31e48-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="31e48-105">PKEY</span></span>

<span data-ttu-id="31e48-106">\_Макерноте фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="31e48-106">PKEY\_Photo\_MakerNote</span></span>

### <a name="containers"></a><span data-ttu-id="31e48-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="31e48-107">Containers</span></span>

<span data-ttu-id="31e48-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="31e48-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="31e48-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="31e48-109">Read-Only</span></span>

<span data-ttu-id="31e48-110">Нет</span><span class="sxs-lookup"><span data-stu-id="31e48-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="31e48-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="31e48-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="31e48-112">\_Векторный \| VTUI1 VT</span><span class="sxs-lookup"><span data-stu-id="31e48-112">VT\_VECTOR \| VTUI1</span></span>

### <a name="input-type"></a><span data-ttu-id="31e48-113">Тип входных данных</span><span class="sxs-lookup"><span data-stu-id="31e48-113">Input Type</span></span>

<span data-ttu-id="31e48-114">Буфер</span><span class="sxs-lookup"><span data-stu-id="31e48-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="31e48-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="31e48-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="31e48-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="31e48-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="31e48-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="31e48-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="31e48-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="31e48-118">Read Paths</span></span>



| <span data-ttu-id="31e48-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-119">Order</span></span> | <span data-ttu-id="31e48-120">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-120">Path</span></span>                          | <span data-ttu-id="31e48-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="31e48-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="31e48-122">1</span><span class="sxs-lookup"><span data-stu-id="31e48-122">1</span></span>     | <span data-ttu-id="31e48-123">/APP1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-123">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="31e48-124">Пути записи</span><span class="sxs-lookup"><span data-stu-id="31e48-124">Write Paths</span></span>



| <span data-ttu-id="31e48-125">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-125">Order</span></span> | <span data-ttu-id="31e48-126">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-126">Path</span></span>                          | <span data-ttu-id="31e48-127">Формат диска</span><span class="sxs-lookup"><span data-stu-id="31e48-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="31e48-128">1</span><span class="sxs-lookup"><span data-stu-id="31e48-128">1</span></span>     | <span data-ttu-id="31e48-129">/APP1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-129">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="31e48-130">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="31e48-130">Remove Paths</span></span>



| <span data-ttu-id="31e48-131">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-131">Order</span></span> | <span data-ttu-id="31e48-132">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-132">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="31e48-133">1</span><span class="sxs-lookup"><span data-stu-id="31e48-133">1</span></span>     | <span data-ttu-id="31e48-134">/APP1/IFD/EXIF/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-134">/app1/ifd/exif/{ushort=37500}</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="31e48-135">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="31e48-135">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="31e48-136">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="31e48-136">Read Paths</span></span>



| <span data-ttu-id="31e48-137">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-137">Order</span></span> | <span data-ttu-id="31e48-138">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-138">Path</span></span>                     | <span data-ttu-id="31e48-139">Формат диска</span><span class="sxs-lookup"><span data-stu-id="31e48-139">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="31e48-140">1</span><span class="sxs-lookup"><span data-stu-id="31e48-140">1</span></span>     | <span data-ttu-id="31e48-141">/ИФД/ексиф/{ушорт = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-141">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="31e48-142">Пути записи</span><span class="sxs-lookup"><span data-stu-id="31e48-142">Write Paths</span></span>



| <span data-ttu-id="31e48-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-143">Order</span></span> | <span data-ttu-id="31e48-144">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-144">Path</span></span>                     | <span data-ttu-id="31e48-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="31e48-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="31e48-146">1</span><span class="sxs-lookup"><span data-stu-id="31e48-146">1</span></span>     | <span data-ttu-id="31e48-147">/ИФД/ексиф/{ушорт = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-147">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="31e48-148">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="31e48-148">Remove Paths</span></span>



| <span data-ttu-id="31e48-149">Заказ</span><span class="sxs-lookup"><span data-stu-id="31e48-149">Order</span></span> | <span data-ttu-id="31e48-150">Путь</span><span class="sxs-lookup"><span data-stu-id="31e48-150">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="31e48-151">1</span><span class="sxs-lookup"><span data-stu-id="31e48-151">1</span></span>     | <span data-ttu-id="31e48-152">/ИФД/ексиф/{ушорт = 37500}</span><span class="sxs-lookup"><span data-stu-id="31e48-152">/ifd/exif/{ushort=37500}</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="31e48-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31e48-153">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="31e48-154">См. также</span><span class="sxs-lookup"><span data-stu-id="31e48-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31e48-155">System. photo. Макерноте</span><span class="sxs-lookup"><span data-stu-id="31e48-155">System.Photo.MakerNote</span></span>](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
