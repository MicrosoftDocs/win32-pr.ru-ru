---
description: Политика метаданных фотографии для свойства System. Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Политика метаданных фотографии System. Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702739"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="e08e2-103">Политика метаданных фотографии System. Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="e08e2-104">Политика метаданных фотографии для свойства [System. Title](../properties/props-system-title.md) .</span><span class="sxs-lookup"><span data-stu-id="e08e2-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e08e2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e08e2-105">PKEY</span></span>

<span data-ttu-id="e08e2-106">\_Название PKEY</span><span class="sxs-lookup"><span data-stu-id="e08e2-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="e08e2-107">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="e08e2-107">Containers</span></span>

<span data-ttu-id="e08e2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e08e2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e08e2-109">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e08e2-109">Read-Only</span></span>

<span data-ttu-id="e08e2-110">Нет</span><span class="sxs-lookup"><span data-stu-id="e08e2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e08e2-111">Тип выходного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e08e2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e08e2-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e08e2-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e08e2-113">Тип входного ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="e08e2-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e08e2-114">VT \_ LPWSTR или VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="e08e2-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e08e2-115">Политика разрешения конфликтов</span><span class="sxs-lookup"><span data-stu-id="e08e2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e08e2-116">Выверяются значения из разных схем.</span><span class="sxs-lookup"><span data-stu-id="e08e2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e08e2-117">Политика JPEG</span><span class="sxs-lookup"><span data-stu-id="e08e2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e08e2-118">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e08e2-118">Read Paths</span></span>



| <span data-ttu-id="e08e2-119">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-119">Order</span></span> | <span data-ttu-id="e08e2-120">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-120">Path</span></span>                                | <span data-ttu-id="e08e2-121">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e08e2-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="e08e2-122">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-122">1</span></span>     | <span data-ttu-id="e08e2-123">/APP1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="e08e2-124">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="e08e2-124">unicode\_bytes</span></span> |
| <span data-ttu-id="e08e2-125">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-125">2</span></span>     | <span data-ttu-id="e08e2-126">/КСМП/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="e08e2-127">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-127">unicode</span></span>        |
| <span data-ttu-id="e08e2-128">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-128">3</span></span>     | <span data-ttu-id="e08e2-129">/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="e08e2-130">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-130">unicode</span></span>        |
| <span data-ttu-id="e08e2-131">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-131">4</span></span>     | <span data-ttu-id="e08e2-132">/APP1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="e08e2-133">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-133">unicode</span></span>        |
| <span data-ttu-id="e08e2-134">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-134">5</span></span>     | <span data-ttu-id="e08e2-135">/APP1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="e08e2-136">ascii</span><span class="sxs-lookup"><span data-stu-id="e08e2-136">ascii</span></span>          |
| <span data-ttu-id="e08e2-137">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-137">6</span></span>     | <span data-ttu-id="e08e2-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="e08e2-139">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-139">7</span></span>     | <span data-ttu-id="e08e2-140">/КСМП/ <xmpalt> DC: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="e08e2-141">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-141">unicode</span></span>        |
| <span data-ttu-id="e08e2-142">8</span><span class="sxs-lookup"><span data-stu-id="e08e2-142">8</span></span>     | <span data-ttu-id="e08e2-143">/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="e08e2-144">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-144">unicode</span></span>        |
| <span data-ttu-id="e08e2-145">9</span><span class="sxs-lookup"><span data-stu-id="e08e2-145">9</span></span>     | <span data-ttu-id="e08e2-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="e08e2-147">10</span><span class="sxs-lookup"><span data-stu-id="e08e2-147">10</span></span>    | <span data-ttu-id="e08e2-148">/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="e08e2-149">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="e08e2-150">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e08e2-150">Write Paths</span></span>



| <span data-ttu-id="e08e2-151">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-151">Order</span></span> | <span data-ttu-id="e08e2-152">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-152">Path</span></span>                                | <span data-ttu-id="e08e2-153">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e08e2-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="e08e2-154">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-154">1</span></span>     | <span data-ttu-id="e08e2-155">/APP1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="e08e2-156">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="e08e2-156">unicode\_bytes</span></span> |
| <span data-ttu-id="e08e2-157">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-157">2</span></span>     | <span data-ttu-id="e08e2-158">/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="e08e2-159">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-159">unicode</span></span>        |
| <span data-ttu-id="e08e2-160">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-160">3</span></span>     | <span data-ttu-id="e08e2-161">/КСМП/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="e08e2-162">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-162">unicode</span></span>        |
| <span data-ttu-id="e08e2-163">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-163">4</span></span>     | <span data-ttu-id="e08e2-164">/APP1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="e08e2-165">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-165">unicode</span></span>        |
| <span data-ttu-id="e08e2-166">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-166">5</span></span>     | <span data-ttu-id="e08e2-167">/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="e08e2-168">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-168">unicode</span></span>        |
| <span data-ttu-id="e08e2-169">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-169">6</span></span>     | <span data-ttu-id="e08e2-170">/APP1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="e08e2-171">ascii</span><span class="sxs-lookup"><span data-stu-id="e08e2-171">ascii</span></span>          |
| <span data-ttu-id="e08e2-172">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-172">7</span></span>     | <span data-ttu-id="e08e2-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="e08e2-174">8</span><span class="sxs-lookup"><span data-stu-id="e08e2-174">8</span></span>     | <span data-ttu-id="e08e2-175">/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="e08e2-176">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-176">unicode</span></span>        |
| <span data-ttu-id="e08e2-177">9</span><span class="sxs-lookup"><span data-stu-id="e08e2-177">9</span></span>     | <span data-ttu-id="e08e2-178">/КСМП/ <xmpalt> DC: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="e08e2-179">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="e08e2-180">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e08e2-180">Remove Paths</span></span>



