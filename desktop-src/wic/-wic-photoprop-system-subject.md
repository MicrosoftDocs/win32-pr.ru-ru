---
description: Политика метаданных фотографии для свойства System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Политика метаданных фотографии System. subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702740"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="66df6-103">Политика метаданных фотографии System. subject</span><span class="sxs-lookup"><span data-stu-id="66df6-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="66df6-104">Политика метаданных фотографии для свойства [System. subject](../properties/props-system-subject.md) .</span><span class="sxs-lookup"><span data-stu-id="66df6-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="66df6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="66df6-105">PKEY</span></span>

<span data-ttu-id="66df6-106">\_Тема PKEY</span><span class="sxs-lookup"><span data-stu-id="66df6-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="66df6-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="66df6-107">Containers</span></span>

<span data-ttu-id="66df6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="66df6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="66df6-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="66df6-109">Read-Only</span></span>

<span data-ttu-id="66df6-110">Нет</span><span class="sxs-lookup"><span data-stu-id="66df6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="66df6-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="66df6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="66df6-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66df6-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="66df6-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="66df6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="66df6-114">VT \_ LPWSTR или VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="66df6-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="66df6-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="66df6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="66df6-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="66df6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="66df6-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="66df6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="66df6-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="66df6-118">Read Paths</span></span>



| <span data-ttu-id="66df6-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-119">Order</span></span> | <span data-ttu-id="66df6-120">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-120">Path</span></span>                     | <span data-ttu-id="66df6-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="66df6-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="66df6-122">1</span><span class="sxs-lookup"><span data-stu-id="66df6-122">1</span></span>     | <span data-ttu-id="66df6-123">/APP1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="66df6-124">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="66df6-124">unicode\_bytes</span></span> |
| <span data-ttu-id="66df6-125">2</span><span class="sxs-lookup"><span data-stu-id="66df6-125">2</span></span>     | <span data-ttu-id="66df6-126">/APP1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="66df6-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="66df6-127">ascii</span><span class="sxs-lookup"><span data-stu-id="66df6-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="66df6-128">Пути записи</span><span class="sxs-lookup"><span data-stu-id="66df6-128">Write Paths</span></span>



| <span data-ttu-id="66df6-129">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-129">Order</span></span> | <span data-ttu-id="66df6-130">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-130">Path</span></span>                     | <span data-ttu-id="66df6-131">Формат диска</span><span class="sxs-lookup"><span data-stu-id="66df6-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="66df6-132">1</span><span class="sxs-lookup"><span data-stu-id="66df6-132">1</span></span>     | <span data-ttu-id="66df6-133">/APP1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="66df6-134">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="66df6-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="66df6-135">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="66df6-135">Remove Paths</span></span>



| <span data-ttu-id="66df6-136">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-136">Order</span></span> | <span data-ttu-id="66df6-137">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="66df6-138">1</span><span class="sxs-lookup"><span data-stu-id="66df6-138">1</span></span>     | <span data-ttu-id="66df6-139">/APP1/IFD/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="66df6-140">2</span><span class="sxs-lookup"><span data-stu-id="66df6-140">2</span></span>     | <span data-ttu-id="66df6-141">/APP1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="66df6-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="66df6-142">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="66df6-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="66df6-143">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="66df6-143">Read Paths</span></span>



| <span data-ttu-id="66df6-144">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-144">Order</span></span> | <span data-ttu-id="66df6-145">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-145">Path</span></span>                | <span data-ttu-id="66df6-146">Формат диска</span><span class="sxs-lookup"><span data-stu-id="66df6-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="66df6-147">1</span><span class="sxs-lookup"><span data-stu-id="66df6-147">1</span></span>     | <span data-ttu-id="66df6-148">/ИФД/{ушорт = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="66df6-149">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="66df6-149">unicode\_bytes</span></span> |
| <span data-ttu-id="66df6-150">2</span><span class="sxs-lookup"><span data-stu-id="66df6-150">2</span></span>     | <span data-ttu-id="66df6-151">/ИФД/{ушорт = 270}</span><span class="sxs-lookup"><span data-stu-id="66df6-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="66df6-152">ascii</span><span class="sxs-lookup"><span data-stu-id="66df6-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="66df6-153">Пути записи</span><span class="sxs-lookup"><span data-stu-id="66df6-153">Write Paths</span></span>



| <span data-ttu-id="66df6-154">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-154">Order</span></span> | <span data-ttu-id="66df6-155">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-155">Path</span></span>                | <span data-ttu-id="66df6-156">Формат диска</span><span class="sxs-lookup"><span data-stu-id="66df6-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="66df6-157">1</span><span class="sxs-lookup"><span data-stu-id="66df6-157">1</span></span>     | <span data-ttu-id="66df6-158">/ИФД/{ушорт = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="66df6-159">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="66df6-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="66df6-160">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="66df6-160">Remove Paths</span></span>



| <span data-ttu-id="66df6-161">Заказ</span><span class="sxs-lookup"><span data-stu-id="66df6-161">Order</span></span> | <span data-ttu-id="66df6-162">Путь</span><span class="sxs-lookup"><span data-stu-id="66df6-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="66df6-163">1</span><span class="sxs-lookup"><span data-stu-id="66df6-163">1</span></span>     | <span data-ttu-id="66df6-164">/ИФД/{ушорт = 40095}</span><span class="sxs-lookup"><span data-stu-id="66df6-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="66df6-165">2</span><span class="sxs-lookup"><span data-stu-id="66df6-165">2</span></span>     | <span data-ttu-id="66df6-166">/ИФД/{ушорт = 270}</span><span class="sxs-lookup"><span data-stu-id="66df6-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="66df6-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66df6-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="66df6-168">См. также</span><span class="sxs-lookup"><span data-stu-id="66df6-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66df6-169">System. subject</span><span class="sxs-lookup"><span data-stu-id="66df6-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
