---
description: Политика метаданных фотографии для свойства System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Политика метаданных фотографии System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719694"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="d0673-103">Политика метаданных фотографии System. Author</span><span class="sxs-lookup"><span data-stu-id="d0673-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="d0673-104">Политика метаданных фотографии для свойства [System. Author](../properties/props-system-author.md) .</span><span class="sxs-lookup"><span data-stu-id="d0673-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d0673-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d0673-105">PKEY</span></span>

<span data-ttu-id="d0673-106">\_Автор PKEY</span><span class="sxs-lookup"><span data-stu-id="d0673-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="d0673-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="d0673-107">Containers</span></span>

<span data-ttu-id="d0673-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d0673-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d0673-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0673-109">Read-Only</span></span>

<span data-ttu-id="d0673-110">Нет</span><span class="sxs-lookup"><span data-stu-id="d0673-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d0673-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="d0673-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d0673-112">VT \_ Векторная \| \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d0673-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d0673-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="d0673-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d0673-114">\_Предпочтителен VT Vector \| VT \_ , но \_ также принимается VT LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d0673-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d0673-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="d0673-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d0673-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="d0673-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d0673-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="d0673-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d0673-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="d0673-118">Read Paths</span></span>



| <span data-ttu-id="d0673-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-119">Order</span></span> | <span data-ttu-id="d0673-120">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-120">Path</span></span>                             | <span data-ttu-id="d0673-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="d0673-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="d0673-122">1</span><span class="sxs-lookup"><span data-stu-id="d0673-122">1</span></span>     | <span data-ttu-id="d0673-123">/APP1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="d0673-124">ascii</span><span class="sxs-lookup"><span data-stu-id="d0673-124">ascii</span></span>          |
| <span data-ttu-id="d0673-125">2</span><span class="sxs-lookup"><span data-stu-id="d0673-125">2</span></span>     | <span data-ttu-id="d0673-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="d0673-127">3</span><span class="sxs-lookup"><span data-stu-id="d0673-127">3</span></span>     | <span data-ttu-id="d0673-128">/КСМП/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="d0673-129">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-129">unicode</span></span>        |
| <span data-ttu-id="d0673-130">4</span><span class="sxs-lookup"><span data-stu-id="d0673-130">4</span></span>     | <span data-ttu-id="d0673-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="d0673-132">5</span><span class="sxs-lookup"><span data-stu-id="d0673-132">5</span></span>     | <span data-ttu-id="d0673-133">/APP1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="d0673-134">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="d0673-134">unicode\_bytes</span></span> |
| <span data-ttu-id="d0673-135">6</span><span class="sxs-lookup"><span data-stu-id="d0673-135">6</span></span>     | <span data-ttu-id="d0673-136">/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="d0673-137">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="d0673-138">Пути записи</span><span class="sxs-lookup"><span data-stu-id="d0673-138">Write Paths</span></span>



| <span data-ttu-id="d0673-139">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-139">Order</span></span> | <span data-ttu-id="d0673-140">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-140">Path</span></span>                             | <span data-ttu-id="d0673-141">Формат диска</span><span class="sxs-lookup"><span data-stu-id="d0673-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="d0673-142">1</span><span class="sxs-lookup"><span data-stu-id="d0673-142">1</span></span>     | <span data-ttu-id="d0673-143">/КСМП/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="d0673-144">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-144">unicode</span></span>        |
| <span data-ttu-id="d0673-145">2</span><span class="sxs-lookup"><span data-stu-id="d0673-145">2</span></span>     | <span data-ttu-id="d0673-146">/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="d0673-147">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-147">unicode</span></span>        |
| <span data-ttu-id="d0673-148">3</span><span class="sxs-lookup"><span data-stu-id="d0673-148">3</span></span>     | <span data-ttu-id="d0673-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="d0673-150">4</span><span class="sxs-lookup"><span data-stu-id="d0673-150">4</span></span>     | <span data-ttu-id="d0673-151">/APP1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="d0673-152">ascii</span><span class="sxs-lookup"><span data-stu-id="d0673-152">ascii</span></span>          |
| <span data-ttu-id="d0673-153">5</span><span class="sxs-lookup"><span data-stu-id="d0673-153">5</span></span>     | <span data-ttu-id="d0673-154">/APP1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="d0673-155">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="d0673-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="d0673-156">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="d0673-156">Remove Paths</span></span>



| <span data-ttu-id="d0673-157">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-157">Order</span></span> | <span data-ttu-id="d0673-158">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="d0673-159">1</span><span class="sxs-lookup"><span data-stu-id="d0673-159">1</span></span>     | <span data-ttu-id="d0673-160">/КСМП/ДК: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="d0673-161">2</span><span class="sxs-lookup"><span data-stu-id="d0673-161">2</span></span>     | <span data-ttu-id="d0673-162">/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="d0673-163">3</span><span class="sxs-lookup"><span data-stu-id="d0673-163">3</span></span>     | <span data-ttu-id="d0673-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="d0673-165">4</span><span class="sxs-lookup"><span data-stu-id="d0673-165">4</span></span>     | <span data-ttu-id="d0673-166">/APP1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="d0673-167">5</span><span class="sxs-lookup"><span data-stu-id="d0673-167">5</span></span>     | <span data-ttu-id="d0673-168">/APP1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="d0673-169">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="d0673-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d0673-170">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="d0673-170">Read Paths</span></span>