| <span data-ttu-id="e08e2-181">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-181">Order</span></span> | <span data-ttu-id="e08e2-182">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="e08e2-183">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-183">1</span></span>     | <span data-ttu-id="e08e2-184">/APP1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="e08e2-185">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-185">2</span></span>     | <span data-ttu-id="e08e2-186">/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="e08e2-187">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-187">3</span></span>     | <span data-ttu-id="e08e2-188">/APP1/IFD/EXIF/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="e08e2-189">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-189">4</span></span>     | <span data-ttu-id="e08e2-190">/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="e08e2-191">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-191">5</span></span>     | <span data-ttu-id="e08e2-192">/APP1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="e08e2-193">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-193">6</span></span>     | <span data-ttu-id="e08e2-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="e08e2-195">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-195">7</span></span>     | <span data-ttu-id="e08e2-196">/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="e08e2-197">Политика TIFF</span><span class="sxs-lookup"><span data-stu-id="e08e2-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e08e2-198">Пути чтения</span><span class="sxs-lookup"><span data-stu-id="e08e2-198">Read Paths</span></span>



| <span data-ttu-id="e08e2-199">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-199">Order</span></span> | <span data-ttu-id="e08e2-200">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-200">Path</span></span>                                    | <span data-ttu-id="e08e2-201">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e08e2-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="e08e2-202">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-202">1</span></span>     | <span data-ttu-id="e08e2-203">/ИФД/{ушорт = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="e08e2-204">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="e08e2-204">unicode\_bytes</span></span> |
| <span data-ttu-id="e08e2-205">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-205">2</span></span>     | <span data-ttu-id="e08e2-206">/ИФД/КСМП/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="e08e2-207">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-207">unicode</span></span>        |
| <span data-ttu-id="e08e2-208">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-208">3</span></span>     | <span data-ttu-id="e08e2-209">/ИФД/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="e08e2-210">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-210">unicode</span></span>        |
| <span data-ttu-id="e08e2-211">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-211">4</span></span>     | <span data-ttu-id="e08e2-212">/ИФД/ексиф/{ушорт = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="e08e2-213">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-213">unicode</span></span>        |
| <span data-ttu-id="e08e2-214">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-214">5</span></span>     | <span data-ttu-id="e08e2-215">/ИФД/{ушорт = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="e08e2-216">ascii</span><span class="sxs-lookup"><span data-stu-id="e08e2-216">ascii</span></span>          |
| <span data-ttu-id="e08e2-217">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-217">6</span></span>     | <span data-ttu-id="e08e2-218">/ифд/иптк/каптион</span><span class="sxs-lookup"><span data-stu-id="e08e2-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="e08e2-219">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-219">7</span></span>     | <span data-ttu-id="e08e2-220">/ИФД/КСМП/ <xmpalt> DC: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="e08e2-221">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-221">unicode</span></span>        |
| <span data-ttu-id="e08e2-222">8</span><span class="sxs-lookup"><span data-stu-id="e08e2-222">8</span></span>     | <span data-ttu-id="e08e2-223">/ИФД/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="e08e2-224">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-224">unicode</span></span>        |
| <span data-ttu-id="e08e2-225">9</span><span class="sxs-lookup"><span data-stu-id="e08e2-225">9</span></span>     | <span data-ttu-id="e08e2-226">/ифд/иптк/каптион</span><span class="sxs-lookup"><span data-stu-id="e08e2-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="e08e2-227">10</span><span class="sxs-lookup"><span data-stu-id="e08e2-227">10</span></span>    | <span data-ttu-id="e08e2-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="e08e2-229">11</span><span class="sxs-lookup"><span data-stu-id="e08e2-229">11</span></span>    | <span data-ttu-id="e08e2-230">/ИФД/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="e08e2-231">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="e08e2-232">Пути записи</span><span class="sxs-lookup"><span data-stu-id="e08e2-232">Write Paths</span></span>



