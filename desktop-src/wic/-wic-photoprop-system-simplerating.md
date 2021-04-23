---
description: Политика метаданных фотографии для свойства System. Симплератинг.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Политика метаданных фотографии System. Симплератинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081300"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="490d5-103">Политика метаданных фотографии System. Симплератинг</span><span class="sxs-lookup"><span data-stu-id="490d5-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="490d5-104">Политика метаданных фотографии для свойства [System. симплератинг](../properties/props-system-simplerating.md) .</span><span class="sxs-lookup"><span data-stu-id="490d5-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="490d5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="490d5-105">PKEY</span></span>

<span data-ttu-id="490d5-106">PKEY \_ симплератинг</span><span class="sxs-lookup"><span data-stu-id="490d5-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="490d5-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="490d5-107">Containers</span></span>

<span data-ttu-id="490d5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="490d5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="490d5-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="490d5-109">Read-Only</span></span>

<span data-ttu-id="490d5-110">Нет</span><span class="sxs-lookup"><span data-stu-id="490d5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="490d5-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="490d5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="490d5-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="490d5-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="490d5-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="490d5-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="490d5-114">Может быть VT \_ UI1, VT \_ UI2 или VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="490d5-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="490d5-115">Целочисленное значение может находиться в диапазоне от 0 до 5.</span><span class="sxs-lookup"><span data-stu-id="490d5-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="490d5-116">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="490d5-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="490d5-117">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="490d5-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="490d5-118">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="490d5-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="490d5-119">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="490d5-119">Read Paths</span></span>



| <span data-ttu-id="490d5-120">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-120">Order</span></span> | <span data-ttu-id="490d5-121">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-121">Path</span></span>                     | <span data-ttu-id="490d5-122">Формат диска</span><span class="sxs-lookup"><span data-stu-id="490d5-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="490d5-123">1</span><span class="sxs-lookup"><span data-stu-id="490d5-123">1</span></span>     | <span data-ttu-id="490d5-124">/APP1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="490d5-125">ushort</span><span class="sxs-lookup"><span data-stu-id="490d5-125">ushort</span></span>      |
| <span data-ttu-id="490d5-126">2</span><span class="sxs-lookup"><span data-stu-id="490d5-126">2</span></span>     | <span data-ttu-id="490d5-127">/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="490d5-128">Юникод</span><span class="sxs-lookup"><span data-stu-id="490d5-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="490d5-129">Пути записи</span><span class="sxs-lookup"><span data-stu-id="490d5-129">Write Paths</span></span>



| <span data-ttu-id="490d5-130">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-130">Order</span></span> | <span data-ttu-id="490d5-131">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-131">Path</span></span>                     | <span data-ttu-id="490d5-132">Формат диска</span><span class="sxs-lookup"><span data-stu-id="490d5-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="490d5-133">1</span><span class="sxs-lookup"><span data-stu-id="490d5-133">1</span></span>     | <span data-ttu-id="490d5-134">/APP1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="490d5-135">ushort</span><span class="sxs-lookup"><span data-stu-id="490d5-135">ushort</span></span>      |
| <span data-ttu-id="490d5-136">2</span><span class="sxs-lookup"><span data-stu-id="490d5-136">2</span></span>     | <span data-ttu-id="490d5-137">/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="490d5-138">Юникод</span><span class="sxs-lookup"><span data-stu-id="490d5-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="490d5-139">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="490d5-139">Remove Paths</span></span>



| <span data-ttu-id="490d5-140">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-140">Order</span></span> | <span data-ttu-id="490d5-141">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="490d5-142">1</span><span class="sxs-lookup"><span data-stu-id="490d5-142">1</span></span>     | <span data-ttu-id="490d5-143">/APP1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="490d5-144">2</span><span class="sxs-lookup"><span data-stu-id="490d5-144">2</span></span>     | <span data-ttu-id="490d5-145">/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="490d5-146">Политики TIFF</span><span class="sxs-lookup"><span data-stu-id="490d5-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="490d5-147">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="490d5-147">Read Paths</span></span>



| <span data-ttu-id="490d5-148">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-148">Order</span></span> | <span data-ttu-id="490d5-149">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-149">Path</span></span>                | <span data-ttu-id="490d5-150">Формат диска</span><span class="sxs-lookup"><span data-stu-id="490d5-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="490d5-151">1</span><span class="sxs-lookup"><span data-stu-id="490d5-151">1</span></span>     | <span data-ttu-id="490d5-152">/ИФД/{ушорт = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="490d5-153">ushort</span><span class="sxs-lookup"><span data-stu-id="490d5-153">ushort</span></span>      |
| <span data-ttu-id="490d5-154">2</span><span class="sxs-lookup"><span data-stu-id="490d5-154">2</span></span>     | <span data-ttu-id="490d5-155">/ИФД/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="490d5-156">Юникод</span><span class="sxs-lookup"><span data-stu-id="490d5-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="490d5-157">Пути записи</span><span class="sxs-lookup"><span data-stu-id="490d5-157">Write Paths</span></span>



| <span data-ttu-id="490d5-158">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-158">Order</span></span> | <span data-ttu-id="490d5-159">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-159">Path</span></span>                | <span data-ttu-id="490d5-160">Формат диска</span><span class="sxs-lookup"><span data-stu-id="490d5-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="490d5-161">1</span><span class="sxs-lookup"><span data-stu-id="490d5-161">1</span></span>     | <span data-ttu-id="490d5-162">/ИФД/{ушорт = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="490d5-163">ushort</span><span class="sxs-lookup"><span data-stu-id="490d5-163">ushort</span></span>      |
| <span data-ttu-id="490d5-164">2</span><span class="sxs-lookup"><span data-stu-id="490d5-164">2</span></span>     | <span data-ttu-id="490d5-165">/ИФД/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="490d5-166">Юникод</span><span class="sxs-lookup"><span data-stu-id="490d5-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="490d5-167">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="490d5-167">Remove Paths</span></span>



| <span data-ttu-id="490d5-168">Заказ</span><span class="sxs-lookup"><span data-stu-id="490d5-168">Order</span></span> | <span data-ttu-id="490d5-169">Путь</span><span class="sxs-lookup"><span data-stu-id="490d5-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="490d5-170">1</span><span class="sxs-lookup"><span data-stu-id="490d5-170">1</span></span>     | <span data-ttu-id="490d5-171">/ИФД/{ушорт = 18246}</span><span class="sxs-lookup"><span data-stu-id="490d5-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="490d5-172">2</span><span class="sxs-lookup"><span data-stu-id="490d5-172">2</span></span>     | <span data-ttu-id="490d5-173">/ИФД/КСМП/КСМП: Оценка</span><span class="sxs-lookup"><span data-stu-id="490d5-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="490d5-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="490d5-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="490d5-175">См. также</span><span class="sxs-lookup"><span data-stu-id="490d5-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="490d5-176">System. Симплератинг</span><span class="sxs-lookup"><span data-stu-id="490d5-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