| <span data-ttu-id="d0673-171">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-171">Order</span></span> | <span data-ttu-id="d0673-172">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-172">Path</span></span>                              | <span data-ttu-id="d0673-173">Формат диска</span><span class="sxs-lookup"><span data-stu-id="d0673-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="d0673-174">1</span><span class="sxs-lookup"><span data-stu-id="d0673-174">1</span></span>     | <span data-ttu-id="d0673-175">/ИФД/{ушорт = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="d0673-176">ascii</span><span class="sxs-lookup"><span data-stu-id="d0673-176">ascii</span></span>          |
| <span data-ttu-id="d0673-177">2</span><span class="sxs-lookup"><span data-stu-id="d0673-177">2</span></span>     | <span data-ttu-id="d0673-178">/ифд/иптк/би-лине</span><span class="sxs-lookup"><span data-stu-id="d0673-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="d0673-179">3</span><span class="sxs-lookup"><span data-stu-id="d0673-179">3</span></span>     | <span data-ttu-id="d0673-180">/ИФД/КСМП/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="d0673-181">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-181">unicode</span></span>        |
| <span data-ttu-id="d0673-182">4</span><span class="sxs-lookup"><span data-stu-id="d0673-182">4</span></span>     | <span data-ttu-id="d0673-183">/ифд/иптк/би-лине</span><span class="sxs-lookup"><span data-stu-id="d0673-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="d0673-184">5</span><span class="sxs-lookup"><span data-stu-id="d0673-184">5</span></span>     | <span data-ttu-id="d0673-185">/ИФД/{ушорт = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="d0673-186">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="d0673-186">unicode\_bytes</span></span> |
| <span data-ttu-id="d0673-187">6</span><span class="sxs-lookup"><span data-stu-id="d0673-187">6</span></span>     | <span data-ttu-id="d0673-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="d0673-189">7</span><span class="sxs-lookup"><span data-stu-id="d0673-189">7</span></span>     | <span data-ttu-id="d0673-190">/ИФД/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="d0673-191">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="d0673-192">Пути записи</span><span class="sxs-lookup"><span data-stu-id="d0673-192">Write Paths</span></span>



| <span data-ttu-id="d0673-193">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-193">Order</span></span> | <span data-ttu-id="d0673-194">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-194">Path</span></span>                              | <span data-ttu-id="d0673-195">Формат диска</span><span class="sxs-lookup"><span data-stu-id="d0673-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="d0673-196">1</span><span class="sxs-lookup"><span data-stu-id="d0673-196">1</span></span>     | <span data-ttu-id="d0673-197">/ИФД/КСМП/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="d0673-198">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-198">unicode</span></span>        |
| <span data-ttu-id="d0673-199">2</span><span class="sxs-lookup"><span data-stu-id="d0673-199">2</span></span>     | <span data-ttu-id="d0673-200">/ИФД/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="d0673-201">Юникод</span><span class="sxs-lookup"><span data-stu-id="d0673-201">unicode</span></span>        |
| <span data-ttu-id="d0673-202">3</span><span class="sxs-lookup"><span data-stu-id="d0673-202">3</span></span>     | <span data-ttu-id="d0673-203">/ифд/иптк/би-лине</span><span class="sxs-lookup"><span data-stu-id="d0673-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="d0673-204">4</span><span class="sxs-lookup"><span data-stu-id="d0673-204">4</span></span>     | <span data-ttu-id="d0673-205">/ИФД/{ушорт = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="d0673-206">\_вектор ASCII</span><span class="sxs-lookup"><span data-stu-id="d0673-206">ascii\_vector</span></span>  |
| <span data-ttu-id="d0673-207">5</span><span class="sxs-lookup"><span data-stu-id="d0673-207">5</span></span>     | <span data-ttu-id="d0673-208">/ИФД/{ушорт = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="d0673-209">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="d0673-209">unicode\_bytes</span></span> |
| <span data-ttu-id="d0673-210">6</span><span class="sxs-lookup"><span data-stu-id="d0673-210">6</span></span>     | <span data-ttu-id="d0673-211">/ифд/иптк/би-лине</span><span class="sxs-lookup"><span data-stu-id="d0673-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="d0673-212">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="d0673-212">Remove Paths</span></span>



| <span data-ttu-id="d0673-213">Заказ</span><span class="sxs-lookup"><span data-stu-id="d0673-213">Order</span></span> | <span data-ttu-id="d0673-214">Путь</span><span class="sxs-lookup"><span data-stu-id="d0673-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="d0673-215">1</span><span class="sxs-lookup"><span data-stu-id="d0673-215">1</span></span>     | <span data-ttu-id="d0673-216">/ИФД/КСМП/ДК: Creator</span><span class="sxs-lookup"><span data-stu-id="d0673-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="d0673-217">2</span><span class="sxs-lookup"><span data-stu-id="d0673-217">2</span></span>     | <span data-ttu-id="d0673-218">/ИФД/КСМП/Тифф: исполнитель</span><span class="sxs-lookup"><span data-stu-id="d0673-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="d0673-219">3</span><span class="sxs-lookup"><span data-stu-id="d0673-219">3</span></span>     | <span data-ttu-id="d0673-220">/ифд/иптк/би-лине</span><span class="sxs-lookup"><span data-stu-id="d0673-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="d0673-221">4</span><span class="sxs-lookup"><span data-stu-id="d0673-221">4</span></span>     | <span data-ttu-id="d0673-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="d0673-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="d0673-223">5</span><span class="sxs-lookup"><span data-stu-id="d0673-223">5</span></span>     | <span data-ttu-id="d0673-224">/ИФД/{ушорт = 315}</span><span class="sxs-lookup"><span data-stu-id="d0673-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="d0673-225">6</span><span class="sxs-lookup"><span data-stu-id="d0673-225">6</span></span>     | <span data-ttu-id="d0673-226">/ИФД/{ушорт = 40093}</span><span class="sxs-lookup"><span data-stu-id="d0673-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="d0673-227">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0673-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0673-228">См. также</span><span class="sxs-lookup"><span data-stu-id="d0673-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0673-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="d0673-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