| <span data-ttu-id="e08e2-233">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-233">Order</span></span> | <span data-ttu-id="e08e2-234">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-234">Path</span></span>                                    | <span data-ttu-id="e08e2-235">Формат диска</span><span class="sxs-lookup"><span data-stu-id="e08e2-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="e08e2-236">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-236">1</span></span>     | <span data-ttu-id="e08e2-237">/ИФД/{ушорт = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="e08e2-238">байт в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="e08e2-238">unicode\_bytes</span></span> |
| <span data-ttu-id="e08e2-239">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-239">2</span></span>     | <span data-ttu-id="e08e2-240">/ИФД/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="e08e2-241">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-241">unicode</span></span>        |
| <span data-ttu-id="e08e2-242">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-242">3</span></span>     | <span data-ttu-id="e08e2-243">/ИФД/КСМП/ <xmpalt> DC: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="e08e2-244">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-244">unicode</span></span>        |
| <span data-ttu-id="e08e2-245">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-245">4</span></span>     | <span data-ttu-id="e08e2-246">/ИФД/ексиф/{ушорт = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="e08e2-247">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-247">unicode</span></span>        |
| <span data-ttu-id="e08e2-248">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-248">5</span></span>     | <span data-ttu-id="e08e2-249">/ИФД/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="e08e2-250">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-250">unicode</span></span>        |
| <span data-ttu-id="e08e2-251">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-251">6</span></span>     | <span data-ttu-id="e08e2-252">/ИФД/{ушорт = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="e08e2-253">ascii</span><span class="sxs-lookup"><span data-stu-id="e08e2-253">ascii</span></span>          |
| <span data-ttu-id="e08e2-254">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-254">7</span></span>     | <span data-ttu-id="e08e2-255">/ифд/иптк/каптион</span><span class="sxs-lookup"><span data-stu-id="e08e2-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="e08e2-256">8</span><span class="sxs-lookup"><span data-stu-id="e08e2-256">8</span></span>     | <span data-ttu-id="e08e2-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="e08e2-258">9</span><span class="sxs-lookup"><span data-stu-id="e08e2-258">9</span></span>     | <span data-ttu-id="e08e2-259">/ИФД/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="e08e2-260">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-260">unicode</span></span>        |
| <span data-ttu-id="e08e2-261">10</span><span class="sxs-lookup"><span data-stu-id="e08e2-261">10</span></span>    | <span data-ttu-id="e08e2-262">/ИФД/КСМП/ <xmpalt> DC: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="e08e2-263">Юникод</span><span class="sxs-lookup"><span data-stu-id="e08e2-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="e08e2-264">Удалить пути</span><span class="sxs-lookup"><span data-stu-id="e08e2-264">Remove Paths</span></span>



| <span data-ttu-id="e08e2-265">Заказ</span><span class="sxs-lookup"><span data-stu-id="e08e2-265">Order</span></span> | <span data-ttu-id="e08e2-266">Путь</span><span class="sxs-lookup"><span data-stu-id="e08e2-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="e08e2-267">1</span><span class="sxs-lookup"><span data-stu-id="e08e2-267">1</span></span>     | <span data-ttu-id="e08e2-268">/ИФД/{ушорт = 40091}</span><span class="sxs-lookup"><span data-stu-id="e08e2-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="e08e2-269">2</span><span class="sxs-lookup"><span data-stu-id="e08e2-269">2</span></span>     | <span data-ttu-id="e08e2-270">/ИФД/КСМП/ДК: Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="e08e2-271">3</span><span class="sxs-lookup"><span data-stu-id="e08e2-271">3</span></span>     | <span data-ttu-id="e08e2-272">/ИФД/ексиф/{ушорт = 37510}</span><span class="sxs-lookup"><span data-stu-id="e08e2-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="e08e2-273">4</span><span class="sxs-lookup"><span data-stu-id="e08e2-273">4</span></span>     | <span data-ttu-id="e08e2-274">/ИФД/КСМП/ <xmpalt> EXIF: усеркоммент</span><span class="sxs-lookup"><span data-stu-id="e08e2-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="e08e2-275">5</span><span class="sxs-lookup"><span data-stu-id="e08e2-275">5</span></span>     | <span data-ttu-id="e08e2-276">/ИФД/{ушорт = 270}</span><span class="sxs-lookup"><span data-stu-id="e08e2-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="e08e2-277">6</span><span class="sxs-lookup"><span data-stu-id="e08e2-277">6</span></span>     | <span data-ttu-id="e08e2-278">/ифд/иптк/каптион</span><span class="sxs-lookup"><span data-stu-id="e08e2-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="e08e2-279">7</span><span class="sxs-lookup"><span data-stu-id="e08e2-279">7</span></span>     | <span data-ttu-id="e08e2-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="e08e2-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="e08e2-281">8</span><span class="sxs-lookup"><span data-stu-id="e08e2-281">8</span></span>     | <span data-ttu-id="e08e2-282">/ИФД/КСМП/ДК: описание</span><span class="sxs-lookup"><span data-stu-id="e08e2-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="e08e2-283">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e08e2-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e08e2-284">См. также</span><span class="sxs-lookup"><span data-stu-id="e08e2-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e08e2-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="e08e2-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
