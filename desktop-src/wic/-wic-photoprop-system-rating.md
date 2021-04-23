---
description: Политика метаданных фотографии для свойства System. рейтингов.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Политика метаданных фотографии System. рейтингов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347175"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="96640-103">Политика метаданных фотографии System. рейтингов</span><span class="sxs-lookup"><span data-stu-id="96640-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="96640-104">Политика метаданных фотографии для свойства [System. рейтингов](../properties/props-system-rating.md) .</span><span class="sxs-lookup"><span data-stu-id="96640-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="96640-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="96640-105">PKEY</span></span>

<span data-ttu-id="96640-106">\_Оценка PKEY</span><span class="sxs-lookup"><span data-stu-id="96640-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="96640-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="96640-107">Containers</span></span>

<span data-ttu-id="96640-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="96640-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="96640-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="96640-109">Read-Only</span></span>

<span data-ttu-id="96640-110">Нет</span><span class="sxs-lookup"><span data-stu-id="96640-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="96640-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="96640-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="96640-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="96640-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="96640-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="96640-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="96640-114">Может быть VT \_ UI1, VT \_ UI2 или VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="96640-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="96640-115">Значение может находиться в диапазоне от 0 до 99.</span><span class="sxs-lookup"><span data-stu-id="96640-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="96640-116">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="96640-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="96640-117">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="96640-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="96640-118">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="96640-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="96640-119">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="96640-119">Read Paths</span></span>



| <span data-ttu-id="96640-120">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-120">Order</span></span> | <span data-ttu-id="96640-121">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-121">Path</span></span>                       | <span data-ttu-id="96640-122">Формат диска</span><span class="sxs-lookup"><span data-stu-id="96640-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="96640-123">1</span><span class="sxs-lookup"><span data-stu-id="96640-123">1</span></span>     | <span data-ttu-id="96640-124">/APP1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="96640-125">ushort</span><span class="sxs-lookup"><span data-stu-id="96640-125">ushort</span></span>      |
| <span data-ttu-id="96640-126">2</span><span class="sxs-lookup"><span data-stu-id="96640-126">2</span></span>     | <span data-ttu-id="96640-127">/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="96640-128">Юникод</span><span class="sxs-lookup"><span data-stu-id="96640-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="96640-129">Пути записи</span><span class="sxs-lookup"><span data-stu-id="96640-129">Write Paths</span></span>



| <span data-ttu-id="96640-130">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-130">Order</span></span> | <span data-ttu-id="96640-131">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-131">Path</span></span>                       | <span data-ttu-id="96640-132">Формат диска</span><span class="sxs-lookup"><span data-stu-id="96640-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="96640-133">1</span><span class="sxs-lookup"><span data-stu-id="96640-133">1</span></span>     | <span data-ttu-id="96640-134">/APP1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="96640-135">ushort</span><span class="sxs-lookup"><span data-stu-id="96640-135">ushort</span></span>      |
| <span data-ttu-id="96640-136">2</span><span class="sxs-lookup"><span data-stu-id="96640-136">2</span></span>     | <span data-ttu-id="96640-137">/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="96640-138">Юникод</span><span class="sxs-lookup"><span data-stu-id="96640-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="96640-139">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="96640-139">Remove Paths</span></span>



| <span data-ttu-id="96640-140">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-140">Order</span></span> | <span data-ttu-id="96640-141">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="96640-142">1</span><span class="sxs-lookup"><span data-stu-id="96640-142">1</span></span>     | <span data-ttu-id="96640-143">/APP1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="96640-144">2</span><span class="sxs-lookup"><span data-stu-id="96640-144">2</span></span>     | <span data-ttu-id="96640-145">/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="96640-146">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="96640-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="96640-147">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="96640-147">Read Paths</span></span>



| <span data-ttu-id="96640-148">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-148">Order</span></span> | <span data-ttu-id="96640-149">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-149">Path</span></span>                           | <span data-ttu-id="96640-150">Формат диска</span><span class="sxs-lookup"><span data-stu-id="96640-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="96640-151">1</span><span class="sxs-lookup"><span data-stu-id="96640-151">1</span></span>     | <span data-ttu-id="96640-152">/ИФД/{ушорт = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="96640-153">ushort</span><span class="sxs-lookup"><span data-stu-id="96640-153">ushort</span></span>      |
| <span data-ttu-id="96640-154">2</span><span class="sxs-lookup"><span data-stu-id="96640-154">2</span></span>     | <span data-ttu-id="96640-155">/ИФД/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="96640-156">Юникод</span><span class="sxs-lookup"><span data-stu-id="96640-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="96640-157">Пути записи</span><span class="sxs-lookup"><span data-stu-id="96640-157">Write Paths</span></span>



| <span data-ttu-id="96640-158">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-158">Order</span></span> | <span data-ttu-id="96640-159">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-159">Path</span></span>                           | <span data-ttu-id="96640-160">Формат диска</span><span class="sxs-lookup"><span data-stu-id="96640-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="96640-161">1</span><span class="sxs-lookup"><span data-stu-id="96640-161">1</span></span>     | <span data-ttu-id="96640-162">/ИФД/{ушорт = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="96640-163">ushort</span><span class="sxs-lookup"><span data-stu-id="96640-163">ushort</span></span>      |
| <span data-ttu-id="96640-164">2</span><span class="sxs-lookup"><span data-stu-id="96640-164">2</span></span>     | <span data-ttu-id="96640-165">/ИФД/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="96640-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="96640-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="96640-167">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="96640-167">Remove Paths</span></span>



| <span data-ttu-id="96640-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="96640-168">Order</span></span> | <span data-ttu-id="96640-169">Путь</span><span class="sxs-lookup"><span data-stu-id="96640-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="96640-170">1</span><span class="sxs-lookup"><span data-stu-id="96640-170">1</span></span>     | <span data-ttu-id="96640-171">/ИФД/{ушорт = 18249}</span><span class="sxs-lookup"><span data-stu-id="96640-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="96640-172">2</span><span class="sxs-lookup"><span data-stu-id="96640-172">2</span></span>     | <span data-ttu-id="96640-173">/ИФД/КСМП/микрософтфото: Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="96640-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96640-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="96640-175">См. также</span><span class="sxs-lookup"><span data-stu-id="96640-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96640-176">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="96640-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
