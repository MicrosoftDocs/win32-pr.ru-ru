---
description: Политика метаданных фотографии для свойства System. photo. Експосуребиас.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Политика метаданных фото для System. photo. Експосуребиас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674006"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="ff615-103">Политика метаданных фото для System. photo. Експосуребиас</span><span class="sxs-lookup"><span data-stu-id="ff615-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="ff615-104">Политика метаданных фотографии для свойства [System. photo. експосуребиас](../properties/props-system-photo-exposurebias.md) .</span><span class="sxs-lookup"><span data-stu-id="ff615-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ff615-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ff615-105">PKEY</span></span>

<span data-ttu-id="ff615-106">\_Експосуребиас фото на PKEY \_</span><span class="sxs-lookup"><span data-stu-id="ff615-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="ff615-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="ff615-107">Containers</span></span>

<span data-ttu-id="ff615-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ff615-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ff615-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff615-109">Read-Only</span></span>

<span data-ttu-id="ff615-110">Да</span><span class="sxs-lookup"><span data-stu-id="ff615-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ff615-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="ff615-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ff615-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="ff615-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ff615-113">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="ff615-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="ff615-114">Это значение формируется из System. photo. Експосуребиаснумератор и System. photo. Експосуребиасденоминатор.</span><span class="sxs-lookup"><span data-stu-id="ff615-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="ff615-115">Он не может быть записан напрямую.</span><span class="sxs-lookup"><span data-stu-id="ff615-115">It cannot be written directly.</span></span> <span data-ttu-id="ff615-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="ff615-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ff615-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="ff615-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ff615-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ff615-118">Read Paths</span></span>



| <span data-ttu-id="ff615-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-119">Order</span></span> | <span data-ttu-id="ff615-120">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-120">Path</span></span>                          | <span data-ttu-id="ff615-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ff615-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ff615-122">1</span><span class="sxs-lookup"><span data-stu-id="ff615-122">1</span></span>     | <span data-ttu-id="ff615-123">/APP1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="ff615-124">2</span><span class="sxs-lookup"><span data-stu-id="ff615-124">2</span></span>     | <span data-ttu-id="ff615-125">/КСМП/ексиф: Експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="ff615-126">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ff615-126">Write Paths</span></span>



| <span data-ttu-id="ff615-127">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-127">Order</span></span> | <span data-ttu-id="ff615-128">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-128">Path</span></span>                          | <span data-ttu-id="ff615-129">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ff615-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="ff615-130">1</span><span class="sxs-lookup"><span data-stu-id="ff615-130">1</span></span>     | <span data-ttu-id="ff615-131">/APP1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="ff615-132">2</span><span class="sxs-lookup"><span data-stu-id="ff615-132">2</span></span>     | <span data-ttu-id="ff615-133">/КСМП/ексиф: Експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ff615-134">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ff615-134">Remove Paths</span></span>



| <span data-ttu-id="ff615-135">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-135">Order</span></span> | <span data-ttu-id="ff615-136">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ff615-137">1</span><span class="sxs-lookup"><span data-stu-id="ff615-137">1</span></span>     | <span data-ttu-id="ff615-138">/APP1/IFD/EXIF/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="ff615-139">2</span><span class="sxs-lookup"><span data-stu-id="ff615-139">2</span></span>     | <span data-ttu-id="ff615-140">/КСМП/ексиф: експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="ff615-141">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="ff615-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ff615-142">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="ff615-142">Read Paths</span></span>



| <span data-ttu-id="ff615-143">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-143">Order</span></span> | <span data-ttu-id="ff615-144">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-144">Path</span></span>                            | <span data-ttu-id="ff615-145">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ff615-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="ff615-146">1</span><span class="sxs-lookup"><span data-stu-id="ff615-146">1</span></span>     | <span data-ttu-id="ff615-147">/ИФД/ексиф/{ушорт = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="ff615-148">2</span><span class="sxs-lookup"><span data-stu-id="ff615-148">2</span></span>     | <span data-ttu-id="ff615-149">/ИФД/КСМП/ексиф: Експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="ff615-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="ff615-150">Write Paths</span></span>



| <span data-ttu-id="ff615-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-151">Order</span></span> | <span data-ttu-id="ff615-152">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-152">Path</span></span>                            | <span data-ttu-id="ff615-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="ff615-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="ff615-154">1</span><span class="sxs-lookup"><span data-stu-id="ff615-154">1</span></span>     | <span data-ttu-id="ff615-155">/ИФД/ексиф/{ушорт = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="ff615-156">2</span><span class="sxs-lookup"><span data-stu-id="ff615-156">2</span></span>     | <span data-ttu-id="ff615-157">/ИФД/КСМП/ексиф: Експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="ff615-158">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="ff615-158">Remove Paths</span></span>



| <span data-ttu-id="ff615-159">Заказ</span><span class="sxs-lookup"><span data-stu-id="ff615-159">Order</span></span> | <span data-ttu-id="ff615-160">Путь</span><span class="sxs-lookup"><span data-stu-id="ff615-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="ff615-161">1</span><span class="sxs-lookup"><span data-stu-id="ff615-161">1</span></span>     | <span data-ttu-id="ff615-162">/ИФД/ексиф/{ушорт = 37380}</span><span class="sxs-lookup"><span data-stu-id="ff615-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="ff615-163">2</span><span class="sxs-lookup"><span data-stu-id="ff615-163">2</span></span>     | <span data-ttu-id="ff615-164">/ИФД/КСМП/ексиф: експосуребиасвалуе</span><span class="sxs-lookup"><span data-stu-id="ff615-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ff615-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff615-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff615-166">См. также</span><span class="sxs-lookup"><span data-stu-id="ff615-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff615-167">System. photo. Експосуребиас</span><span class="sxs-lookup"><span data-stu-id="ff615-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
